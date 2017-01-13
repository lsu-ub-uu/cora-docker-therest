FROM  tomcat:jre8-alpine

COPY /storagefiles /mnt/data/basicstorage

COPY /therest.war /usr/local/tomcat/webapps/therest.war
COPY /therest.xml /usr/local/tomcat/conf/Catalina/localhost/therest.xml 
COPY /systemone.jar /usr/local/tomcat/lib/systemone.jar

#build with:
#maven build

#start on build server with:
#docker run --network=cora-test --name therest-test  -p 8180:8080 --link gatekeeper-test:gatekeeper -d  therest

#start on external with:
#docker run --network=cora -p 8280:8080 --name therest --link gatekeeper:gatekeeper -d  therest
