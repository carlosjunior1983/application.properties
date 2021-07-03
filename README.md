# application.properties

Dicas de configurações rápidas para Spring Boot Java, para vários bancos de dados.

`h2` `PostgreSql`

`Jpa`



#Spring Boot server configuration
server.port=8000
server.servlet.context-path=/
 
# Database configuration
# ----------------------

#h2
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=root
spring.datasource.password=root

spring.jpa.database.platform=org.hibernate.dialect.H2Dialect

spring.h2.console.enabled=true
spring.h2.console.path=/h2-console


#PostgreSql-Local
spring.datasource.url=jdbc:postgresql://localhost:5432/db_jdev
spring.datasource.username=postgres
spring.datasource.password=1234567


#PostgreSQL Heroku configuration 

spring.datasource.driverClassName=org.postgresql.Driver
spring.jpa.database-platform=org.hibernate.dialect.PostgreSQLDialect
spring.jpa.hibernate.ddl-auto=update

### Environment-dev
spring.datasource.url=jdbc:postgresql://host:port/database
spring.datasource.username=user
spring.datasource.password=pass

### Environment-prod
spring.datasource.url=jdbc:postgresql:${DATABASE_URL}


#MySql - INI ------------------------------------------------------------------------------
spring.datasource.url=jdbc:mysql://localhost:3306/sms?useSSL=false&serverTimezone=UTC&useLegacyDatetimeCode=false
spring.datasource.username=root
spring.datasource.password=root

#Hibernate
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5InnoDBDialect

#Hibernate auto dll
spring.jpa.hibernate.ddl-auto=update

logging.level.org.hibernate.SQL=debug
#MySql - End ------------------------------------------------------------------------------







#Jpa Config
spring.jpa.properties.hibernate.jdbc.lob.non_contextual_creation=true
spring.jpa.hibernate.ddl-auto=update
