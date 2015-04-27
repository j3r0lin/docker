FROM ubuntu:trusty
MAINTAINER jerolin <j3r0lin@gmail.com>

ENV DEBIAN_FRONTEND noninteractive
WORKDIR /opt/
RUN apt-get update && \
	apt-get -y install software-properties-common python-software-properties && \
	apt-add-repository ppa:mosquitto-dev/mosquitto-ppa && \
	apt-get update && \
    apt-get -y install mosquitto && \
	apt-get clean && \
	rm -rf /var/lib/apt/lists/*

EXPOSE 1883
CMD ["mosquitto"]
