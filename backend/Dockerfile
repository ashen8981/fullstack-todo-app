# Use an official Node.js runtime as the base image
FROM node:16

# Set the working directory to /app
WORKDIR /app

# Copy the package.json and package-lock.json to install dependencies
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Run TypeScript build to generate the dist folder
RUN npm run build  # Make sure this command generates the dist folder

# Expose the backend port
EXPOSE 5000

# Start the server
CMD ["node", "dist/server.js"]
