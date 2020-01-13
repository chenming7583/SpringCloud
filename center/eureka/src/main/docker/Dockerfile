#基础镜像来源
FROM registry.test.com/common/jdk1.8.0_111

#方式一
#同步容器和宿主机时间
#RUN /bin/cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone
ADD /eureka-server-0.0.1-SNAPSHOT.jar /
ADD ./run.sh /
RUN chmod u+x /*.sh
ENV JAVA_OPTS=""
ENV SERVICE_HOST="eureka-server"
ENV CONFIG_HOST="eureka-service"
ENV CONFIG_PROFILE="default"
ENV SERVER_PORT="8080"
ENTRYPOINT [ "bash", "-c", "/run.sh" ]
