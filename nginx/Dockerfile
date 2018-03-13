FROM library/ubuntu

WORKDIR /root
RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y git build-essential libjansson-dev automake libtool pkg-config \
    libpcre3-dev libcurl4-openssl-dev wget libssl-dev
RUN wget https://github.com/ScaleFT/libxjwt/releases/download/v1.0.2/libxjwt-1.0.2.tar.gz && \
    tar xvf libxjwt-1.0.2.tar.gz && \
    cd libxjwt-1.0.2 && ./configure && make && make install && cd .. && \
    rm -rf libxjwt-1.0.2 libxjwt-1.0.2.tar.gz
RUN git clone https://github.com/ScaleFT/nginx_auth_accessfabric.git && \
    wget http://nginx.org/download/nginx-1.13.7.tar.gz && \
    tar -xvzf nginx-1.13.7.tar.gz && \
    cd nginx-1.13.7 && ./configure --add-dynamic-module=../nginx_auth_accessfabric && make && make install && \
    cd .. && rm -rf nginx*

RUN mkdir /var/log/nginx
RUN ln -sf /dev/stdout /var/log/nginx/access.log \
    && ln -sf /dev/stderr /var/log/nginx/error.log
RUN ldconfig

COPY nginx.conf /etc/nginx/nginx.conf

EXPOSE 80

CMD ["/usr/local/nginx/sbin/nginx", "-g", "daemon off;", "-c", "/etc/nginx/nginx.conf"]
