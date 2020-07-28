FROM centos:7

RUN yum install -y epel-release && \
		yum install -y banner

COPY docker-entrypoint.sh /usr/local/bin

ENTRYPOINT ["docker-entrypoint.sh"]
