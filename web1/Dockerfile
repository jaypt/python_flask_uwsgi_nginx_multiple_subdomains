FROM python:2.7

MAINTAINER jaypt

RUN apt-get -yqq update

COPY requirements.txt .
RUN pip install -r requirements.txt



RUN apt-get -yqq install vim


#copy conf for uwsgi
COPY emperor.ini /etc/uwsgi/
RUN mkdir /etc/uwsgi/vassals sudo
COPY uwsgi.ini /etc/uwsgi/vassals

EXPOSE 8000

COPY ./app /app
WORKDIR /app


