# Use official Tomcat base image
FROM tomcat:9.0

# Remove default webapps you don't need (optional)
RUN rm -rf /usr/local/tomcat/webapps/*

RUN echo "<role rolename="manager-gui"/>" >> /usr/local/tomcat/conf/tomcat-users.xml

RUN echo "<user username="tomcat" password="s3cret" roles="manager-gui"/>" >> /usr/local/tomcat/conf/tomcat-users.xml

RUN cat /usr/local/tomcat/conf/tomcat-users.xml

# (Optional) Restore default webapps including manager and host-manager
RUN mkdir -p /usr/local/tomcat/webapps \
    && cp -r /usr/local/tomcat/webapps.dist/* /usr/local/tomcat/webapps/

EXPOSE 8080
CMD ["catalina.sh", "run"]

