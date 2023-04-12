
#스프링


## gradlew
---
>gradlew
```
implementation 'org.springframework.boot:spring-boot-starter-web'
implementation 'org.mybatis.spring.boot:mybatis-spring-boot-starter:2.3.0'
compileOnly 'org.projectlombok:lombok'
developmentOnly 'org.springframework.boot:spring-boot-devtools'
runtimeOnly 'com.mysql:mysql-connector-j'
annotationProcessor 'org.projectlombok:lombok'
providedRuntime 'org.springframework.boot:spring-boot-starter-tomcat'
testImplementation 'org.springframework.boot:spring-boot-starter-test'
implementation group: 'jstl', name: 'jstl', version: '1.2'
implementation group: 'org.apache.tomcat.embed', name: 'tomcat-embed-jasper', version: '9.0.58'
implementation group: 'com.servlets', name: 'cos', version: '09May2002'

```


> property
```
spring.main.banner-mode=off
server.port=8899
server.servlet.context-path=/boot
spring.datasource.username=root
spring.datasource.password=mysql
spring.datasource.url=jdbc:mysql:localhost://3306/thisisjava
spring.datasource.dbcp2.driver-class-name=com.mysql.cj.jdbc.Driver
spring.mvc.view.prefix=/WEB-INF/view/
spring.mvc.view.suffix=.jsp
spring.servlet.multipart.enabled=false

```


## Maven
---
```
<dependency>
<groupId>javax.servlet</groupId>
<artifactId>jstl</artifactId>
</dependency>
<dependency>
<groupId>org.apache.tomcat.embed</groupId>
<artifactId>tomcat-embed-jasper</artifactId>
</dependency>

spring.mvc.view.prefix=/WEB-INF/board/
spring.mvc.view.suffix=.jsp

```