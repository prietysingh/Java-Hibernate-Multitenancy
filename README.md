# README #

Spring Boot application to allow multi tenant application to access multiple databases using hibernate and C3P0. This allows user to specify pooling in a multi tenant application. This has been achieved using ComboPooledDataSource.

### Requirements ###

* Java 7+
* Maven 3.2.x+
* SQL server to create a couple of databases.

and update `application.yml` appropriately.

### Building the artifact ###

```
mvn clean package
```

### Running the application from command line ###

```
mvn spring-boot:run
```

### Available URLs

```
curl -v -H "X-TENANT-ID: tenant_1" "http://localhost:8800/demo/1"
curl -v -H "X-TENANT-ID: tenant_2" "http://localhost:8800/demo/1"
```
should result in successful responses.
