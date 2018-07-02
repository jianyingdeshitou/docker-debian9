FROM debian9

MAINTAINER 坚硬的石头 <do_nb@outlook.com>

# 更新安装 git
RUN apt-get update && \
    apt-get install -y man git git-flow vim ctags \
        dos2unix && \
    rm -rf /var/lib/apt/lists/*

VOLUME /app
VOLUME /root

WORKDIR /app
