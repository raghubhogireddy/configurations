# Configuring H2 InMemory Database for SpringBoot Applications

- Below dependencies have to be added to the `pom.xml`
    ```xml
            <dependency>
		    <groupId>org.springframework.boot</groupId>
		    <artifactId>spring-boot-starter-data-jpa</artifactId>
		</dependency>
		<dependency>
		    <groupId>com.h2database</groupId>
		    <artifactId>h2</artifactId>
		</dependency>
    ```
- The `schema.sql` & `data.sql` to be placed in the resources folder so that during app initialization H2 picks the schema and load the data.  