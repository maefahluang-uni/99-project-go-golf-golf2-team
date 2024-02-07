FROM node:7.7-alpine

# install deps
ADD package.json /tmp/package.json
RUN cd /tmp && npm install

# Copy deps
RUN mkdir -p /opt/demojs-app && cp -a /tmp/node_modules /opt/demojs

# Setup workdir
WORKDIR /opt/demojs-app
COPY . /opt/demojs-app

# run
EXPOSE 3000
CMD ["npm", "start"]
