FROM node:lts-alpine3.14

RUN apk update && apk add curl

WORKDIR /app

COPY src/ .

RUN npm install

HEALTHCHECK --interval=45s --timeout=5s --retries=2 --start-period=5s \
    CMD curl -f http://localhost:8080 || exit 1  

ENTRYPOINT [ "npm", "start"]