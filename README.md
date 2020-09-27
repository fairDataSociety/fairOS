# FairOS

### Introduction

The most important resources in a computer are the storage(disk) and compute(processor). Applications that run on the 
computer use either or both of these resources. Operating System(OS) are programs which manage these resources and also 
schedules their usage across multiple applications.   

### Big Data Frameworks

During the turn of the last century, internet boomed and gave rise to many internet based Applications. This helped
companies to grow on a global scale, which in turn rise to data explosion and these companies started looking for Big
Data Processing frameworks.

It is not trivial to build distributed applications because of several factors. Hardware failures and algorithmic 
consensus are few of the problems that make it complex to build distributed applications. Because of that, several
frameworks have emerged in the past which helped developers build applications that scale out. Most of them require the
applications to be written in different paradigms and demand specific knowledge of the system. It is becaue of this, 
that the investment in writing a distributed application is high.

Some applications are CPU heavy and some are IO heavy. The Big Data Frameworks are tuned to specific types, like batch,
streaming, iterative etc. For this reason, we cannot say that one framework fits all. These frameworks achieve scaling 
out by splitting the task in hand in to several pieces and sending them to be processed by different computers at the 
same time working on differnt piece of the same data. 

In the last copuple of decades, many open source applications started to emerge commoditising Big Data Processing. Some
of famouse ones are Apache Hadoop, Apach Spark and the likes. Today many exterprises use these frameowrks to process
their data. 

![Big Data Framework Blueprint](https://github.com/fairDataSociety/fairOS/blob/master/doc/images/Big%20Data%20Framework.png)

The above diagram shows the basic blueprint of a Big Data Processing Framework. It contains two layers. The lower layer 
binds together the storage of all the computers involved, in to a Distributed File System (Ex: HDFS) and the upper layer
taker care of the programming paradigm required to split the data and process it (ex: MapReduce). They usually have weak
consesus which are non byzantine fault tolerant. 

The issues with this applications are, that following
- They give rise to data silos
- They are not Byzantine fault tolerant
- The data is owned by the organization and not by the user
- External auditing is not possible

### Internet Computer Blueprint

![Internet Computer](https://github.com/fairDataSociety/fairOS/blob/master/doc/images/Internet%20Computer.png)

The above diagram shows a blue print of a Internet Computer which has a Operating System that glues the web3.0 storage
layer with the already existing Big Data Frameworks. This requires that the storage layer is cmopatible with these frameworks
at the same time make the entire system Byzantine fault tolerant by introducing blockchain for consensus.

### What is FairOS

FairOS is a glue that runs web-2.0 Big Data Frameworks(like Hadoop, Spark etc.) on web-3.0 storage systems(Swarm). 
It has 2 layers, namely
- ![FairOs-dfs](https://github.com/fairDataSociety/fairOS-dfs)
- ![FairOs-engine](https://github.com/fairDataSociety/fairOS-engine)

##### FairOS-dfs 
The Decentralsied File System(dfs) is a stateless layer over Swarm. It uses the building blocks provided by Swarm and exposes
high level File system functionalities like
- Logical File system over Swarm
- Data Structures 
- User and Permission Management
- Payments and Charging

##### FairOS-engine
The FairOS engine exposes the dfs to the existing big data fraeworks so that they can use it transperantly. Apart from 
storage abstraction it will also provide resource management and scheduling abstractions to run these frameworks over
the Internet.


### Architecture

![Test Image 4](https://github.com/fairDataSociety/fairOS/blob/master/doc/images/FairOS-Architecture.png)

