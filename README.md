# config-server
````
Spring boot config server which provides configuration file 
to it's client based on profiles from configured config-repository...
add set -Dhttps.proxyHost= -Dhttps.proxyPort= as VM Argument if it is required ?  
when you have used cloud url like 
uri: https://github.com/singhmahabir/config-repository
````

##### you can run the application using maven and port like below
> - mvn spring-boot:run
> - Runs on port 8701

** config server urls **
1. https://cloud.spring.io/spring-cloud-config/multi/multi__spring_cloud_config_server.html
2. https://cloud.spring.io/spring-cloud-config/multi/multi__quick_start.html

------------------------------------------------------------
#### How config files looks like
> {ServiceID}-{profile}.properties

1. ServiceID defined as below
    - spring.application.name = anyname

2. profile
    - anyname-dev.properties
    - anyname-test.properties
    - Here **dev** and **test** are profiles
3. Example
    - anyname-dev.properties
    - http://localhost:8701/{service-Id}/{profile}/{label}
    - http://localhost:8701/{required}/{required}/{optional}
    - http://localhost:8701/s1rates/test/master

------------------------------------------------------------

#### Below properties must be on bootstrap.yml

````
spring:
  cloud: 
    config:
      server:
        encrypt:
          enabled: false
encrypt:
  key: ABCDEFGHIJKLMNOPQRSTUVWXYZ
````