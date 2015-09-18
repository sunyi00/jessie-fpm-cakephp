FROM occitech/cakephp:5.6-fpm

RUN apt-get update \
    && apt-get install -y \
        locales \
        vim \
        lsof \
        curl \
        ca-certificates \
        nginx \
        python \
        python-pip \
    && echo "zh_CN.UTF-8 UTF-8" > /etc/locale.gen \
    && locale-gen \
    && apt-get -y autoclean \
    && apt-get -y clean \
    && rm -rf /var/cache/apt/archives/* \
    && rm -rf /var/lib/apt/lists/* \
    && rm -f /etc/localtime \
    && ln -s /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && pip install supervisor

ENV LANG zh_CN.UTF-8
ENV LC_ALL zh_CN.UTF-8
