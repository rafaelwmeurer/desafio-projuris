ARG VERSION_ARG=alpine
FROM node:$VERSION_ARG

ARG PORT_ARG=3000
ARG API_HOST_ARG=http://localhost:3001
ENV PORT $PORT_ARG
ENV API_HOST $API_HOST_ARG

WORKDIR /app

COPY package.json /app
COPY app.js /app
COPY ./bin /app/bin
COPY ./public /app/public
COPY ./routes /app/routes
COPY ./views /app/views

RUN chown -R node:node /app
USER node

RUN npm i

EXPOSE $PORT_ARG

CMD [ "node", "./bin/www" ]
