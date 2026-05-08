# Use a lightweight Node.js base image
FROM node:20-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies (only production dependencies are needed for the final image)
RUN npm install --production

# Copy the rest of the backend application code
COPY . .

# Expose the port the app runs on
EXPOSE 5000

# Define the command to start the application
CMD ["npm", "start"]
