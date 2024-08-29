
FROM eclipse-temurin:21-jre-alpine
LABEL maintainer="jason <a01071865081@gmail.com>"
LABEL version="1.1"
COPY 06_Subject-0.0.1-SNAPSHOT.jar /root
# build 명령어 실행 시 Dockerfile 내부로 값을 전달받을 수 있는 변수 선언
ARG PROFILE=dev
ARG PORT=8089
ENV TZ=Asia/Seoul
# ARG 이미지 빌드 시에만 적용되고 실제 컨테이너에서는 사용할 수 없기 때문에 입력받은 ENV를 통해서 전달한다.
ENV PROFILE=${PROFILE}
# PORT 변수의 값으로 컨테이너에서 사용할 포트를 지정한다.
EXPOSE ${PORT}
WORKDIR /root
CMD [ "java","-jar","06_Subject-0.0.1-SNAPSHOT.jar", "--spring.profiles.active=${PROFILE}" ]

