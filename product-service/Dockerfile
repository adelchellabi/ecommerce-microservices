FROM maven:3.9.6-eclipse-temurin-21 AS builder

WORKDIR /app

RUN useradd -m appuser
USER appuser

ENV MAVEN_CONFIG=/app/.m2

COPY --chown=appuser:appuser .mvn/ .mvn
COPY --chown=appuser:appuser mvnw pom.xml ./
COPY --chown=appuser:appuser src ./src

RUN chmod +x mvnw

CMD ["./mvnw", "spring-boot:run"]