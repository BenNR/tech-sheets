 docker logs -f --tail 10 vllmn

 docker login -u b.naujoks.roldan@googlemail.com -p 385(yipPLhP%5uA

docker build --platform=linux/amd64 -t nginx-health-check .

docker tag nginx-health-check bennr/nginx-health-check:0.0.1

docker push bennr/nginx-health-check:0.0.1

docker run -d --name nginx-health-check bennr/nginx-health-check:0.0.1


docker run -dit --name nginx-health -p 8081:80 bennr/nginx-health-check:0.0.1
