# Circuit Breaker Pattern

The circuit breaker pattern was popularized by the book Release It by Michael
Nygard.  This pattern allows for systems that make remote calls to degrade
gracefully when these network calls fail.

The pattern wraps the network call inside a circuit breaker object that monitors
the calls for failures and successes.  If the call fails, the circuit breaker
trips and subsequent calls will return an error or a default value.  The
circuit breaker will attempt the network call after a certain threshold is
reached.  If the call succeeds, the circuit is closed until another failure is
detected.

#Hystrix
Hystrix is Netflix's implementation of the circuit breaker pattern.  Spring Boot
has brought this library into the Spring ecosystem.

Add the circuit breaker pattern to the application by using Spring Boot's implementation of Hystrix.  The following post will give you more information
on how to add Hystrix -

https://spring.io/guides/gs/circuit-breaker/

# More Resources
[Spring Boot and Hystrix](https://spring.io/guides/gs/circuit-breaker/)

[Circuit Breaker by Martin Fowler](https://martinfowler.com/bliki/CircuitBreaker.html)
