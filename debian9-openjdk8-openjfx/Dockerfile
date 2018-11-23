FROM debian:9

ENV TZ=Asia/Shanghai

RUN apt update \
    && apt install openjdk-8-jdk openjfx locales -y \ 
    && ln -sf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone \
    && locale-gen --purge en_US.UTF-8 zh_CN.UTF-8 \ 
    && localedef -i en_US -c -f UTF-8 -A /usr/share/locale/locale.alias en_US.UTF-8 \
    &&  echo -e 'LANG="en_US.UTF-8"' > /etc/default/locale &&  echo -e 'LANGUAGE="en_US:en"' >> /etc/default/locale  \

CMD ["bash"]
