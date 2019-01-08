# spring-config-autorefresh
Spring config server and client implementation. The client's configuration is auto refreshed without the need to restart the client or server

# How to test the functionality
1. Git clone https://github.com/amitdhodi/spring-config-autorefresh.git

2. Import configclient and configserver gradle projects in IDE

3. Build and run first the configserver and then the configclient project

4. configserver runs on port 8888 and configclient runs on port 8080

5. configserver refers to git URL https://github.com/amitdhodi/spring-config-autorefresh.git to refer to ConfigClient.properties (ConfigClient is also the name of the client project) 

6. configclient project refers to the property "message" present in file ConfigClient.properties using URL http://localhost:8080/message (hitting this URL would display the message property)

# Property Refresh
7. Update the file ConfigClient.properties present at https://github.com/amitdhodi/spring-config-autorefresh.git location and commit it.

8. Hit the refresh endpoint in client project (http://localhost:8080/actuator/refresh). This would fetch the latest property value from the ConfigClient.properties

9. Access the endpoint http://localhost:8080/message again, the updated property value is displayed

 
