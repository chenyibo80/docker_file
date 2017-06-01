FROM chenyibo/openjdk:6

ENV TC_MAJOR 6 
ENV TC_MINOR 6.0.53 
ENV CATALINA_HOME /usr/local/tomcat-$TC_MINOR 
ENV TOMCAT_TGZ_URL https://mirrors.aliyun.com/apache/tomcat/tomcat-$TC_MAJOR/v$TC_MINOR/bin/apache-tomcat-$TC_MINOR.tar.gz

RUN \
  cd /tmp && \
  curl -O "$TOMCAT_TGZ_URL" && \
  tar -xvf apache-tomcat-$TC_MINOR.tar.gz && \
  rm apache-tomcat-$TC_MINOR.tar.gz && \
  mv apache-tomcat-$TC_MINOR $CATALINA_HOME && \
  chmod +x $CATALINA_HOME/bin/*.sh && \
  rm $CATALINA_HOME/bin/*.bat

WORKDIR $CATALINA_HOME

VOLUME ["/usr/local/tomcat-6.0.53/webapps", "/usr/local/tomcat-6.0.53/logs"]

EXPOSE 8080
CMD ["bin/catalina.sh", "run"]