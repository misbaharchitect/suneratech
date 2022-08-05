# suneratech Microservices Training

# JDK-11:
https://www.oracle.com/java/technologies/javase-jdk11-downloads.html

# JDK-8 : 
https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

# Spring Boot Links:
https://start.spring.io
https://spring.io/projects
https://spring.io/projects/spring-boot
https://spring.io/guides/gs/spring-boot/
latest: https://docs.spring.io
https://spring.io/guides/gs/spring-boot/
https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-documentation


# Maven Commands:
mvnw clean install -Dmaven.test.skip=true
mvnw clean
mvnw clean package -Dmaven.test.skip=true

# Dependencies: 
Web, Jpa, H2
swagger:
		<dependency>
			<groupId>org.springdoc</groupId>
			<artifactId>springdoc-openapi-ui</artifactId>
			<version>1.6.9</version>
		</dependency>
		
# Swagger-url:
http://localhost:8080/swagger-ui/index.html
http://localhost:8081/v3/api-docs/
		
application.properties:
server.port=8080

# H2-Inmemory DB-console --> http://localhost:8080/h2-console
spring.h2.console.enabled=true
# Hibernate/JPA
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=create

# Actuator
management.endpoints.web.exposure.include=*

spring data jpa:
https://spring.io/guides/gs/accessing-data-jpa/
Nice example for "Supported keywords inside method names":
https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#jpa.query-methods.query-creation
spring data jpa with mysql:
https://spring.io/guides/gs/accessing-data-mysql/

# Actuator Doc:
https://docs.spring.io/spring-boot/docs/current/reference/html/production-ready-features.html
Customize: 
https://www.baeldung.com/spring-boot-actuators

# Actuator
management.endpoints.web.exposure.include=*
management.endpoint.web.exposure.exclude=beans

# /actuator/beans
endpoints.beans.id=springbeans
endpoints.beans.sensitive=false
endpoints.beans.enabled=true

# /actuator/info
info.app.name=Actuator-App
info.app.description=My Edu App
info.app.version=1.2.3

# Profile
spring.profiles.active=dev,messaging
-Dspring.profiles.active=dev
--spring.profiles.active=dev

java -jar orderms.jar --server.port=8082 --spring.profiles.active=prod
java -jar orderms.jar --server.port=8083
mvn spring-boot:run
mvn spring-boot:run -Dspring-boot.run.arguments=--server.port=8085

# xml
		<dependency>
			<groupId>com.fasterxml.jackson.dataformat</groupId>
			<artifactId>jackson-dataformat-xml</artifactId>
		</dependency>
		

Config-server:
http://localhost:9999/config-client/default
http://localhost:8085/properties
curl -X POST http://localhost:8085/actuator/refresh -v



API Gateway:
http://localhost:8080/actuator/gateway/routes
http://localhost:8080/dummy/hello-client


Oauth2 Security:
curl -X POST -d grant_type=client_credentials http://client:secret@localhost:9000/oauth/token

curl -X GET http://localhost:8080/actuator/gateway/routes -v -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzY29wZSI6WyJyZWFkIl0sImV4cCI6MTY1OTcxODUzNSwianRpIjoiY2U4ZTEyNDMtZTQ5YS00NTIxLWIzZWUtZDE4YmIzMTlmYzJkIiwiY2xpZW50X2lkIjoiY2xpZW50In0.myNynHDa73XdoDmx9D3Y3UE72jWiSQp2eQwVvTUd4yU"
curl -X GET http://localhost:8080/dummy-firstms/hello -v -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzY29wZSI6WyJyZWFkIl0sImV4cCI6MTY1OTcxODUzNSwianRpIjoiY2U4ZTEyNDMtZTQ5YS00NTIxLWIzZWUtZDE4YmIzMTlmYzJkIiwiY2xpZW50X2lkIjoiY2xpZW50In0.myNynHDa73XdoDmx9D3Y3UE72jWiSQp2eQwVvTUd4yU"


MCQ Link:
https://docs.google.com/forms/d/e/1FAIpQLScSPFV8PmneKkIT6zJEAU81-xd8XBBMEy7rAauPsLSB6x-8tg/viewform?vc=0&c=0&w=1&flr=0

--------------------------------------------------------------------------------------------------------------------------------------------------------------------

++++ Installations Starts ++++
- JDK-11:
https://www.oracle.com/java/technologies/javase-jdk11-downloads.html
- Important JDK-8 : https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
Set Path of JAVA_HOME
https://docs.oracle.com/cd/E19182-01/820-7851/inst_cli_jdk_javahome_t/
- Recommend to install JDK-11
- Optional: Maven: https://maven.apache.org/download.cgi
	https://www.mkyong.com/maven/how-to-install-maven-in-windows/
	Download Maven: https://maven.apache.org/download.cgi
	Extract Maven
	Set Path of Maven
	
IDE--> Eclipse/Netbeans/SpringToolSuite/Intellij Idea(Community/Ultimate Edition)
Eclipse: https://www.eclipse.org/downloads/packages/
Intellij Idea(Community): https://www.jetbrains.com/idea/download/#section=windows

---- Installation ends ----

**** Install JDK-11 before proceeding ****

++++ Spring Boot Links Starts ++++

https://spring.io/projects
https://spring.io/projects/spring-boot
https://spring.io/guides/gs/spring-boot/
latest: https://docs.spring.io
https://docs.spring.io/spring-boot/docs/2.3.3.RELEASE/reference/htmlsingle/#using-boot-starter
https://docs.spring.io/spring-boot/docs/2.2.2.RELEASE/reference/htmlsingle/
https://spring.io/guides/gs/spring-boot/
https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/#boot-documentation

Reactive programming links:
https://projectreactor.io/
https://spring.io/reactive
https://spring.io/blog/2016/04/19/understanding-reactive-types
https://docs.spring.io/spring-framework/docs/current/reference/html/web-reactive.html#webflux

RSocket:
https://docs.spring.io/spring-framework/docs/current/reference/html/web-reactive.html#rsocket

Commercial Support:
Commercial support for Spring Boot is available from VMware. Please see https://tanzu.vmware.com/spring-runtime for details.


SpringBoot--> https://start.spring.io/
For Dotnet(Netflix OSS)--> https://steeltoe.io/

---- Spring Boot Links Ends ----

++++ Userms Starts ++++
Browser -> https://start.spring.io/
Enter Group, Artifact and add Dependencies.
Dependencies: Web, Jpa, H2, Lombok, Eureka-Client, sleuth/zipkin
Download zip, Extract and open console/cmd from the extracted directory where "pom.xml" exists.

Run:
Windows:
mvnw clean install -Dmaven.test.skip=true
Linux/MacOS:
chmod +x ./mvnw
./mvnw clean install -Dmaven.test.skip=true

++++ Maven ++++
deletes target directory
mvn clean

generates target directory with respective jar eg. userms.jar and compiles & executes tests
mvn install

-Dmaven.test.skip=true: does not compile test code and does not execute them

-DskipTests: compiles test code but does not execute them

-P: activates profile declared in pom.xml eg. -Pzipkin

launches spring-boot project from console/cmd:
java -jar orderms.jar 
java -jar orderms.jar --server.port=8083

