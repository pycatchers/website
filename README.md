## How to Run
Clone this repository - {repo_url}

Make sure you are using JDK 1.8 and Maven 4.x

### Build the Maven project and installs the project files
```
mvn install or mvnw clean install
```

### Run with below VM options in run config
```
mvn spring-boot:run -Dspring.profiles.active=service,cloud
-Dcom.esrx.app.monitoring.environment=local
-Dcom.esrx.app.monitoring.region=dev
-Dcom.esrx.app.monitoring.organization=RPT
-Dcom.esrx.app.monitoring.version=1
-Dnewrelic.config.app_name={appname}
-Dcom.esrx.app.monitoring.instanceId=1
```

Once the application runs you should see something like this
```
2023-10-31 23:26:48.883  INFO 125659 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat initialized with port(s): 8080 (http)
2023-10-31 23:26:48.891  INFO 125659 --- [           main] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
2023-10-31 23:26:48.891  INFO 125659 --- [           main] org.apache.catalina.core.StandardEngine  : Starting Servlet engine: [Apache Tomcat/9.0.82]
2023-10-31 23:26:48.967  INFO 125659 --- [           main] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring embedded WebApplicationContext
2023-10-31 23:26:48.967  INFO 125659 --- [           main] w.s.c.ServletWebServerApplicationContext : Root WebApplicationContext: initialization completed in 636 ms
```
