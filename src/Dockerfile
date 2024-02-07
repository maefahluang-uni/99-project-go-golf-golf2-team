FROM node:7.7-alpine

# Install dependencies
ADD package.json /tmp/package.json
RUN cd /tmp && npm install

# Copy dependencies
RUN mkdir -p /opt/demo-app && cp -a /tmp/node_modules /opt/demo

# Setup workdir
WORKDIR /opt/demo-app
COPY . /opt/demo-app

# Run
EXPOSE 3000
CMD ["npm", "start"]
