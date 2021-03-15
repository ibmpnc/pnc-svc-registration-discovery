# pnc-svc-registration-discovery
Sample project about service registration and discovery (eureka)


To build :

in pnc-service-registration-and-discovery directory % mvn clean install


To run and test pnc-service-registration-and-discovery :

open a terminal window, go in folder pnc-service-registration-and-discovery : run "mvn spring-boot:run -pl eureka-service"
open a terminal window, go in folder pnc-service-registration-and-discovery : run "mvn spring-boot:run -pl eureka-client"
open a terminal window, go in folder pnc-service-registration-and-discovery : run "mvn spring-boot:run -pl eureka-client-n"

In a browser do a GET to http://localhost:8099/service-instances/registry-discovery-client
=> We can see the feature "Peer Awareness" in node 0, this is the information regarding itself app 8099 and in node 1 a peer which is app 8095

In a browser do a GET to http://localhost:8095/service-instances/registry-discovery-client
=> We can see the feature "Peer Awareness" in node 0, this is the information regarding itself app 8095 and in node 1 a peer which is app 8099


In a browser do a GET to http://localhost:8761/
=> We can see all the client apps registered 
(REGISTRY-DISCOVERY-CLIENT 	n/a (2) 	(2) 	UP (2) - 192.168.5.7:registry-discovery-client:8099 , 192.168.5.7:registry-discovery-client:8095)

