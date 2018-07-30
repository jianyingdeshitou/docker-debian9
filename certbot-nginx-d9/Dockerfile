FROM nginx-d9

MAINTAINER 坚硬的石头 <do_nb@outlook.com>

RUN echo "deb http://ftp.cn.debian.org/debian stretch-backports main" > /etc/apt/sources.list.d/certbot.list
# 更新安装 certbot
RUN apt-get update && \
    apt-get install -y python-certbot-nginx -t stretch-backports && \
    rm -rf /var/lib/apt/lists/*

# forward request and error logs to docker log collector
# RUN ln -sf /dev/stdout /var/log/nginx/access.log \
#     && ln -sf /dev/stderr /var/log/nginx/error.log

# EXPOSE 90 443

# CMD ["nginx", "-g", "daemon off;"]

