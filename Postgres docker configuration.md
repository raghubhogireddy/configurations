# Configuring Postgres in SpringBoot Application


- Below dependencies have to be added to the `pom.xml`
  
    ```xml
            <dependency>
		    <groupId>org.springframework.boot</groupId>
		    <artifactId>spring-boot-starter-data-jpa</artifactId>
		</dependency>
		<dependency>
		    <groupId>org.postgresql</groupId>
		    <artifactId>postgresql</artifactId>
		</dependency>
    ```
- Below are the steps to execute/spin up the postgres db as a docker container
``` docker
  docker run -it -p 5432:5432 -e POSTGRES_PASSSWORD=<password> POSTGRES_DB=local postgres
  docker exec -it <container_name> /bin/bash
  psql -d local postgres
  local=# select * from db.table;
 ```
- Spring Boot Applicaton's `application.properties` has to be updated to add the datasource url, username, password

``` properties
spring.database.jpa=postgresql
spring.datasource.url=jdbc:postgresql://<ip>:<port>/<db>?currentSchema=<schema>
spring.datasource.username=<username>
spring.datasource.password=<password>
```
