# Stage 1: Build the app
FROM node:18 AS builder

WORKDIR /app

# Install deps
COPY package*.json ./
RUN npm install

# Copy app and env
COPY . .
COPY .env.production .env.production

# Build for production
RUN npm run build

# Stage 2: Serve with Nginx
FROM nginx:alpine
COPY --from=builder /app/dist /usr/share/nginx/html
COPY nginx.conf /etc/nginx/conf.d/default.conf
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
