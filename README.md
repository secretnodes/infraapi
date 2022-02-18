# Deploying Swagger UI to Infra API.

## As root on the server
## On the server install docker
https://docs.docker.com/engine/install/ubuntu/

## Then get swagger-ui
sudo docker pull swaggerapi/swagger-ui

## running it individually
sudo docker run -d -e API_URL=https://raw.githubusercontent.com/secretnodes/infraapi/master/docs/secret-4.yaml -p 80:8080 swaggerapi/swagger-ui

## to see logs 
sudo docker logs -f {container-id}
