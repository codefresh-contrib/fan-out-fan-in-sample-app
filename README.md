# Use parallel mode to fan-in and fan-out your step dependencies

![codefresh](flat-logo.png)

This is an example Java application that uses Spring Boot 2, Maven and Docker.
It is compiled using Codefresh.

## Instructions

To compile (also runs unit tests)

```
cd complete
mvn package
```

## To run the webapp manually

```
mvn spring-boot:run
```

...and navigate your browser to  http://localhost:8080/

## To create the Docker image

```
cd complete
mvn package
docker build -t fan-out-fan-in-sample .
```

## To run the docker image

```
docker run -p 8080:8080 fan-out-fan-in-sample
```

## To use this project in Codefresh 

There is also a [codefresh.yml](codefresh.yml) for easy usage with the [Codefresh](codefresh.io) CI/CD platform.


More details can be found in [Codefresh documentation](https://codefresh.io/docs//docs/yaml-examples/examples/fan-in-fan-out/)

