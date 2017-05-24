FROM debian:wheezy-slim

RUN apt-get update && apt-get install -y --no-install-recommends \
		ca-certificates \
		curl \
		wget \
	&& rm -rf /var/lib/apt/lists/* \
	&& echo "alias ll='ls -l'" >> /etc/bash.bashrc