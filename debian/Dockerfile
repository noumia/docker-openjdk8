FROM buildpack-deps:stretch-curl

RUN set -x  \
 && cd /opt \
 && curl -fsSLO "https://github.com/bell-sw/Liberica/releases/download/8u192/bellsoft-jdk1.8.0-linux-amd64.tar.gz" \
 && tar xzf bellsoft-jdk1.8.0-linux-amd64.tar.gz \
 && rm -f bellsoft-jdk1.8.0-linux-amd64.tar.gz

ENV JAVA_HOME=/opt/jdk-1.8.0 PATH=/opt/jdk-1.8.0/bin:${PATH}

