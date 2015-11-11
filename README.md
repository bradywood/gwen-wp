#Installing wordpress specific to gwen
thanks to http://jgreat.me/

docker run -d \
--volume=/data/mysql:/var/lib/mysql \
--restart=always \
--publish=172.17.42.1:3306:3306 \
--env='MYSQL_USER=wp-user' \
--env='MYSQL_PASSWORD=myAwesomePassword' \
--env='MYSQL_DATABASE=wordpress' \
--env='MYSQL_ROOT_PASSWORD=myAwesomeRootPassword' \
--name=mysql \
mysql:5.6

