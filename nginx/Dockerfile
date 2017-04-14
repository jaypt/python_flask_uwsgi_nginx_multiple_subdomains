FROM nginx

MAINTAINER jaypt


# forward request and error logs to docker log collector
RUN ln -sf /dev/stdout /var/log/nginx/access.log \
    && ln -sf /dev/stderr /var/log/nginx/error.log

RUN apt-get -yqq update
RUN apt-get -yqq install curl

#copy conf for nginx
COPY nginx.conf /etc/nginx/conf.d/

#RUN rm /etc/nginx/sites-enabled/default
RUN rm /etc/nginx/conf.d/default.conf

EXPOSE 80




