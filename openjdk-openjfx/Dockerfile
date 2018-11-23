FROM ubuntu:16.04

RUN apt update \
    && apt install  openjdk-8-jre openjfx -y \ 
    && dpkg-reconfigure tzdata \
    && cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime 

CMD ["/bin/bash"]
