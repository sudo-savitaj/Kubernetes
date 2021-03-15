FROM openjdk:8-alpine

RUN apk add bash
RUN apk add nodejs

ENV SPARK_VERSION 2.4.7
ENV HADOOP_VERSION 2.7
ENV SPARK_PACKAGE spark-${SPARK_VERSION}-bin-hadoop${HADOOP_VERSION}
ENV SPARK_HOME /usr/spark-${SPARK_VERSION}

RUN wget \
  "https://downloads.apache.org/spark/spark-${SPARK_VERSION}/${SPARK_PACKAGE}.tgz" \
  && tar xvf  ${SPARK_PACKAGE}.tgz  \
&& mv $SPARK_PACKAGE $SPARK_HOME \
&& chown -R root:root $SPARK_HOME

ENV PATH $PATH:${SPARK_HOME}/bin

