FROM debian9

MAINTAINER 坚硬的石头 <do_nb@outlook.com>

RUN apt-get update \
    && apt-get install -y vim vim-nox ctags\
    && rm -rf /var/lib/apt/lists/*

#RUN curl http://j.mp/spf13-vim3 -L -o - | sh
RUN curl https://raw.githubusercontent.com/spf13/spf13-vim/3.0/bootstrap.sh -L -o - | sh

COPY files/vimrc.bundles.local /root/.vimrc.bundles.local
RUN vim +BundleInstall! +BundleClean +qall

COPY files/vimrc.local /root/.vimrc.local

VOLUME /app
WORKDIR /app
