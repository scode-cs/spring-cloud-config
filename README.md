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
## Usage
```java
@EnableConfigServer
public class Application {

	public static void main(String[] args) {
		SpringApplication.run(CloudConfigServerApplication.class, args);
	}

}

```