compiles and launches spring-boot project:
mvn spring-boot:run
mvn spring-boot:run -Dspring-boot.run.arguments=--server.port=8085

Maven Commands:
mvn clean install -DskipTests
mvnw clean install -Dmaven.test.skip=true
mvnw clean install -Dmaven.test.skip=true -Pzipkin
java -jar orderms.jar --server.port=8082 --spring.profiles.active=prod
java -jar orderms.jar --server.port=8083
mvn spring-boot:run
mvn spring-boot:run -Dspring-boot.run.arguments=--server.port=8085
mvn spring-boot:run -Pzipkin -Dspring-boot.run.arguments=--spring.profiles.active=prod
mvn clean install -Pintegration
mvn spring-boot:run -Pzipkin

Gradle:
gradlew clean
gradlew build -x test
---- Userms Ends ----

++++ Orderms Starts ++++
Dependencies: Web or Spring Data Rest, Jpa, H2, Lombok, sleuth/zipkin, Eureka-Client

orderms-properties:
logging.level.org.springframework: DEBUG
server.port=8082
spring.application.name=orderms
security.basic.enabled=false

#H2-Inmemory DB-console --> http://localhost:8081/h2-console
spring.h2.console.enabled=true
#Hibernate/JPA
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=
spring.jpa.hibernate.ddl-auto=create

spring.h2.console.path=/h2

#Eureka config
eureka.client.serviceUrl.defaultZone=http://localhost:8761/eureka

spring.profiles.active=dev,messaging
H2#
console: http://localhost:8080/h2-console
jdbc:h2:mem:testdb
username: sa
password: empty (means no password)

data.sql or import.sql:::
insert into order_data (order_name, user_id, nick_name) values ('iPhone-X', 1, 'Apple-Phone-X');
insert into order_data (order_name, user_id, nick_name) values ('iPhone-Normal', 1, 'Apple-Phone');
insert into order_data (order_name, user_id, nick_name) values ('Nexus-7', 2, 'Google-7');
insert into order_data (order_name, user_id, nick_name) values ('Nexus-6', 2, 'Google-6');
insert into order_data (order_name, user_id, nick_name) values ('Blackberry', 2, 'BB');
insert into order_data (order_name, user_id, nick_name) values ('BlueBerry', 1, 'BB');
insert into order_data (order_name, user_id, nick_name) values ('BrownBerry', 1, 'BB');

---- Orderms Ends ----

++++ Zuul Starts ++++

https://cloud.spring.io/spring-cloud-netflix/multi/multi__router_and_filter_zuul.html
https://github.com/marcosbarbero/spring-cloud-zuul-ratelimit/blob/master/README.adoc
https://github.com/marcosbarbero/spring-cloud-zuul-ratelimit

Spring Cloud Gateway:
https://spring.io/blog/2021/04/05/api-rate-limiting-with-spring-cloud-gateway
https://cloud.spring.io/spring-cloud-gateway/reference/html/#fully-expanded-arguments


Dependencies: spring-cloud-starter-netflix-zuul, Eureka-Client
@SpringBootApplication
@EnableZuulProxy

Filter:
RequestContext currentContext = RequestContext.getCurrentContext();
        currentContext.set("starttime", Instant.now());

application.properties:
server.port=8080
spring.application.name=apigateway

eureka.client.serviceUrl.defaultZone=http://localhost:8761/eureka
ribbon.eureka.enabled=true

#Zuul Properties
# http://localhost:8080/api/userms/users using prefix here
#zuul.prefix=/api
# http://localhost:8080/actuator/routes
management.endpoints.web.exposure.include=*
#management.endpoints.web.exposure.exclude=*
zuul.ignored-services=orderms,userms,paymentms





---- Zuul Ends ----

++++ Distributed Tracing Starts ++++
Zipkin:
https://zipkin.io/pages/quickstart.html
Download jar of Zipkin
java -jar zipkin.jar

application.properties
spring.zipkin.baseUrl=http://localhost:9411
# 100 % traces sent
spring.sleuth.sampler.percentage=1

Sleuth/Zipkin:
https://cloud.spring.io/spring-cloud-static/Greenwich.SR5/multi/multi__introduction.html

Sleuth Custom Sampling:
https://cloud.spring.io/spring-cloud-sleuth/2.0.x/multi/multi__sampling.html

Dotnet Tracing:
https://opencensus.io/quickstart/dotnet/tracing/
Dotnet Zipkin:
https://github.com/openzipkin/zipkin4net

---- Distributed Tracing Ends ----

Feign:
https://cloud.spring.io/spring-cloud-static/Greenwich.SR5/multi/multi_spring-cloud-feign.html

++++ spring data jpa starts ++++

https://spring.io/guides/gs/accessing-data-jpa/
Nice example for "Supported keywords inside method names":
https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#jpa.query-methods.query-creation
spring data jpa with mysql:
https://spring.io/guides/gs/accessing-data-mysql/
spring data rest: data-rest
https://spring.io/guides/gs/accessing-data-rest/
https://docs.spring.io/spring-data/rest/docs/current/reference/html/#reference
https://docs.spring.io/spring-data/rest/docs/current/reference/html/#customizing-sdr
@RepositoryRestController
https://www.baeldung.com/spring-data-rest-validators
Page<User> findByUserName(@RequestParam("id") Long id, Pageable pageable);

---- spring data jpa ends ----


------------------------


--------------------------------------------------

# application.properties
https://docs.spring.io/spring-boot/docs/current/reference/html/common-application-properties.html
https://docs.spring.io/spring-boot/docs/current/reference/html/appendix-application-properties.html
# Tomcat:
https://www.baeldung.com/spring-boot-configure-tomcat

HTTP Methods:
GET: Yes == Idempotent + Safe
POST: No == Non-Idempotent + Not-Safe
DELETE: No/Yes == Idempotent + Not-Safe
PUT: No/Yes == Idempotent + Not-Safe
PATCH: No == Non-Idempotent + Not-Safe

Exception Handling:
https://www.baeldung.com/exception-handling-for-rest-with-spring
spring-security:
https://spring.io/guides/gs/securing-web/
https://www.manning.com/books/spring-security-in-action
https://www.baeldung.com/spring-security-method-security

swagger-ui: 
http://localhost:8082/swagger-ui.html
http://localhost:8082/swagger-ui/index.html
http://localhost:8082/swagger-ui/
http://localhost:8081/v3/api-docs/
springdoc.api-docs.path=/api-docs
http://localhost:8081/api-docs/
++++++++ Eureka Starts ++++++++:
http://localhost:8761/
https://cloud.spring.io/spring-cloud-netflix/reference/html/
# https://github.com/Netflix/eureka/wiki/Understanding-eureka-client-server-communication#renew
https://medium.com/@zilayhuda/register-nodejs-service-with-netflix-eureka-and-use-zuul-for-routing-service-part-1-e50fc49d1219

Eureka Clients Availability-Zone specific for Peer Aware Eureka:
https://docs.spring.io/spring-cloud-netflix/docs/current/reference/html/index.html#alternatives-to-the-native-netflix-eurekaclient
Eureka Highly Available Deployment Model:
https://cloud.spring.io/spring-cloud-netflix/multi/multi_spring-cloud-eureka-server.html

server.port=8761
spring.application.name=eureka-server

