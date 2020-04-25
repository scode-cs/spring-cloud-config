# spring-cloud-config
```bash
Spring Cloud Config Server. Reads the configurations from GitHub
```

## Quering the Configuration
```bash
/{application}/{profile}[/{label}]
/{application}-{profile}.yml
/{label}/{application}-{profile}.yml
/{application}-{profile}.properties
/{label}/{application}-{profile}.properties
```
## Enable Spring Cloud Config Server
```java
@SpringBootApplication
@EnableConfigServer
public class Application {
	public static void main(String[] args) {
		SpringApplication.run(CloudConfigServerApplication.class, args);
	}
}

```
## Cloud Config Server Configuration - application.yml
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
