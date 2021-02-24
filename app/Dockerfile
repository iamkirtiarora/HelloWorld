# Linux image we are going to use
FROM alpine
WORKDIR /root/hello-world
COPY HelloWorld.java /root/hello-world

#Install JDK
RUN apk add openjdk8
ENV JAVA_HOME /usr/lib/jvm/java-1.8-openjdk
ENV PATH $PATH:$JAVA_HOME/bin

#Compile our Helloworld
RUN javac HelloWorld.java
ENV LISTEN_PORT=9171
EXPOSE 9171

ENTRYPOINT java HelloWorld