#Eureka Not Peer Aware(Standalone)
eureka.client.register-with-eureka=false
eureka.client.fetch-registry=false
eureka.server.enableSelfPreservation=false

-------- Eureka Ends --------
++++++++ Load Balancer Starts ++++++++
https://cloud.spring.io/spring-cloud-netflix/multi/multi_spring-cloud-ribbon.html
https://spring.io/blog/2020/03/25/spring-tips-spring-cloud-loadbalancer
https://cloud.spring.io/spring-cloud-openfeign/reference/html/
--------------- Load Balancer  Ends-----------------

HATEOAS--> API Maturity Level
HATEOAS (Hypertext As The Engine Of Application State)
https://martinfowler.com/articles/richardsonMaturityModel.html

Domain Driven Design:
https://www.amazon.in/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215

Implementing DDD:
https://www.amazon.in/Implementing-Domain-Driven-Design-Vernon/dp/9332545480?tag=googinhydr18418-21&tag=googinkenshoo-21&ascsubtag=_k_CjwKCAjwvbLkBRBbEiwAChbckRXXF_hou6s4hYWBxio_AgLBgdgotwtsjaZy7OmJP7BqUz4xfduNHhoCKYgQAvD_BwE_k_&gclid=CjwKCAjwvbLkBRBbEiwAChbckRXXF_hou6s4hYWBxio_AgLBgdgotwtsjaZy7OmJP7BqUz4xfduNHhoCKYgQAvD_BwE

Microservice Book:
https://www.amazon.in/Building-Microservices-Designing-Fine-Grained-Systems-ebook/dp/B00T3N7XB4

Richardson Maturity Model:
https://martinfowler.com/articles/richardsonMaturityModel.html

+++++++++++ Saga and Finite State Machine Starts ++++++++
State Machine Factory:
https://docs.spring.io/spring-statemachine/docs/current/api/
https://docs.spring.io/spring-statemachine/docs/current/reference
MachineId:
https://docs.spring.io/spring-statemachine/docs/current/reference/#sm-machineid

Persisting State Machine:
https://docs.spring.io/spring-statemachine/docs/current/reference/#sm-persist

State machine Distributed:
https://docs.spring.io/spring-statemachine/docs/current/reference/#sm-distributed

dependency:
<dependency>
	<groupId>org.springframework.statemachine</groupId>
	<artifactId>spring-statemachine-core</artifactId>
	<version>2.2.0.RELEASE</version>
</dependency>

Saga Pattern:
https://microservices.io/patterns/data/saga.html

curl -X POST -v -H "Content-Type: application/json" http://localhost:8079/orders -d "{\"sourceLocation\":\"New Delhi\", \"destinationLocation\":\"Mumbai\"}"

-------- Saga and Finite State Machine Ends --------

Domain Driven Design:

https://www.amazon.in/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215

https://www.amazon.in/dp/B00BCLEBN8/ref=dp-kindle-redirect?_encoding=UTF8&btkr=1

Netflix OSS:
https://github.com/Netflix/eureka

#Actuator Doc:
https://docs.spring.io/spring-boot/docs/current/reference/html/production-ready-features.html
Customize: 
https://www.baeldung.com/spring-boot-actuators

#Actuator
management.endpoints.web.exposure.include=*
management.endpoint.web.exposure.exclude=beans

#/actuator/beans
endpoints.beans.id=springbeans
endpoints.beans.sensitive=false
endpoints.beans.enabled=true

#/actuator/info
info.app.name=Actuator-App
info.app.description=My Edureka App
info.app.version=1.2.3


++++ Lombok Starts ++++
Eclipse/STS:
There are few things that you need to do to fix lombok issue with eclipse:
1. run "java -jar lombok.jar" from .m2\repository\org\projectlombok\lombok\1.18.18 directory
2. Select eclipse.ini file. Note you need to choose "ini" file of eclipse.
3. Close eclipse. Do not select restart option. Simple Exit. 
4. Launch eclipse
5. Clean all projects.

Intellij Idea:
Idea--> Plugins --> Repository --> Lombok --> Install--> Restart

---- Lombok Ends ----
++++ Cucumber Starts ++++
Cucumber:
https://cucumber.io/
Eclipse: https://marketplace.eclipse.org/content/cucumber-eclipse-plugin
Eclipse -> Help -> Marketplace -> Search "Cucumber" -> Install
Eclipse -> Right Click Project -> Configure -> Convert to Cucumber Project
Intellij Idea: 
Idea--> Plugins --> Repository --> Cucumber(also installs Gherkin) --> Install--> Restart


++ users.feature ++
Feature: users api calls

  Background: Clean up database
    Given I have no data in users table
    And I add a new user with name NewName

  Scenario: client wants to fetch all users
    When client calls /users GET api
    Then client receives following users
      | userName |
      | NewName  |

-- users.feature --
++ UserStepDefinition ++
package com.edureka.userms.steps;

import com.edureka.userms.model.User;
import com.edureka.userms.repository.UserRepository;
import io.cucumber.datatable.DataTable;
import io.cucumber.java.en.And;
import io.cucumber.java.en.Given;
import io.cucumber.java.en.Then;
import io.cucumber.java.en.When;
import io.cucumber.spring.CucumberContextConfiguration;
import org.hamcrest.Matchers;
import org.junit.Assert;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.boot.test.autoconfigure.web.servlet.AutoConfigureMockMvc;
import org.springframework.boot.test.context.SpringBootTest;
import org.springframework.http.MediaType;
import org.springframework.test.context.TestPropertySource;
import org.springframework.test.web.servlet.MockMvc;
import org.springframework.test.web.servlet.MvcResult;
import org.springframework.test.web.servlet.ResultActions;
import org.springframework.test.web.servlet.request.MockHttpServletRequestBuilder;
import org.springframework.test.web.servlet.request.MockMvcRequestBuilders;
import org.springframework.test.web.servlet.result.MockMvcResultHandlers;
import org.springframework.test.web.servlet.result.MockMvcResultMatchers;

import java.util.List;

@CucumberContextConfiguration
@SpringBootTest(webEnvironment = SpringBootTest.WebEnvironment.RANDOM_PORT)
@TestPropertySource(locations = "classpath:application-test.properties")
@AutoConfigureMockMvc
public class UserStepDefinition {
    @Autowired
    private UserRepository userRepository;
    @Autowired
    private MockMvc mockMvc;
    private MvcResult mvcResult;
    private ResultActions resultActions;

    @Given("I have no data in users table")
    public void cleanupUsersTable() {
        userRepository.deleteAll();
    }

    @And("^I add a new user with name (\\w+)$")
    public void addNewUser(String userName) {
        System.out.println("UserName: " + userName);
        final User user = new User();
        user.setName(userName);
        userRepository.save(user);
    }

    @When("client calls /users GET api")
    public void getAllUsers() throws Exception {
        System.out.println("111111");
        final MockHttpServletRequestBuilder requestBuilder = MockMvcRequestBuilders.get("/users");
        resultActions = mockMvc.perform(requestBuilder)
                .andDo(MockMvcResultHandlers.print());
    }

