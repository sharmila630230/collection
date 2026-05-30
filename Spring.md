# Spring Framework

**Prerequisites**
Bdsucs
XML, json, REST API, maven, gradle, hibernate

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
