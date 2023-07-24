# Use an official Node runtime as the parent image
FROM node:latest

# Set the working directory
WORKDIR /src/app

# Add `/usr/src/app/node_modules/.bin` to $PATH
ENV PATH /src/app/node_modules/.bin:$PATH

# Copy package.json and package-lock.json
COPY package*.json ./

# Install application dependencies
RUN npm install --silent

# Copy the rest of the application
COPY . .

# Make port 3000 available to the world outside this container
EXPOSE 3000

# Run the application
CMD [ "npm", "start" ]

