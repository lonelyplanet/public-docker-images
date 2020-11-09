FROM lonelyplanet/java-8

ENV SCALA_VERSION=2.11.8 \
    SBT_VERSION=0.13.11


# INSTALL Scala and SBT
WORKDIR /tmp
RUN wget -nv http://downloads.typesafe.com/scala/$SCALA_VERSION/scala-$SCALA_VERSION.deb && \
    dpkg -i scala-$SCALA_VERSION.deb && \
    wget -nv http://dl.bintray.com/sbt/debian/sbt-$SBT_VERSION.deb && \
    dpkg -i sbt-$SBT_VERSION.deb && \
    rm -f scala-* && \
    rm -f sbt-* && \
    sbt exit
