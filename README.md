# config-server
Spring boot config server which provides configuration file to it's client based on profiles from configured config-repository...
add set -Dhttps.proxyHost= -Dhttps.proxyPort= as VM Argument if it is required ?  
when you have used cloud url like 
uri: https://github.com/singhmahabir/config-repository

Runs on port 8701

you can run the application using maven like below
mvn spring-boot:run

config server urls 
https://cloud.spring.io/spring-cloud-config/multi/multi__spring_cloud_config_server.html
https://cloud.spring.io/spring-cloud-config/multi/multi__quick_start.html