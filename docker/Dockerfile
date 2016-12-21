FROM  tomcat:jre8-alpine

COPY /storagefiles /mnt/data/basicstorage

COPY /therest.war /usr/local/tomcat/webapps/therest.war
COPY /therest.xml /usr/local/tomcat/conf/Catalina/localhost/therest.xml 

#start with  docker run   -p 8081:8080 --name therest -d  therest
#docker run   -p 8081:8080 --name therest --link gatekeeper:gatekeeper -d  therest