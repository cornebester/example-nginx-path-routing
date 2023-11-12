# example-nginx-path-routing

Example showing how to do path based routing using nginx as reverse proxy  

* Using 3 nginx containers as targets, each loading some static content  
* http only, no ssl  
* path / routes to default-target container  
* path /2 routes to target2 container  
* path /3 routes to target3 container  

## pre-requisites

Git and Docker installed and working

## get started

1. Clone repo
2. Bring stack up

        docker-compose up - d

3. Test endpoints / targets

        curl localhost
        curl localhost/2
        curl localhost/3

4. Check individual container logs

        docker-compose logs default-target
        docker-compose logs target2
        docker-compose logs target3
        docker-compose logs proxy

5. shutdown

        docker-compose down 