    @Then("client receives following users")
    public void verifyAllUsers(DataTable dataTable) throws Exception {
        System.out.println("22222");
        final List<String> userList = dataTable.asList();
        Assert.assertEquals("userName", userList.get(0));
        resultActions.andExpect(MockMvcResultMatchers.content().contentType(MediaType.APPLICATION_JSON))
                .andExpect(MockMvcResultMatchers.jsonPath("$[0].name", Matchers.is(userList.get(1))))
        ;
    }

}
-- UserStepDefinition --



---- Cucumber Ends ----
++++++++ Docker starts ++++++++ 
docker:
install Docker on windows machine:
https://docs.docker.com/toolbox/toolbox_install_windows/
https://docs.docker.com/install/linux/docker-ce/ubuntu/
https://docs.docker.com/engine/reference/commandline/tag/

Docker toolbox error:
"this computer doesn't have VT-X/AMD-v enabled. enabling it in BIOS is mandatory"
In case virtualization is already enabled (check in TaskManager Performance Tab)

replace below line with flag "--virtualbox-no-vtx-check" in C:\Program Files\Docker Toolbox\start.sh
echo "Misbah script"
  #"${DOCKER_MACHINE}" create -d virtualbox $PROXY_ENV "${VM}"
  "${DOCKER_MACHINE}" create -d virtualbox --virtualbox-no-vtx-check $PROXY_ENV "${VM}"


pom.xml
cd <directory to your microservices>
add dockerfile
add docker plugin to pom.xml file

Don't use maven plugin anymore.
properties: <docker.image.prefix>edureka</docker.image.prefix>
<plugin>
	<groupId>com.spotify</groupId>
	<artifactId>dockerfile-maven-plugin</artifactId>
	<version>1.4.9</version>
	<configuration>
		<repository>${docker.image.prefix}/${project.artifactId}</repository>
		<buildArgs>
			<JAR_FILE>target/${project.build.finalName}.jar</JAR_FILE>
		</buildArgs>
	</configuration>
</plugin>

dockerfile:
FROM openjdk:8-jdk-alpine
VOLUME /tmp
ARG JAR_FILE
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./urandom","-jar","/app.jar"]


FROM openjdk:8-jdk-alpine
VOLUME /tmp
COPY orderms-0.0.1-SNAPSHOT.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]

FROM openjdk:11-jdk-slim
VOLUME /tmp
# Copy jar file form host to container and rename
COPY orderms-0.0.1-SNAPSHOT.jar app.jar
ENTRYPOINT ["java","-jar","/app.jar"]

implicitly this is what Docker runs(Entrypoint): java -jar app.jar

---------AWS Docker simpler one(20-Dec-2020)---------
Browser based Docker (Play with Docker for four hours per session):
https://labs.play-with-docker.com/

Amazon Linux AMI:
chmod 400 <your-key-pair>
ssh -i "<your-key-pair>" 
ec2-user@ec2-13-233-225-237.ap-south-1.compute.amazonaws.com
sudo yum update -y
# optional if Jar is already built.
sudo amazon-linux-extras install java-openjdk11
New AWS Amazon Linux suggests to use:
sudo amazon-linux-extras install docker
sudo yum install docker -y
sudo service docker status
sudo service docker start
sudo service docker status


+++++++ Deploy to AWS with Docker +++++++
1) ssh -i "19-Sep-2020.pem" ec2-user@ec2-3-95-11-221.compute-1.amazonaws.com
2) 
CentOS:
sudo yum install docker -y
Ubuntu:
sudo apt-get update
sudo apt-get install docker.io -y
sudo apt-get install git -y

docker --version

3) sudo service docker start
4) Copy jar:
CentOS:
scp -i "19-Sep-2020.pem" -r /c/code_base/21-Aug_12-Sep/orderms/target/orderms-0.0.1-SNAPSHOT.jar ec2-user@ec2-3-95-11-221.compute-1.amazonaws.com:/home/ec2-user

ubuntu:
scp -i "citius-docker.pem" -r /c/code_base/java_training_08-Nov-2021/orderms/target/orderms-0.0.1-SNAPSHOT.jar ubuntu@ec2-65-1-112-207.ap-south-1.compute.amazonaws.com:/home/ubuntu

ssh -i "citius-docker.pem" ubuntu@ec2-65-1-112-207.ap-south-1.compute.amazonaws.com
5) Add Dockerfile
6) 
sudo docker image build -t dockerHubId/repoName:imageName
sudo docker image build --tag orderms:1.0 .
sudo docker image build --tag orderms:1.0 .
7) sudo docker images
8) Run
sudo docker run -p 8081:8082 -t 3e739e0937c5
sudo docker run -p 8081:8082 -t orderms:1.0

------- Deploy to AWS with Docker -------


docker compose install:
https://docs.docker.com/compose/install/
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

sudo chmod +x /usr/local/bin/docker-compose
docker-compose version
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
sudo docker-compose up

Start a new shell



-- Try uploading only jar file
scp -i "19-Sep-2020.pem" -r /c/code_base/21-Aug_12-Sep/orderms/target/orderms-0.0.1-SNAPSHOT.jar ec2-user@ec2-3-95-11-221.compute-1.amazonaws.com:/home/ec2-user

Dockerfile:
FROM openjdk:11-jdk-slim
VOLUME /tmp
COPY orderms-0.0.1-SNAPSHOT.jar app.jar
ENTRYPOINT ["java","-Djava.security.egd=file:/dev/./from on","-jar","/app.jar"]

sudo docker images

sudo docker image build --tag orderms:1.0 .
sudo docker images
sudo docker run -p 8080:8081 -t <docker-image>
sudo docker run -p 8080:8082 -t 5e095ca12795
sudo docker run -p 8081:8082 -t 3e739e0937c5

----------------------
CentOS/Amazon Linux AMI:
sudo yum install java-1.8.0-openjdk-devel
Only CentOS:
sudo yum install java-11-openjdk-devel
For AWS Linux AMI: 
sudo amazon-linux-extras install java-openjdk11
sudo yum install docker -y

----------- copy orderms files to AWS-----
scp -i "19-Sep-2020.pem" -r /d/code_base/edureka/java-11/userms ec2-user@ec2-52-87-217-52.compute-1.amazonaws.com:/home/ec2-user
sudo yum install java-1.8.0-openjdk-devel
yum install docker -y

service docker start
scp -i "<your-key-pair>" -r /f/Edureka_Batches/28-Dec-2019_19-Jan-2020/orderms ec2-user@ec2-13-233-225-237.ap-south-1.compute.amazonaws.com:/home/ec2-user
sudo yum install java-1.8.0-openjdk-devel
yum install docker -y
service docker start

./mvnw install dockerfile:build

docker images
docker run -p 8080:8082 -t <docker-image>
docker run -p 8080:8082 -t cbb5e63bcc7b

--------------ubuntu:
ssh -i first_key_pair.pem ubuntu@18.212.3.211

update package manager:
sudo apt-get update

sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

//optional to make sure above certificate is correct
sudo apt-key fingerprint 0EBFCD88

sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

sudo apt-get update

install docker (above steps are required):
sudo apt-get install docker-ce docker-ce-cli containerd.io

docker --version
--------------ubuntu ends
in browser:
add a new/signin account: https://cloud.docker.com

Laptop:
docker login --username=<username>
docker tag <image-id> <dockerhub-repo>:<anynameofyourchoice>
docker tag cbb5e63bcc7b misbaharchitect/edureka:userms_02_Nov_19

