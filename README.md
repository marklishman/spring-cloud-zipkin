# Zipkin Server

## Add the Dependency 

Include the zipkin dependencies.

```xml
<dependency>
    <groupId>io.zipkin.java</groupId>
    <artifactId>zipkin-server</artifactId>
    <version>2.11.8</version>
</dependency>
<dependency>
    <groupId>io.zipkin.java</groupId>
    <artifactId>zipkin-autoconfigure-ui</artifactId>
    <version>2.11.8</version>
    <scope>runtime</scope>
</dependency>
```

## Enable the zipkin Server

Add the `@EnableZipkinServer` annotation to the Spring Boot application.

```java
@SpringBootApplication
@EnableZipkinServer
public class ZipkinApplication {

    public static void main(String[] args) {
        SpringApplication.run(ZipkinApplication.class, args);
    }
}
```

## Configure

Set the port in the `application.yml` file.

```yaml
server:
  port: 9411
```

## User Interface

Go to this URL to explore the Zipkin user interface

    http://localhost:9411/zipkin
    
Output

![Zipkin](screenshot/zipkin.png?raw=true "Zipkin Output")
