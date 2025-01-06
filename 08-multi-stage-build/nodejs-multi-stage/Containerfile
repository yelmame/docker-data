# Stage 1
# Using lightweight image
FROM node:14 as build

# Set working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install --production

# Copy application files
COPY . .

# Stage 2

FROM node:14-alpine
WORKDIR /app
COPY --from=build /app/ /app
# Expose the port the app runs on
EXPOSE 8090

# Command to run the app
CMD ["node", "app.js"]

