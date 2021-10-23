# Deploying Swagger UI to Infra API.

## As root on the server
## On the server install docker
https://docs.docker.com/engine/install/ubuntu/

## Then get swagger-ui
sudo docker pull swaggerapi/swagger-ui

## running it individually
sudo docker run -d -p 80:8080 -e BASE_URL=/docs -e SWAGGER_JSON=/foo/securesecrets-api-secret-network-3.1.yaml -v ~/docs:/foo swaggerapi/swagger-ui

*** Note
This assumes that the docs folder is `~/docs` is relative to your home directory. Or change path.

## to see logs 
sudo docker logs -f {container-id}