docker push misbaharchitect/edureka:userms_02_Nov_19

docker pull misbaharchitect/edureka:userms_02_Nov_19
docker run -p 8080:8081 -t <docker-image>
docker run -p 8080:8081 -t cbb5e63bcc7b


Useful commands in Docker:
docker --version
// list all docker images
docker images

docker run hello-world

docker run -it ubuntu bash

// list running containers
docker container ls
docker ps
// list running and dead containers both
docker container ls -a
docker ps -a
// remove dead container
docker rm <container-id>
// remove image
docker rmi <image-id>
// remove all dead containers
docker system prune -a
// logs
docker logs <container-id>
// follow logs
docker logs -f <container-id>
// stop container
docker stop <container-id>
// start container
docker start <container-id>

// copy the jar file to cloud machine
scp -i "<your-pem-file>.pem" -r /c/code_base/25-Jun_17-Jul_2022/mongodbms/target/mongodbms-0.0.1-SNAPSHOT.jar ubuntu@ec2-65-1-148-159.ap-south-1.compute.amazonaws.com:/home/ubuntu
// build image
docker image build --tag mongodbms:1.0 .
// run spring-boot based docker image
docker run -d -p 8081:8080 -t 9a34ea0625b7
// tail the logs the container
docker logs -f <container-id>
// All docker logs of the container
docker logs <container-id>

-------------Docker ends-----------------
ActiveMQ:
Download: http://activemq.apache.org/activemq-5155-release.html
Windows Distribution apache-activemq-5.15.5-bin.zip

Extract to a local folder: D:\software\apache-activemq-5.15.5

D:\software\apache-activemq-5.15.5\bin>activemq start

http://127.0.0.1:8161/admin
username: admin
password: admin

-----------security starts------------
spring security basics:
https://www.baeldung.com/spring-security-expressions-basic
https://docs.spring.io/spring-security-oauth2-boot/docs/current/reference/htmlsingle/
oauth2-jdbc:
https://codeaches.com/spring-cloud-security/oauth2-authorization-jdbc-token-store
https://cloud.spring.io/spring-cloud-security/reference/html/
https://spring.io/projects/spring-security

OAuth2RestTemplate

<dependency>
   <groupId>org.springframework.cloud</groupId>
   <artifactId>spring-cloud-starter-oauth2</artifactId>
   <version>2.2.5.RELEASE</version>
</dependency>

oAuth2:
application.properties:
server.port=9000
spring.application.name=oauth-server
#Eureka Config
eureka.client.serviceUrl.defaultZone=http://localhost:8761/eureka

# deprecated since spring boot-2
security.basic.enabled=false
oAuth2:
https://www.jsonwebtoken.io/
generate access token:
curl -X POST -d grant_type=client_credentials http://candy:123@localhost:9000/oauth/token
curl -X POST -d grant_type=client_credentials http://crush:123@localhost:9000/oauth/token
From userms to oauth2 server:
curl -X POST -d grant_type=client_credentials http://candy:123@oauth-server/oauth/token
Password Grant Type, not single quote in url because of Params:
curl -v -X POST -u client:secret 'http://localhost:8080/oauth/token?grant_type=password&username=john&password=12345&scope=read'

 curl -v localhost:8080/userms/users -H "Authorization:Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzY29wZSI6WyJyZWFkIiwid3JpdGUiXSwiZXhwIjoxNTkzMzU0NDU4LCJqdGkiOiJiYjNjYTI1Ny1iMTJjLTQ4OGEtYTZiZC02YTI0MzBkMmYwZmUiLCJjbGllbnRfaWQiOiJjYW5keSJ9.xs9LAHHwfC-G-UtCJj89_Ka1WKaDZIU5QJ1adTprr1Q"
 
curl -v localhost:8080/orderms/orders -H "Authorization:Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzY29wZSI6WyJyZWFkIiwid3JpdGUiXSwiZXhwIjoxNjAwMDIyNjg5LCJqdGkiOiI1MTUwZTU0ZS05OGIxLTQ0N2UtOGQ3MC0xZTMwOTg2MWUzZjMiLCJjbGllbnRfaWQiOiJjYW5keSJ9.JroOuJOTdvWHHdOYi3yP88sWipEGk0-ZuaQ__SOM7RA"
 
curl localhost:9000/user -H "Authorization:Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzY29wZSI6WyJyZWFkIiwid3JpdGUiXSwiZXhwIjoxNTg2NjczNjA1LCJqdGkiOiI4Y2I3ZjA5YS1jOWI5LTQ5YzQtOTA0ZC1lM2I3ZTVkMmExMmMiLCJjbGllbnRfaWQiOiJjYW5keSJ9.aCmrg9LKPkAD99v5R30I9ajbkbiqb4ZxWzkhjTPKacY"

{"access_token":"3999755e-e987-4a8b-8666-d109ce0261f3","token_type":"bearer","expires_in":38,"scope":"read write"}

<dependency>
	<groupId>org.springframework.security</groupId>
	<artifactId>spring-security-jwt</artifactId>
	<version>1.0.10.RELEASE</version>
</dependency>

++++ SSO ++++
https://github.com/settings/applications/new
---- SSO ----

++++++++ SAML ++++++++
https://spring.io/projects/spring-security-saml
https://docs.spring.io/spring-security-saml/docs/current/reference/htmlsingle/

-----------security ends------------

AWS Signup:
https://aws.amazon.com/console/
aws.amazon.com/free

AWS Regions & AZ:
https://aws.amazon.com/about-aws/global-infrastructure/
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html
https://aws.amazon.com/about-aws/global-infrastructure/regions_az/

AWS ssh:
https://aws.amazon.com/free --> create your free account
Mobaxterm: 
https://mobaxterm.mobatek.net/download-home-edition.html
Personal
https://alestic.com/2014/01/ec2-ssh-username/

ssh -i "<security-key>.pem" ec2-user@<public-ip-address>

-------------------------
sudo su
yum install httpd -y
echo "<html><h1>Hello Edureka</h1></html>" > /var/www/html/index.html
ls -ltr /var/www/html/
service httpd start

Kubernetes:
https://kubernetes.io/docs/tutorials/kubernetes-basics/
https://kubernetes.io/docs/tutorials/hello-minikube/

++++++++++++++CONFIG-SERVER STARTS+++++++++++++++++
Rabbitmq:
https://www.rabbitmq.com/install-windows-manual.html
https://www.rabbitmq.com/which-erlang.html
https://www.erlang.org/downloads
set ERLANG_HOME (set by default if erlang windows installer used)

Steps:
1) install Erlang (otp_win64_22.1.exe)
2) install RabbitMQ (rabbitmq-server-3.8.1.exe)
3) cd D:\software\rabbitmq_server-3.8.9\sbin
4) rabbitmq-server.bat // should start rabbitmq server in win-console
5) rabbitmq-plugins enable rabbitmq_management //should install management web page
6) Check Management url of RabbitMQ in browser:
http://localhost:15672/mgmt
username: guest
password: guest

in case of issues do below cleanup:
D:\software\rabbitmq_server-3.8.9\sbin
rabbitmq-service remove
rabbitmq-service install
rabbitmq-plugins enable rabbitmq_management  // required for mgmt webpage
rabbitmq-service start // does not work

