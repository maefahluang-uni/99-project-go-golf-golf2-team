FROM node:7.7-alpine

ADD package.json /tmp/package.json
RUN cd /tmp && npm install
RUN mkdir -p /opt/hellojs-app
RUN cp -a /tmp/node_modules /usr/src/demojs
WORKDIR /usr/src/demojs
ADD . /usr/src/demojs
RUN npm run build
EXPOSE 3000
CMD ["npm","start"]
