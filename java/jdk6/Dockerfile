FROM centos:7

ENV JAVA_HOME=/usr/java/jdk1.6.0_45
ENV PATH=$PATH:$JAVA_HOME/bin

RUN \
  cd /tmp && \
  curl -O "http://mirrors.linuxeye.com/jdk/jdk-6u45-linux-x64.bin" && \
  sh jdk-*.bin && \
  rm jdk-*.bin && \
  mkdir -p /usr/java && \
  mv jdk1.* /usr/java && \
  rm -rf $JAVA_HOME/src.zip && \
  java -version
  
