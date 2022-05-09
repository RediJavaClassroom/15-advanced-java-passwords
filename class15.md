# Authentication, passwords, hashing

----

## Where are we at?

* We implemented link shortner service
* We know how to use Spring Security to protect our controllers

----

## Agenda for today
* Recap: testing with docker
* Live coding storing password in database

----

### Run the application
```
mvn clean package
docker-compose build
docker-compose up
```

Alternatively

```
docker run --publish 5432:5432 --env POSTGRES_PASSWORD=mysecretpassword --detach postgres
+ run in IntelliJ IDEA
```

----

## Try application
```
curl -X POST http://localhost:8080/links --data '{"url": "https://mkysoft.com"}' -H "Content-Type: application/json"
curl http://localhost:8080/xxx -v
```

----

## Recap

Testcontainers

----


## Hashing

* "Non-reversable function"

![](img/class15-hashing.png)
From https://auth0.com/blog/hashing-passwords-one-way-road-to-security/


----

## Home assignment
* Implement hashing with something stronger than MD5


