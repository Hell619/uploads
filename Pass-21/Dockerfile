FROM upload-labs

MAINTAINER c0ny1 <root@gv7.me>
ENV LC_ALL C.UTF-8
ENV TZ=Asia/Shanghai

COPY . /tmp/


# install upload-labs
RUN cd /tmp/ &&\
git clone https://github.com/Hell619/uploads.git &&\
    mkdir /var/www/html/upload &&\
    mv /tmp/uploads/Pass-21/* /var/www/html/ &&\
    chown www-data:www-data -R /var/www/html/ &&\
    rm -rf /tmp/*
EXPOSE 80
