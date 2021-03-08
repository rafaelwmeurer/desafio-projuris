ARG VERSION_ARG=alpine
FROM node:$VERSION_ARG

ARG PORT_ARG=3001
ENV PORT $PORT_ARG

WORKDIR /app

COPY package.json /app
COPY app.js /app
COPY ./bin /app/bin

RUN chown -R node:node /app
USER node

RUN npm i

EXPOSE $PORT_ARG

CMD [ "node", "./bin/www" ]
