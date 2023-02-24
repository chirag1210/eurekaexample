# eurekaexample


# Eureka server (Naming-server)

- ***Step 1*** :  add dependencies for eureka-server  
  
```
pom.xml  
  
<dependency>  
			<groupId>org.springframework.cloud</groupId>  
			<artifactId>spring-cloud-starter-netflix-eureka-server</artifactId>  
		</dependency>  
``` 
   
- ***Step 2***: Goto main application class and ***@EnableEurekaServer***  
  
- ***Step 3***: Goto 
```
application.properties 
    
spring.application.name=naming-server
server.port=8761

eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false
```
  
Step 4: Run application   
```
localhost:8761

it will display eureka page
```

- ***Step 5***: Go to currency-exchange & currency-conversion application  
```  
add eureka client dependencies  
<dependency>  
			<groupId>org.springframework.cloud</groupId>  
			<artifactId>spring-cloud-starter-netflix-eureka-client</artifactId>  
		</dependency>  
```		
  
step 6: go to 
```
application.properties  
  
eureka.client.serviceUrl.defaultZone=http://localhost:8761/eureka		
```		
		
		
