FROM openjdk:11.0.10-jre-buster
MAINTAINER MrBird 852252810@qq.com

COPY ./target/febs-gateway-2.2-RELEASE.jar /febs/febs-gateway-2.2-RELEASE.jar
ADD agent/ /agent

ENTRYPOINT ["java", "-javaagent:/agent/skywalking-agent.jar", "-Dskywalking.agent.service_name=febs-gateway", "-Dskywalking.collector.backend_service=skywalkingIp:11800", "-jar", "/febs/febs-gateway-2.2-RELEASE.jar"]