05-Apr-2020: Run this command to start RabbitMQ
D:\software\rabbitmq_server-3.8.9\sbin\rabbitmq-server.bat

RabbitMQ on Amazon Linux AMI:
sudo yum install rabbitmq-server
sudo systemctl enable rabbitmq-server
sudo systemctl start  rabbitmq-server
systemctl status rabbitmq-server.service
ex


ConfigServer:
https://cloud.spring.io/spring-cloud-config/reference/html/
https://cloud.spring.io/spring-cloud-config/reference/html/#_jdbc_backend
https://cloud.spring.io/spring-cloud-config/reference/html/#_push_notifications_and_spring_cloud_bus
https://cloud.spring.io/spring-cloud-config/multi/multi__spring_cloud_config_server.html#:~:text=Spring%20Cloud%20Config%20Server%20supports%20JDBC%20(relational%20database)%20as%20a,a%20bean%20of%20type%20JdbcEnvironmentRepository%20.
______________config-server dependencies:______________
https://cloud.spring.io/spring-cloud-config/multi/multi__spring_cloud_config_server.html
<dependency>
	<groupId>org.springframework.cloud</groupId>
	<artifactId>spring-cloud-config-monitor</artifactId>
	<version>2.1.2.RELEASE</version>
	<scope>runtime</scope>
</dependency>
<dependency>
	<groupId>org.springframework.cloud</groupId>
	<artifactId>spring-cloud-starter-stream-rabbit</artifactId>
	<version>2.2.0.RELEASE</version>
</dependency>

@EnableConfigServer
@EnableEurekaClient


config-server--> application.properties
#Config server
server.port=9999
spring.application.name=config-server
#Eureka config
eureka.client.serviceUrl.defaultZone=http://localhost:8761/eureka

spring.cloud.config.server.git.uri=https://github.com/misbaharchitect/hello_world.git
spring.cloud.config.server.git.clone-on-start=true
spring.cloud.bus.enabled=true

#Rabbitmq
spring.rabbitmq.host=localhost
spring.rabbitmq.port=5672
spring.rabbitmq.username=guest
spring.rabbitmq.password=guest

#Security
security.user.name=root
security.user.password=secret123
______________config-client______________
config-client dependency:
<dependency>
	<groupId>org.springframework.cloud</groupId>
	<artifactId>spring-cloud-starter-bus-amqp</artifactId>
	<version>2.1.1.RELEASE</version>
</dependency>
<dependency>
	<groupId>org.springframework.cloud</groupId>
	<artifactId>spring-cloud-starter-config</artifactId>
</dependency>

Spring-Boot > 2.5 versions:
spring.config.import=configserver:
spring.config.import=configserver:http://localhost:9999
spring.cloud.config.discovery.serviceId=config-server
spring.cloud.config.discovery.enabled=true

Spring-Boot < 2.4 versions:
config-client(userms):
#bootstrap.properties:
#spring.cloud.config.uri=http://localhost:8888
spring.cloud.config.discovery.serviceId=config-server
spring.cloud.config.discovery.enabled=true
spring.cloud.config.username=root
spring.cloud.config.password=secret123

application.properties:
server.port=8085
spring.application.name=config-client

#For integration with config-server
#Rabbitmq
spring.rabbitmq.host=localhost
spring.rabbitmq.port=5672
spring.rabbitmq.username=guest
spring.rabbitmq.password=guest

#config-server default
my-property=dummy
your-property=dummy

server.port=9999

spring.application.name=config-server
management.endpoints.web.exposure.include=*


# Provide Github uri below
spring.cloud.config.server.git.uri=https://github.com/misbaharchitect/hello_world.git
spring.cloud.config.server.git.clone-on-start=true


encrypt.key=MyEncryptionKey

______________Webhook: github:______________
curl -v -X POST "http://localhost:9999/monitor" \
-H "Content-Type: application/json" \
-H "X-Event-Key: repo:push" \
-H "X-Hook-UUID: webhook-uuid" \
-d '{"push": {"changes": []} }'

Add Webhook on github:
http://35.175.135.48:9999/monitor
curl -v -X POST "http://35.175.135.48:9999/monitor" \
-H "Content-Type: application/json" \
-H "X-Event-Key: repo:push" \
-H "X-Hook-UUID: webhook-uuid" \
-d '{"push": {"changes": []} }'

-Dspring.profiles.active=dev
--spring.profiles.active=dev
Intellij add to Program Arguments: --spring.profiles.active=dev

http://35.175.135.48:9999/config-client/global
http://35.175.135.48:9999/config-client/default
http://35.175.135.48:9999/config-client/dev
http://localhost:9999/userms/dev
http://localhost:9999/userms/global
http://localhost:9999/config-client/global
http://localhost:9999/config-client/dev
http://localhost:9999/config-client.properties
http://localhost:9999/config-client-dev.properties

Encryption:
curl --location --request POST 'localhost:9999/encrypt' \
--header 'Content-Type: text/plain' \
--data-raw 'This is a new password that we are building'

Decryption:
curl --location --request POST 'localhost:9999/decrypt' \
--header 'Content-Type: text/plain' \
--data-raw 'bd484f98b21b89ea95735ce3d7584c367168c1c4d4474b832f1e7adfbf64fe16eb882b80ae16af6c14601c0d94ede5591766c4f43afd77923db094e614e12d22'

---------------CONFIG-SERVER ENDS----------------

Chaos Monkey:
https://netflixtechblog.com/the-netflix-simian-army-16e57fbab116
https://github.com/search?q=org%3ANetflix+chaos&unscoped_q=chaos
-----------------------------
Jenkins:
https://jenkins.io/doc/pipeline/tour/getting-started/

AWS Lambda:
https://docs.aws.amazon.com/lambda/latest/dg/getting-started.html
----------------------------------------------------------
Hystrix:
https://github.com/Netflix/Hystrix/wiki
https://github.com/Netflix/Hystrix/wiki/Configuration
https://github.com/Netflix/Hystrix/wiki/How-To-Use
https://www.linkedin.com/pulse/spring-cloud-netflix-hystrix-tadeu-barbosa/
https://spring.io/guides/gs/circuit-breaker/
https://cloud.spring.io/spring-cloud-netflix/single/spring-cloud-netflix.html

@EnableHystrix

@HystrixCommand(fallbackMethod = "getUsersFromFallback", commandProperties =
            {@HystrixProperty(name = "execution.isolation.thread.timeoutInMilliseconds", value = "3000")},
	// Bulkhead
    threadPoolKey = "getAllUsersThreadPool",
    threadPoolProperties = {
            @HystrixProperty(name = "coreSize", value = "30"),
            @HystrixProperty(name = "maxQueueSize", value = "10")
    })

---------Hystrix-Dashboard Starts--------
@EnableHystrixDashboard
http://localhost:7075/hystrix
Start Eureka:
Search in Dashboard:
http://localhost:8081/actuator/hystrix.stream

Turbine:
It combines multiple service instances into one single view using Eureka. eg Cluster of services eg Dev servers, Prod Servers etc
But Turbine does not aggregate data from multiple services together into one group. So rather use Turbine Stream.

