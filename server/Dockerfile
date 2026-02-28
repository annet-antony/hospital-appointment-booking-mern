# Use an official Node runtime as a parent image
FROM node:12

# Set the working directory in the container to /app
WORKDIR /app

# Add the current directory contents into the container at /app
ADD . /app

COPY package*.json /app
RUN npm install

EXPOSE 5000

# Run server.py when the container launches
CMD ["npm", "start"]