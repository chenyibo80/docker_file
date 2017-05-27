FROM chenyibo/openjdk:6

ENV MAJOR_VERSION 8 
ENV MINOR_VERSION 8.0.44 
ENV CATALINA_HOME /usr/local/tomcat-$MINOR_VERSION 
ENV TOMCAT_TGZ_URL https://mirrors.aliyun.com/apache/tomcat/tomcat-$MAJOR_VERSION/v$MINOR_VERSION/bin/apache-tomcat-$MINOR_VERSION.tar.gz

RUN \
  cd /tmp && \
  curl -O "$TOMCAT_TGZ_URL" && \
  tar -xvf apache-tomcat-$MINOR_VERSION.tar.gz && \
  rm apache-tomcat-$MINOR_VERSION.tar.gz && \
  mv apache-tomcat-$MINOR_VERSION $CATALINA_HOME && \
  chmod +x $CATALINA_HOME/bin/*.sh && \
  rm $CATALINA_HOME/bin/*.bat

WORKDIR $CATALINA_HOME

EXPOSE 8080
CMD ["bin/catalina.sh", "run"]