FROM tomcat:9.0.93-jre11-temurin
WORKDIR /usr/local/tomcat/webapps
RUN mkdir ./ROOT
COPY index.jsp ./ROOT
ENV TZ=Asia/Seoul
EXPOSE 8080
CMD [ "catalina.sh", "run" ]
