# spring-cloud-v2

---
# Readme Note 1
## Microservices samples with spring cloud. Latest versions of spring boot & spring cloud. 

 Spring Cloud LoadBalancer instead of Ribbon
 Spring Cloud Gateway instead of Zuul
 Resilience4j instead of Hystrix

## Docker: Containerize Microservices
 Run microservices using Docker and Docker Compose

## Kubernetes: Orchestrate all your Microservices with Kubernetes

## Ports

|     Application       |     Port          |
| ------------- | ------------- |
| Limits Service | 8080, 8081, ... |
| Spring Cloud Config Server | 8888 |
|  |  |
| Currency Exchange Service | 8000, 8001, 8002, ..  |
| Currency Conversion Service | 8100, 8101, 8102, ... |
| Netflix Eureka Naming Server | 8761 |
| Netflix Zuul API Gateway Server | 8765 |
| Zipkin Distributed Tracing Server | 9411 |


## URLs

|     Application       |     URL          |
| ------------- | ------------- |
| Limits Service | http://localhost:8080/limits POST -> http://localhost:8080/actuator/refresh|
|Spring Cloud Config Server| http://localhost:8888/limits-service/default http://localhost:8888/limits-service/dev |
|  Currency Converter Service - Direct Call| http://localhost:8100/currency-converter/from/USD/to/TRY/quantity/10|
|  Currency Converter Service - Feign| http://localhost:8100/currency-converter-feign/from/EUR/to/TRY/quantity/10000|
| Currency Exchange Service | http://localhost:8000/currency-exchange/from/EUR/to/TRY http://localhost:8001/currency-exchange/from/USD/to/TRY|
| Eureka | http://localhost:8761/|
| Zuul - Currency Exchange & Exchange Services | http://localhost:8765/currency-exchange-service/currency-exchange/from/EUR/to/TRY http://localhost:8765/currency-conversion-service/currency-converter-feign/from/USD/to/TRY/quantity/10|
| Zipkin | http://localhost:9411/zipkin/ |
| Spring Cloud Bus Refresh | http://localhost:8080/bus/refresh |
---

# Readme Note 2
## Limits-Service URL
http://localhost:8080/limits

# Readme Note 3
## Config Server URL
http://localhost:8888/limits-service/dev
http://localhost:8888/limits-service/qa
http://localhost:8888/limits-service/default

# Readme Note 4
## Currency Exchange Service URL
http://localhost:8000/currency-exchange/from/USD/to/TRY

## Currency Conversion Service
http://localhost:8100/currency-conversion/from/USD/to/TRY/quantity/10
http://localhost:8100/currency-conversion-feign/from/USD/to/TRY/quantity/10

## Eureka
http://localhost:8761/

## API GATEWAY
http://localhost:8765/CURRENCY-EXCHANGE/currency-exchange/from/USD/to/TRY
http://localhost:8765/CURRENCY-CONVERSION/currency-conversion/from/USD/to/TRY/quantity/10
http://localhost:8765/CURRENCY-CONVERSION/currency-conversion-feign/from/USD/to/TRY/quantity/10

http://localhost:8765/currency-exchange/currency-exchange/from/USD/to/TRY
http://localhost:8765/currency-conversion/currency-conversion/from/USD/to/TRY/quantity/10
http://localhost:8765/currency-conversion/currency-conversion-feign/from/USD/to/TRY/quantity/10