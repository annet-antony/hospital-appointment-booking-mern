# Use an official Node runtime as a parent image
FROM node:12

# Set the working directory in the container to /app
WORKDIR /app

# Add the current directory contents into the container at /app
ADD . /app

# Update pip
# RUN pip3 install --upgrade pip

# Copy local directories to the current local directory of our docker image (/app)
COPY ./src ./src
COPY ./public ./public

# Install node packages, install serve, build the app, and remove dependencies at the end
RUN npm install \
    && npm install -g serve \
    && npm run build \
    && rm -fr node_modules


COPY package*.json /app
RUN npm install

EXPOSE 3000

# Run server.py when the container launches
CMD ["npm", "start"]
