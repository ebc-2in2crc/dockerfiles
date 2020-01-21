FROM mysql:5.6

RUN apt update && \
		apt install wget -y && \
		apt install lsb-release -y && \
		wget https://repo.percona.com/apt/percona-release_latest.$(lsb_release -sc)_all.deb && \
		dpkg -i percona-release_latest.$(lsb_release -sc)_all.deb && \
		apt update && \
		apt install percona-xtrabackup-24 -y

ENTRYPOINT ["docker-entrypoint.sh"]

EXPOSE 3306
CMD ["mysqld"]
