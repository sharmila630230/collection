# Spring Framework

**Prerequisites**
Bdsucs
XML, json, REST API, maven, hibernate

**XML**
eXtensible Markup Language
It is mainly compises of data to send between enttities often verry popular.
Known for it's markup format and freedom to create own tags

Uses
- Transfer data
- Configure Framework
- Design

**Json**
Javascript object notation
It is succesor of xml,

It is fromat of sending information from client to server and server to cient.

Server change obj to json
Client json to object

In a way, that both converse.

ex: var emp = {
  eid: "2",
  name:"Vishnu",
  other:[{}, {}] 
  }

  You can have more json objects inside array, which in inside a bigger json object. It is very smooth and comfatrible for data progression.

Both xml and json has struture and schema for content. Preferred over plain text for many reasons.

**Rest API**
A set of rules and protocols that allows different software applications to communicate and exchange data with each other

You are planning to do a startup of weather forecast, You can't possibly put sensors all over the world.

What you can do, is contact the nearest srevors or servlets, which serves same purpose.

They said for some price, they will give info.

To request them, and get response. You need API

While doing the same, REST is standard principle to ensure safe and secure connection following princliples like CRUD(Create, read, Update, Delete)

That return from server might be a direct html webpage, Although we need data not the design.

So we firthur ask to give just dat, They can give in 2 different formats

xml and json, where xml is heiracichal and json is just javascript form of creating array object.

you can prefer json, 

Th reall problem ois the overhead of post, get delete and all these operrations

To counter this, we have REST Api

There are two main menthods of implementsing this
Jersey & Spring

**Maven**
When you start working simple java project that uses spring, which helps make code quicker and clean.
You need dependencies, tehre are re 100's of dependencies to use, when spring version chnages you need to basically reinstall things manually.
This is very frustating and time staking process.

Maven make life easier by auto doing thsi and also provdes a way to store.jar file which is importnat for pject and much more advantages.

Maven is a build automation and project management tool primarily used for Java applications. It simplifies software development by handling dependency management, compiling code, running tests, and packaging the final application, all standardized through a centralized configuration file called pom.xml


# Spring Framework
Learning using _Intellij idea_ 
The program of every order, comprises of 2 things.
- Business Logic
- Object Creation

That second one is real pain, creating managinga nd deleting.
To counter this or help this, Spring will take care of everything.

Thsi concept is also known as IOC(Inversion Of Control)

Dependency Injection, is the technique to implement IOC.

Instead of doing A a = new A(); 
We can inject the object using Spring.

3 ways
- Constructor Injection
- Setter Injection
- Field Injection

**.war** file
It is web archive, which we send to cloud and run on apache Tomcat

But guess what, I don't care

**.jar**
Because i got a jar file that has embedded tomcat.

Go to **start.spring.io** and install a zip file with adding some needed dependencies

**Spring boot** will give some convention libraries that decreas ethe time taken, It is really good. But the drawback is that you don't use that many libraries a in acode.

Objects are created inside **JVM**(Java Virtual Machine)

As we know the job of creating objects is spring's work.
But where it will create, inside jm, but not same as others, It will have sperate container inside jvm(**IOC** Container)  

```java
SpringApplication.run(MyAppApplication.class, args);
```
This above line is responsible for creating IOC Container
<img width="1552" height="375" alt="image" src="https://github.com/user-attachments/assets/a1e9aa3c-6abf-4ab1-9215-d119d6e3aa0b" />
Just mentioning ApllicationContext, getBean and annotation of @Component.
We are telling the Spring framework to create object of that class , manage and delete at your convincence
