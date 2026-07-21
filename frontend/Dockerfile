# Use Node LTS
FROM node:18-alpine AS builder
WORKDIR /usr/src/app

# Install deps based on package.json
COPY frontend/package.json frontend/package-lock.json* ./
# Allow fallback to npm install when package-lock.json is not present
RUN npm ci || npm install

# Copy source and build
COPY frontend/ ./
RUN npm run build

# Production image
FROM node:18-alpine
WORKDIR /usr/src/app
ENV NODE_ENV=production
COPY --from=builder /usr/src/app/ ./
EXPOSE 3000
CMD ["npm", "run", "start"]
