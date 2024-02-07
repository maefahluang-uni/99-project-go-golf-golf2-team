FROM node:7.7-alpine

# Install dependencies
ADD package.json /tmp/package.json
RUN cd /tmp && npm install

# Copy dependencies
RUN mkdir -p /opt/hellojs && cp -a /tmp/node_modules /opt/hellojs

# Setup workdir
WORKDIR /opt/hellojs
COPY . /opt/hellojs

# Run
EXPOSE 3000
CMD ["/usr/local/bin/npm", "start"]
