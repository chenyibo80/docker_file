FROM chenyibo/openjdk:8

ENV TC_MAJOR 8 
ENV TC_MINOR 8.0.44 
ENV CATALINA_HOME /usr/local/tomcat-$TC_MINOR 
ENV CATALINA_OPTS -Djava.security.egd=file:/dev/urandom
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

EXPOSE 8080
CMD ["bin/catalina.sh", "run"]