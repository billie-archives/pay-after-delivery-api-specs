# Paella API spec

## How to take a look on interactive documentation:

- Run the image from DockerHub
There is a docker image published in [DockerHub](https://hub.docker.com/r/swaggerapi/swagger-editor/).

To use this, run the following:

```
docker pull swaggerapi/swagger-editor
docker run -d -p 80:8080 swaggerapi/swagger-editor
```

This will run Swagger Editor (in detached mode) on port 80 on your machine, so you can open it by navigating to `http://localhost` in your browser.

- Import `swagger.yaml` and run tests

## How to create a library

- Either using swagger UI
- Or by [openapi-generator](https://github.com/OpenAPITools/openapi-generator). E.g. 
```
openapi-generator generate -i https://raw.githubusercontent.com/openapitools/openapi-generator/master/modules/openapi-generator/src/test/resources/2_0/petstore.yaml -g php -o /Volumes/Development/billie/php-paella-api-sdk
```

## List of current SDKs 

To be updated
