FROM  tomcat:9.0-jre11-slim

COPY /storagefiles /mnt/data/basicstorage

COPY /therest*.war /usr/local/tomcat/webapps/therest.war
COPY /therest.xml /usr/local/tomcat/conf/Catalina/localhost/therest.xml 

COPY /*.jar /usr/local/tomcat/lib/
COPY /*.properties /usr/local/tomcat/lib/

#build with:
#maven build

#start on development with:
#docker run --net=cora--volumes-from gatekeeper -p 8080:8080 --name therest --link gatekeeper:gatekeeper --link solr:solr -d  therest


#start on build server with:
#docker run --net=cora-test --volumes-from gatekeeper-test --name therest-test --link gatekeeper-test:gatekeeper --link solr-test:solr -d  therest

#start on external with:
#docker run --network=cora -p 8280:8080 --name therest --link gatekeeper:gatekeeper --link solr:solr -d  therest

#reomove unused volumes with:
#docker volume rm $(docker volume ls -q)