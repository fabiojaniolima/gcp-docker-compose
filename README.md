# Docker-compose

Possibilita que o comando `docker-compose` seja invocado no [Google Cloud Build](cloud.google.com/cloud-build/).

Os argumentos passados para este construtor/step serão repassados para o `docker-compose`, permitindo desta forma a execução de qualquer instrução [docker-compose command](https://docs.docker.com/compose/reference/overview/).

## Setup

Para disponibilizar este construtor em seu projeto no Google Cloud:

```bash
cd fabiojaniolima/docker-compose
gcloud builds submit --config=cloudbuild.yaml .
```

Para substituir a versão do `docker-compose` que está sendo construída, substitua `_DOCKER_COMPOSE_VERSION`:

```bash
cd fabiojaniolima/docker-compose
gcloud builds submit --config=cloudbuild.yaml --substitutions=_DOCKER_COMPOSE_VERSION="1.24.0"
```

Você pode encontrar uma lista de lançamentos e seus números de versões [aqui](https://github.com/docker/compose/releases).

## Exemplos

Veja o exemplo fornecido [hello-world](./examples/hello-world/).

## Considerações

Fonte: https://github.com/GoogleCloudPlatform/cloud-builders-community/tree/master/docker-compose
