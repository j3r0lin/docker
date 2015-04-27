FROM tutum/apache-php
MAINTAINER jerolin <j3r0lin@gmail.com>

ENV DEBIAN_FRONTEND noninteractive
ADD http://www.hivemq.com/downloads/releases/latest /opt/hivemq.zip
WORKDIR /opt/
RUN apt-get update && \
	apt-get -y install \
		openjdk-7-jre \
		vim \
		unzip && \
	apt-get clean && \
	rm -rf /var/lib/apt/lists/* && \
	unzip hivemq.zip && \
	useradd -d /opt/hivemq hivemq && \
	chown -R hivemq:hivemq /opt/hivemq && \
    chmod a+x /opt/hivemq/bin/run.sh


EXPOSE 1883
CMD ["/opt/hivemq/bin/run.sh"]
