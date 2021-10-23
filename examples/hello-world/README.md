# Exemplo de build
O `cloudbuild.yaml` fornecido simplesmente invoca `docker-compose up` que executa um serviço que imprime "Hello world".

```bash
cd fabiojaniolima/docker-compose/examples/hello-world
gcloud builds submit --config=cloudbuild.yaml .
```
