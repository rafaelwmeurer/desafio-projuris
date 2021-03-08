# Deliverable 1 - Docker

1. Create a clean web Dockerfile
2. Create a clean api Dockerfile
3. Define a docker-compose.yml in the project root that run the web and api with a simple docker-compose up
4. The docker-compose.yml needs to make the developer life better
5. Publish the image in a public registry with the command docker-compose push web api

OBS: API requires PostgreSQL

## Como utilizar

Basicamente é executar o comando abaixo quando estiver nesta pasta
```sh
docker-compose up
```

## Pontos a serem comentados

Infelizmente as rotas não funcionam, porém eu não foquei em resolver o problema no código, apenas configurei a parte de container que instala as dependências, defini variáveis de ambiente e demais dependências.