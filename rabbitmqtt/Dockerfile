FROM tutum/rabbitmq
MAINTAINER jerolin <j3r0lin@gmail.com>

ENV DEBIAN_FRONTEND noninteractive
ENV RABBITMQ_PASS admin

RUN rabbitmq-plugins enable rabbitmq_mqtt --offline

EXPOSE 1883
