FROM registry.cn-zhangjiakou.aliyuncs.com/ylns/openjdk8:1.0.0

RUN mkdir -p /monkey-gateway

WORKDIR /monkey-gateway

ARG JAR_FILE=target/monkey-gateway.jar

COPY ${JAR_FILE} app.jar

EXPOSE 9999

ENV TZ=Asia/Shanghai JAVA_OPTS="-Xms128m -Xmx256m -Djava.security.egd=file:/dev/./urandom"

CMD sleep 60; java -jar app.jar $JAVA_OPTS
