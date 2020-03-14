--criando o site 1:

docker container run -p 8080:80 -v ${pwd}:/usr/share/nginx/html --name site1 nginx

--criando o site2:

docker container run -p 8081:80 -v ${pwd}:/usr/share/nginx/html --name site2 nginx

--criando o load balancer:

docker container run  --rm -p 8082:80 -v ${pwd}/loadbalancer:/etc/nginx/conf.d --name loadbalancer nginx
