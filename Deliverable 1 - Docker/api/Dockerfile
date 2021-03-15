ARG VERSION_ARG=alpine
FROM node:$VERSION_ARG

ARG PORT_ARG=3001
ARG DB_ARG=postgres://postgres:postgres@database-postgres:5432/postgres
ENV PORT $PORT_ARG
ENV DB $DB_ARG

WORKDIR /app

COPY package.json /app
COPY app.js /app
COPY ./bin /app/bin

RUN chown -R node:node /app
USER node

RUN npm i

EXPOSE $PORT_ARG

CMD [ "node", "./bin/www" ]
