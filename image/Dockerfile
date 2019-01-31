FROM phusion/baseimage

RUN apt-get update && \
	apt-get install -y git curl && \
	rm -rf /var/lib/apt/lists/*

RUN curl -sS https://get.symfony.com/cli/installer | bash && \
	mv "/root/.symfony/bin/symfony" "/usr/local/bin/symfony" && \
	chmod +x "/usr/local/bin/symfony"

ENTRYPOINT ["symfony"]
