FROM tomcat:latest
LABEL "maintainer"="vamsi krishna"
WORKDIR /usr/local/tomcat/webapps
COPY *.war My-app.war
WORKDIR /usr/local/tomcat/bin
CMD["catalia.sh","start"]
