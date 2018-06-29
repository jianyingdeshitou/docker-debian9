FROM debian9

MAINTAINER 坚硬的石头 <do_nb@outlook.com>

# 更新安装 nginx
RUN apt-get update && apt-get install man git git-flow vim -y && \
        rm -rf /var/lib/apt/lists/*

VOLUME /app
VOLUME /root

WORKDIR /app
