FROM openjdk:11

WORKDIR /app

RUN curl https://start.spring.io/starter.tgz \
    -d dependencies=devtools,lombok,web \
    -d type=gradle-project \
    -d bootVersion=2.2.4.RELEASE \
    -d javaVersion=11 \
    | tar -xzvf -

# ./gradlew build --continuous
# for hot reload
CMD ["./gradlew", "build", "--continuous", "-x", "test"]
