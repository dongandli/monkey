FROM registry.cn-zhangjiakou.aliyuncs.com/ylns/openjdk8:1.0.0

RUN mkdir -p /monkey-monitor

WORKDIR /monkey-monitor

ARG JAR_FILE=target/monkey-monitor.jar

COPY ${JAR_FILE} app.jar

EXPOSE 5001

ENV TZ=Asia/Shanghai JAVA_OPTS="-Xms128m -Xmx256m -Djava.security.egd=file:/dev/./urandom"

CMD sleep 60; java -jar app.jar $JAVA_OPTS
