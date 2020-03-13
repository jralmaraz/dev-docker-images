FROM image-registry.openshift-image-registry.svc:5000/openshift/ubi:latest

MAINTAINER Jose Almaraz

RUN mkdir /opt/tomcat/

WORKDIR /opt/tomcat
RUN curl -O https://apache.mirror.digitalpacific.com.au/tomcat/tomcat-8/v8.5.51/bin/apache-tomcat-8.5.51.tar.gz
RUN tar xvfz apache*.tar.gz
RUN mv apache-tomcat-8.5.51/* /opt/tomcat/.
RUN yum -y install java
RUN java -version

#WORKDIR /opt/tomcat/webapps
#Download a war sample app to deploy
#RUN curl -O -L 

EXPOSE 8080

CMD ["/opt/tomcat/bin/catalina.sh", "run"]