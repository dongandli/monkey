FROM registry.cn-zhangjiakou.aliyuncs.com/ylns/openjdk8:1.0.0

RUN mkdir -p /monkey-xxl-job-admin

WORKDIR /monkey-xxl-job-admin

ARG JAR_FILE=target/monkey-xxl-job-admin.jar

COPY ${JAR_FILE} app.jar

EXPOSE 5004

ENV TZ=Asia/Shanghai JAVA_OPTS="-Xms128m -Xmx256m -Djava.security.egd=file:/dev/./urandom"

CMD sleep 60; java -jar app.jar $JAVA_OPTS
