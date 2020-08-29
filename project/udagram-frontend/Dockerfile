# Use NodeJS base image
FROM beevelop/ionic:latest

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies by copying
# package.json and package-lock.json
COPY *.json ./

# Copy app source
COPY src ./src
COPY e2e ./e2e

# Install dependencies
RUN npm install
# Build ionic for production
RUN ionic build

# Bind the port that the image will run on
EXPOSE 8100

# Define the Docker image's behavior at runtime
CMD ["ionic", "serve"]
