# TheMicroservicesJourney

My journey to center of the microservices.


 As i begin my journey to understand what it takes to create microservices in java (i am a c++ developer and java naturally was 
  the next closest to start of with), i document simple helloworld projects, which help me understand things better. 
  
  Most of the repositories here are carved or heavily inspired from online tutorials etc., but i try to write on my own in my favorite
  eclipse editor.
  
  I would list down here the repositories in the order i started writing.
  
  The very first thing i found quite fasicnating was Spring framework, (i know little of core-java) and thats where it all begins.
  
  I start with spring mvc and move on further in the direction wind takes me.
  
 ### Day 1
 * [Spring MVC] This is a simple spring mvc project, which creates a restcontroller and showcases the use of basic servlets etc.
  
 * [Spring Boot Basic] Once i understood the basics of spring, ofcourse only a thin part of mvc, i quickly deiced that i better change gears and hooked on to Spring boot. To my surprise writing application in spring boot is quite easy. If you are from Spring background, you will have a sigh of relief. A lot of boilerplate annotations go away, and you get to work on the real meat. This application is again a simple rest server, with multiple endpoints. Idea here is to understand how i can use spring boot. As a part of it, i used spring-data-cache, Redis in this case. It was too sleek and easy with few annotations.
 This tutorial helped me understand the real deal -> https://www.baeldung.com/spring-cache-tutorial.  Then i was fascinated with the world of annotation, how easy life becomes with them and naturally wanted to write one. As a   result i wrote a small annotations creator.
 
 3. https://github.com/samair/java_annotations.git : I heavily relied on a online tutorial in order to finish this as i had no idea of what reflection really meant. At the end of writing this project i got a hang of what reflection is and how it could be used.
 
 Now i have to get back to track, plan is to write another spring boot application , this time something with a bit of meat.
 
  ### Day 2
 I stumbled upon this : http://www.springboottutorial.com/creating-microservices-with-spring-boot-part-1-getting-started
 
 Above link was quite useful to kickoff my understanding of practical usage of spring boot.
 
 As i started, i noticed that a lot stuff happen automatically, i no longer  need to define a configurations unlike spring mvc.
 If you want to connect to a Database for example H2, you need not install it anymore, spring boot provides a handy embedded H2 data base if it finds the jar in the CLASSPATH.
 
Found a good link which explains how this magic happens :
http://www.springboottutorial.com/spring-boot-auto-configuration

 ### Day 3
So, now i completed a small microservice which has its own embedded H2 database (RDBMS).
* [Forex Exchange] : Is a simple microservice which has its own embbeded data base, where currency conversion-rate values are stored.

### Day 4
* [Spring Boot Service with client]  I wrote another microservice, a simple one though, but communicating with another microservice.

### Day 7
* Well after a gap i started off again, now with intent to finish a basic set of microservices.

A high level diagram below refers to my first project with microservices, idea was picked from [here]. It is not entirely as the referred source describes, but my own version. Basic idea is to have a currency conversion service. This service has two parts 
1) [Forex Exchange] which i build on day 3 (refer above),
    [Forex Exchange] registers to Eureka (Netflix OSS load balancer) as a client.
2) [Conversion Serivce] which is the actual front end service, which could be used to convert one type of currency to another.




  ![Alt text](https://github.com/samair/TheMicroservicesJourney/blob/master/First_Microservice.png)
  
### Day 10
New day new project, upskilling now

![Alt text](https://github.com/samair/TheMicroservicesJourney/blob/master/Bank_Project.png)

### Day 11
Finished writing a simple quote [Quote Service].
Which takes a Stock symbol and returns the current price. 

Next step is to create Account Service, plan is to use elastic serach. Using [this online es example]

### Day 12
Deployed Qoute service in GCE 
User guide to deploy @GCE 
 
[here]: <http://www.springboottutorial.com>
[Spring MVC]:  <https://github.com/samair/spring-mvc.git>
[Forex Exchange]: <https://github.com/samair/Forex-Exchange-service.git>
[Spring Boot Basic]: <https://github.com/samair/springboot.git >
[Conversion Serivce]: <https://github.com/samair/conversionService.git>
[Quote Service]: <https://github.com/samair/Quote-Service.git>
[this online es example]: <https://www.journaldev.com/18148/spring-boot-elasticsearch>
[User guide to deploy @GCE ]: <https://codelabs.developers.google.com/codelabs/cloud-app-engine-springboot/index.html?index=..%2F..index#0>

