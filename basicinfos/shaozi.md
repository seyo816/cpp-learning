docker pull seyo816/centos:7
docker run -it --name shaozi -v /data/docker/shaozi:/data seyo816/shaozi /bin/bash
docker run -it --rm seyo816/centos:7 /bin/bash
docker run -it --rm seyo816/shaozi /bin/bash
docker run -it -p 81:80 --rm seyo816/shaozi_basic /bin/bash

docker commit shaozi shaozi_test:1.0

docker commit shaozi_basic_data shaozi_basic_data:1.0


/usr/local/nginx/sbin/nginx -s reload
docker exec -it shaozi_basic_data /bin/bash


# 启动mongo外网服务
rinetd
