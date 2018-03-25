## Usage

```
from asia.gcr.io/fapp-c37ca/nginx-node-docker:latest
# Add Node.js app
COPY app /app

# Install app packages
WORKDIR /app

RUN yarn

# Build app packages
RUN yarn build

ENV NODE_MODE prod
ENV NODE_PORT 3000

# Run the startup script
WORKDIR /

CMD ["/start.sh"]
```
