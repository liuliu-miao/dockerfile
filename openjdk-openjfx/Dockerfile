FROM ubuntu:16.04

ENV TZ=Asia/Shanghai

RUN apt update \
    && apt install openjdk-8-jdk openjfx -y \ 
    && ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo $TZ > /etc/timezone \
    && apt install tzdata -y  \
    && dpkg-reconfigure --frontend noninteractive tzdata \
    && apt install language-pack-zh-hans -y \
    && locale-gen zh_CN.UTF-8 && locale \
    && echo "export LC_ALL='zh_CN.UTF-8'" >> /etc/bash.bashrc  && source /etc/bash.bashrc 


CMD ["/bin/bash"]
