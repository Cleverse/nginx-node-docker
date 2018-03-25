from asia.gcr.io/fapp-c37ca/nginx-node-docker:latest

# Add Node.js app
RUN mkdir /app
WORKDIR /app
COPY package.json /app
RUN yarn

COPY . /app

ENV NODE_MODE prod
ENV NODE_PORT 4000

# Run the startup script
WORKDIR /

CMD ["/start.sh"]