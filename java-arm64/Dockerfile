FROM ericvh/arm64-ubuntu 

ENV JAVA_VERSION_MAJOR 8
ENV JAVA_VERSION_UPDATE 111
ENV JAVA_VERSION_BUILD b14

VOLUME /workdir

RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install curl tar

# Install Java
RUN curl -jL -H "Cookie: oraclelicense=accept-securebackup-cookie" http://download.oracle.com/otn-pub/java/jdk/${JAVA_VERSION_MAJOR}u${JAVA_VERSION_UPDATE}-${JAVA_VERSION_BUILD}/jdk-${JAVA_VERSION_MAJOR}u${JAVA_VERSION_UPDATE}-linux-arm64-vfp-hflt.tar.gz > jdk.tar.gz
RUN tar xvfz jdk.tar.gz

ENV JAVA_HOME /jdk1.${JAVA_VERSION_MAJOR}.0_${JAVA_VERSION_UPDATE}
ENV PATH $PATH:$JAVA_HOME/bin
WORKDIR /workdir

