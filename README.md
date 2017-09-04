This repo demonstrates how to setup a mysql master slave using docker-compose and the official mysql docker image.

For detailed article refere to http://mysqlrelease.com/2016/08/mysql-group-replication-docker-images/


docker network create cluster1

docker run -d --net=cluster1 --name=node1  dockermysqlgroupreplicationproxysql_mysqlmaster --group_replication_bootstrap_group=ON

docker run -d --net=cluster1 --name=node2  dockermysqlgroupreplicationproxysql_mysqlslave --group_replication_group_seeds='node1:6606'