Turbine Stream:
It uses messaging to aggregate service metrics.
Hystrix Dashboard spring boot app would use an endpoint provided by Turbine Stream spring boot app.
So Hystrix Dashboard does not have to hit individual hystrix streams but hits only one Turbine stream server. Thus all services are visible in a single Dashboard.

Turbine(Without Stream):
  Hystrix-Dashboard:
	<dependency>
		<groupId>org.springframework.cloud</groupId>
		<artifactId>spring-cloud-starter-netflix-turbine</artifactId>
	</dependency>
  @EnableTurbine
  
  # Verified
  turbine.appConfig=onems-client,twoms-client
# To combine all microservices in single view
#turbine.clusterNameExpression= new String("default")
# One microservices in one view
turbine.aggregator.clusterConfig=USERMS,ONEMS-CLIENT,TWOMS-CLIENT

  application.properties
  turbine.appConfig=userms,msone-client,mstwo-client
  turbine.aggregator.clusterConfig=USERMS,MSONE-CLIENT,MSTWO-CLIENT
	Search: Hystrix-Dashboard port=7075
	http://localhost:7075/turbine.stream?cluster=default
  
  application.properties
  turbine.appConfig=onems-client,twoms-client
  turbine.clusterNameExpression= new String("default")
    Search: Hystrix-Dashboard port=7075 
	http://localhost:7075/turbine.stream?cluster=default





Turbine With Stream (RabbitMQ/Kafka):
  Turbine(Spring boot project):
	<dependency>
		<groupId>org.springframework.cloud</groupId>
  <artifactId>spring-cloud-starter-netflix-turbine-stream</artifactId>
	</dependency>
  @EnableTurbine
---------Hystrix-Dashboard Ends--------
---------------------------------------------------------
Kafka:
Download:
https://kafka.apache.org/downloads
Quickstart:
https://kafka.apache.org/quickstart

Kafka does not require Zookeeper in future:
https://issues.apache.org/jira/browse/KAFKA-9119
https://cwiki.apache.org/confluence/display/KAFKA/KIP-500%3A+Replace+ZooKeeper+with+a+Self-Managed+Metadata+Quorum#KIP500:ReplaceZooKeeperwithaSelfManagedMetadataQuorum-Status

https://kafka.apache.org/documentation/#messages

spring-kafka: https://docs.spring.io/spring-kafka/reference/html/
Dotnet-Kafka:
https://docs.confluent.io/clients-confluent-kafka-dotnet/current/overview.html

windows:
change log path in config\zookeeper.properties(dataDir) and config\server.properties

Start Zookeeper and Kafka Broker:
bin\windows\zookeeper-server-start.bat config\zookeeper.properties
bin\windows\kafka-server-start.bat config\server.properties


-- list topics
bin/kafka-topics.sh --list --bootstrap-server localhost:9092
bin\windows\kafka-topics.bat --list --bootstrap-server localhost:9092

-- New Topic
/bin/kafka-topics.sh --create --zookeeper <hostname>:<port> --topic <topic-name> --partitions <number-of-partitions> --replication-factor <number-of-replicating-servers>

bin/kafka-topics.sh --create --topic quickstart-events --bootstrap-server localhost:9092

- verified below
D:\software\kafka_2.12-2.4.1\bin\windows\kafka-topics.bat --create --zookeeper localhost:2181 --topic mytopic --partitions 2 --replication-factor 1
bin\windows\kafka-topics.bat --create --topic quickstart-events --bootstrap-server localhost:9092
bin\windows\kafka-topics.bat --create --topic abcd --bootstrap-server localhost:9092 --partitions 2 --replication-factor 1

- Delete
bin\windows\kafka-topics.bat --delete --zookeeper localhost:2181 --topic myTopic

- add partition
kafka/bin/kafka-topics. sh --create \ --zookeeper localhost:2181 \ --replication-factor 2 \ --partitions 3 \ --topic unique-topic-name Copy.
bin/kafka-topics.sh --zookeeper zk_host:port/chroot --alter --topic my_topic_name 
       --partitions 40 


-- topic details quickstart-events
bin/kafka-topics.sh --describe --topic quickstart-events --bootstrap-server localhost:9092
bin/kafka-topics.sh --describe --topic quickstart-events --bootstrap-server localhost:9092
bin\windows\kafka-topics.bat --describe --topic mytopic --bootstrap-server localhost:9092
bin\windows\kafka-topics.bat --describe --bootstrap-server localhost:9092 --topic mytopic


-- start console-producer
bin\windows\kafka-console-producer.bat --topic mytopic --broker-list localhost:9092
bin\windows\kafka-console-producer.bat --topic wordcount-input --bootstrap-server localhost:9092 --property parse.key=true --property key.separator=:

-- start console-consumer   
bin\windows\kafka-console-consumer.bat --topic edudb.payment --from-beginning --bootstrap-server localhost:9092

bin\windows\kafka-console-consumer.bat --topic mytopic123 --bootstrap-server localhost:9092
 

bin\windows\kafka-console-consumer.bat --topic paymentdb.payment --from-beginning --bootstrap-server localhost:9092

Kafka-Connect:
https://www.confluent.io/hub/?utm_medium=sem&utm_source=google&utm_campaign=ch.sem_br.nonbrand_tp.rmkt_tgt.kafka_mt.xct_rgn.india_lng.eng_dv.all&utm_term=mongodb%20kafka%20connector&creative=&device=c&placement=&gclid=CjwKCAjwlID8BRAFEiwAnUoK1SSHfYK0lQO3mJqyuBG161dmlfQZJFlHZ90q_JyEP-Tr0V1R1WQd1hoCBNgQAvD_BwE

https://kafka.apache.org/documentation/#connect



MongoDB Atlas:
https://www.mongodb.com/cloud/atlas/lp/try2?utm_source=google&utm_campaign=gs_apac_india_search_brand_atlas_desktop&utm_term=mongodb%20atlas%20login&utm_medium=cpc_paid_search&utm_ad=e&utm_ad_campaign_id=6501677905&gclid=EAIaIQobChMIoqD9gvOE7QIVQJVLBR1aaQxYEAAYASAAEgLGAvD_BwE

MongDB Community Installation:
https://docs.mongodb.com/manual/administration/install-community/

Enterprise MongoDB Embedded:
https://www.mongodb.com/licensing/embedded-license

Compass:
https://www.mongodb.com/products/compass

Change Stream:
https://docs.mongodb.com/manual/changeStreams/
https://www.mongodb.com/blog/post/an-introduction-to-change-streams

Download MongoDB-Kafka-Connect:
https://www.confluent.io/hub/mongodb/kafka-connect-mongodb
25-Jul-2021:
Download uber(all) jar from:
https://search.maven.org/search?q=a:mongo-kafka-connect
https://github.com/mongodb/mongo-kafka/blob/master/README.md

D:\\software\\mongodb\\mongodb-kafka-connect-mongodb-1.3.0
copy below to config\connect-distributed.properties
plugin.path=D:\\software\\mongodb\\mongodb-kafka-connect-mongodb-1.3.0\\lib\\mongo-kafka-1.1.0-all.jar,D:\\software\\mongodb\\m ongodb-kafka-connect-mongodb-1.1.0\\lib\\customconnector-1.0-SNAPSHOT-jar-with-dependencies.jar

start Kafka-Connect:
bin\windows\connect-distributed.bat config\connect-distributed.properties


