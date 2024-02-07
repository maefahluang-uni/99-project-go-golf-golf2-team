FROM node:7.7-alpine

# Install dependencies
ADD package.json /tmp/package.json
RUN cd /tmp && npm install

# Copy dependencies
RUN mkdir -p /opt/src && cp -a /tmp/node_modules /opt/src

# Setup workdir
WORKDIR /opt/src
COPY . /opt/src

# Run
EXPOSE 3000
CMD ["npm", "start"]
