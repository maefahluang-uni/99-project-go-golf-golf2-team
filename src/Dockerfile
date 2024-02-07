FROM node:7.7-alpine

# Install dependencies
ADD package.json /tmp/package.json
RUN cd /tmp && npm install

# Copy dependencies
RUN mkdir -p /opt/demojs-app && cp -a /tmp/node_modules /opt/demojs

# Setup workdir
WORKDIR /opt/demojs-app
COPY . /opt/demojs-app

# Run
EXPOSE 3000
CMD ["npm", "start"]
