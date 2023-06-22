# Use the official Node.js image as the base
FROM node:14-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the application code to the working directory
COPY . .

# Expose the port that the app will listen on
EXPOSE 3000

# Start the Node.js app
CMD ["node", "app.js"]