Kafka-Connect REST-API:
curl -X GET localhost:8083/connectors

curl --location --request POST 'localhost:8083/connectors' \
--header 'Content-Type: application/json' \
--data-raw '{
	"name":"mongo-source-connector",
	"config": {
		"connector.class": "com.mongodb.kafka.connect.MongoSourceConnector",
		"tasks.max": 1,
		"connection.uri": "mongodb+srv://username:password@cluster0.fku8p.mongodb.net/M001?retryWrites=true&w=majority",
		"database": "edudb",
		"collection": "payment",
		"change.stream.full.document": "updateLookup"
	}
}'

MongoDB:
mongodb+srv://<username>:<password>@cluster0.fku8p.mongodb.net/<dbname>?retryWrites=true&w=majority

Kafka Stream:
https://cloud.spring.io/spring-cloud-static/spring-cloud-stream-binder-kafka/3.0.0.RELEASE/reference/html/spring-cloud-stream-binder-kafka.html#_setting_up_bootstrap_server_configuration

https://cloud.spring.io/spring-cloud-static/spring-cloud-stream-binder-kafka/3.0.0.RELEASE/reference/html/spring-cloud-stream-binder-kafka.html#_kafka_streams_application_id

https://www.confluent.io/blog/spring-for-apache-kafka-deep-dive-part-2-apache-kafka-spring-cloud-stream/
----
Debezium SQL Server:
https://debezium.io/documentation/reference/connectors/sqlserver.html

--------------------------------------------------------------------
Testing:
Wiremock: http://wiremock.org/
UnitTest:
mockMvc.perform(get("/test"))
                .andExpect(content().contentType(MediaType.APPLICATION_JSON_UTF8_VALUE))
                .andExpect(status().isOk())
                .andExpect(jsonPath("$.value", is("Hello!")));

@Autowired
private ObjectMapper objectMapper;				
mockMvc.perform(post("/users")
            .contentType("application/json")
            .param("mykey", "myvalue")
            .content(objectMapper.writeValueAsString(user)))
            .andExpect(status().isOk());

Contract Test:
Pact Contract Test: https://docs.pact.io/
Spring Cloud Contract:
https://cloud.spring.io/spring-cloud-contract/reference/html/
https://spring.io/projects/spring-cloud-contract
1. Make Contract groovy file
2. Run mvn clean install -DskipTests to generate stub with tests-skipped

ELK:
https://www.elastic.co/what-is/elk-stack
https://www.elastic.co/beats/
Download Elastic Search, Logstash and Kibana:
https://www.elastic.co/downloads/
Download FileBeat:
https://www.elastic.co/downloads/beats/filebeat
https://github.com/elastic/beats/tree/master/filebeat

Follow this for Filebeat setup:
https://www.elastic.co/guide/en/logstash/7.12/advanced-pipeline.html

Installation Order:
https://www.elastic.co/guide/en/elastic-stack/current/installing-elastic-stack.html
Unzip all three.

Elastic Search:
run D:\software\ELK\elasticsearch-7.12.0\bin\elasticsearch
Open http://localhost:9200

Kibana:
open D:\software\ELK\kibana-7.12.0-windows-x86_64\config\kibana.yml
Uncomment:
elasticsearch.hosts: ["http://localhost:9200"]

Kibana takes quite some time to start.
run D:\software\ELK\kibana-7.12.0-windows-x86_64\bin\kibana
open:
localhost:5601
First time user, select "Explore on my own"->
Kibana-> Discover -> Add Data -> Logstash Logs
http://localhost:5601/app/home#/tutorial/logstashLogs

install FileBeat before proceeding.
For Windows in case Powershell is not executed:
PowerShell.exe -ExecutionPolicy UnRestricted -File .\install-service-filebeat.ps1.

OR 

Set-ExecutionPolicy RemoteSigned
After runnin FileBeat Powershell, restore the policy back:
Set-ExecutionPolicy Restricted

Logstash:
Make a copy of D:\software\ELK\logstash-7.12.0\config\logstash-sample.conf
and rename to logstash.conf

D:\software\ELK\logstash-7.12.0\bin\logstash -f ..\config\logstash.conf



Unzip FileBeat:
https://www.elastic.co/guide/en/logstash/7.12/advanced-pipeline.html

open D:\software\ELK\filebeat-7.12.0-windows-x86_64\filebeat.yml
Change paths: value to your logfile path for - type: log:
eg from - /var/log/*.log to D:\software\ELK
enabled: true

Uncomment:
#output.logstash:
#hosts: ["localhost:5044"]



Spring Cloud Stream:
https://cloud.spring.io/spring-cloud-static/Greenwich.SR5/multi/multi__quick_start_2.html
https://docs.spring.io/spring-cloud-stream/docs/Brooklyn.RELEASE/reference/html/_apache_kafka_binder.html

Spring Cloud Stream is a framework for building message-driven microservice applications. Spring Cloud Stream builds upon Spring Boot to create standalone, production-grade Spring applications and uses Spring Integration to provide connectivity to message brokers. 

https://cloud.spring.io/spring-cloud-static/Greenwich.SR5/multi/multi_spring-cloud-stream-overview-introducing.html

Apache Kafka Binder/Stream:
https://cloud.spring.io/spring-cloud-static/Greenwich.SR5/multi/multi__apache_kafka_binder.html
https://cloud.spring.io/spring-cloud-stream-binder-kafka/spring-cloud-stream-binder-kafka.html#_kafka_streams_binder

RabbitMQ Binder/Stream:
https://cloud.spring.io/spring-cloud-static/Greenwich.SR5/multi/multi__rabbitmq_binder.html

Spring Cloud Bus:
https://cloud.spring.io/spring-cloud-bus/reference/html/#quick-start
https://cloud.spring.io/spring-cloud-static/Greenwich.SR5/multi/multi__spring_cloud_bus.html
Spring Cloud Bus links the nodes of a distributed system with a lightweight message broker. This broker can then be used to broadcast state changes (such as configuration changes) or other management instructions. A key idea is that the bus is like a distributed actuator for a Spring Boot application that is scaled out. However, it can also be used as a communication channel between apps. This project provides starters for either an AMQP broker or Kafka as the transport.

++++++++++++++++++++++++++
Spring-Path-Matcher:
https://docs.spring.io/spring-framework/docs/current/javadoc-api/org/springframework/util/AntPathMatcher.html
--------------------------
++++++++++++++++++++++++++
Migration Tools:
IBM Mono2Micro:
IBM Mono2Micro, offered by WebSphere Hybrid Edition, uses the power of AI to refactor Java monoliths into microservices.

https://www.ibm.com/support/pages/node/6398670

++++ Additional Links ++++
12-Factor-App:
https://12factor.net/

Service Mesh (Istio):
https://istio.io/latest/about/service-mesh/

Cache: https://www.baeldung.com/spring-boot-ehcache

Dropwizard: https://www.dropwizard.io/en/stable/
logback file: https://www.baeldung.com/spring-boot-logging

swagger code-generation: https://swagger.io/tools/swagger-codegen/


Microservice certification:
https://www.redhat.com/en/services/certification/red-hat-certified-enterprise-microservices-developer
https://aws.amazon.com/certification/
---- Additional Links ----
