# Stage 1: Build React app
FROM node:22 AS build

# Set working directory to match assignment instructions
WORKDIR /abao_marissa_ui_garden_build_checks

# Install only package.json and lockfile first for better caching
COPY package*.json ./
RUN npm install

# Copy the rest of the app
COPY . .
RUN npm run build

# Stage 2: Serve with NGINX
FROM nginx:1.25.3

# Copy build output from build stage
COPY --from=build /abao_marissa_ui_garden_build_checks/build /usr/share/nginx/html

# Expose port 80 inside container (mapped to 8018 on host)
EXPOSE 80

# Start NGINX
CMD ["nginx", "-g", "daemon off;"]
