FROM maven:3-jdk-11
COPY . /app
WORKDIR /app
# -------------
ENV JDBC_URL=localhost
ENV JDBC_PORT=6546
ENV JDBC_DB=jcorporation
ENV JDBC_USER=jcorporation
ENV JDBC_PASSWORD=jcorporation
# -------------

RUN mvn package -DskipTests -q
ENTRYPOINT [ "java", "-jar", "/app/target/api-0.0.1-SNAPSHOT.jar" ]
