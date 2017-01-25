FROM  tomcat:jre8-alpine

COPY /therest.war /usr/local/tomcat/webapps/therest.war
COPY /therest.xml /usr/local/tomcat/conf/Catalina/localhost/therest.xml 
COPY /systemone.jar /usr/local/tomcat/lib/systemone.jar

#build with:
#maven build

#start on development with:
#docker run --net=cora--volumes-from gatekeeper:ro -p 8080:8080 --name therest --link gatekeeper:gatekeeper -d  therest


#start on build server with:
#docker run --net=cora-test --volumes-from gatekeeper-test --name therest-test --link gatekeeper-test:gatekeeper -d  therest

#start on external with:
#docker run --network=cora -p 8280:8080 --name therest --link gatekeeper:gatekeeper -d  therest

#reomove unused volumes with:
#docker volume rm $(docker volume ls -q)