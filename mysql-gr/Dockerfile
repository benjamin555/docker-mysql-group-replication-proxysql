FROM perconalab/mysql-group-replication-base

VOLUME /var/lib/mysql
EXPOSE 3306

COPY mgr-entry.sh /entrypoint.sh

RUN chmod +x entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]