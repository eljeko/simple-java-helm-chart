# Manual deploy


## build the app locally

```
mvn clean package spring-boot:repackage
```

## Create the binary builder

Login into OCP from cli

Install the helm chart  ```java-build-chart```


Run the binary deploy from cli:

```
oc start-build springboot-app --from-file target/bookstore-books-rest-api-1.0.jar
```