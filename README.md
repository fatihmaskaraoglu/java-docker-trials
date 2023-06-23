# Docker

## Images

- https://hub.docker.com/repository/docker/fatihmas/myapp/general

  
- Currency Exchange Service 
	- myapp/mmv2-currency-exchange-service:0.0.1-SNAPSHOT
- Currency Conversion Service
	- myapp/mmv2-currency-conversion-service:0.0.1-SNAPSHOT
- Eureka
	- myapp/mmv2-naming-server:0.0.1-SNAPSHOT
- API GATEWAY
	- myapp/mmv2-api-gateway:0.0.1-SNAPSHOT

## URLS

#### Currency Exchange Service
- http://localhost:8000/currency-exchange/from/USD/to/INR

#### Currency Conversion Service
- http://localhost:8100/currency-conversion/from/USD/to/INR/quantity/10
- http://localhost:8100/currency-conversion-feign/from/USD/to/INR/quantity/10

#### Eureka
- http://localhost:8761/

#### Zipkin
- http://localhost:9411/

#### API GATEWAY
- http://localhost:8765/currency-exchange/from/USD/to/INR
- http://localhost:8765/currency-conversion/from/USD/to/INR/quantity/10
- http://localhost:8765/currency-conversion-feign/from/USD/to/INR/quantity/10
- http://localhost:8765/currency-conversion-new/from/USD/to/INR/quantity/10

#### Commands
```
docker run -p 9411:9411 openzipkin/zipkin:2.23
docker push docker.io/myapp/mmv2-currency-exchange-service:0.0.1-SNAPSHOT
docker-compose --version
docker-compose up
docker push myapp/mmv2-naming-server:0.0.1-SNAPSHOT
docker push myapp/mmv2-currency-conversion-service:0.0.1-SNAPSHOT
docker push myapp/mmv2-api-gateway:0.0.1-SNAPSHOT
watch -n 0.1 curl http://localhost:8000/sample-api
```
