# Spring Cloud Config Server
```bash
Spring Cloud Config Server provides an HTTP resource-based API for external configuration
(name-value pairs or equivalent YAML content). 
```

### Dependency
```xml
<dependency>
	<groupId>org.springframework.cloud</groupId>
	<artifactId>spring-cloud-config-server</artifactId>
</dependency>
```
### Enable Spring Cloud Config Server
```java
@SpringBootApplication
@EnableConfigServer
public class Application {
	public static void main(String[] args) {
		SpringApplication.run(CloudConfigServerApplication.class, args);
	}
}

```
### Cloud Config Server Configuration - application.yml
```yml
#DefaultPort: 8888
server:
  port: 8888

spring:
  application:
    name: config-server

  cloud:
    config:
      server:
        git:
          clone-on-start: true
          uri: https://github.com/scode-cs/spring-cloud-config-data.git
```
### Quering the Configuration from Cloud-Config Server
```bash
/{application}/{profile}[/{label}]
/{application}-{profile}.yml
/{label}/{application}-{profile}.yml
/{application}-{profile}.properties
/{label}/{application}-{profile}.properties
```
