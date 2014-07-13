5 Day Java 6 Introduction
----------------------

#Learning Objectives
##Set up for Java Development
* Install the JavaSE (JDK 1.6 or 1.7)
  * [Download](http://www.oracle.com/technetwork/java/javasebusiness/downloads/java-archive-downloads-javase6-419409.html#jdk-6u45-oth-JPR)

* Install Eclipse for Java Developers
  * [Download](https://eclipse.org/downloads/packages/eclipse-ide-java-developers/lunar)

* Install Maven
  * [Instructions](http://maven.apache.org/guides/getting-started/windows-prerequisites.html)
  * [Download](http://maven.apache.org/download.cgi#Maven_3.2.2)

* Install GIT
  * [Download](http://git-scm.com/download)

* Verify java installation
```$ java -version```
```java version "1.7.0_60"
Java(TM) SE Runtime Environment (build 1.7.0_60-b19)
Java HotSpot(TM) 64-Bit Server VM (build 24.60-b09, mixed mode)
``

* Verify maven installation
```$ mvn -version```
```Apache Maven 3.2.1 (ea8b2b07643dbb1b84b6d16e1f08391b666bc1e9; 2014-02-14T09:37:52-08:00)
Maven home: /usr/local/Cellar/maven/3.2.1/libexec
Java version: 1.6.0_65, vendor: Apple Inc.
Java home: /System/Library/Java/JavaVirtualMachines/1.6.0.jdk/Contents/Home
Default locale: en_US, platform encoding: MacRoman
OS name: "mac os x", version: "10.9.3", arch: "x86_64", family: "mac"
```
* Verify GIT installation
```$ git --version```
```git version 2.0.0```

* Verify Eclipse Installation
  * Start Eclipse
  * Go to Preferences -> Java -> Installed JREs
  * Verify that the installed JRE is show in the list 


##Java Development Skills
* Explain the Java Development Workflow
* [](http://www.oracle.com/technetwork/topics/newtojava/downloads/index.html)
* Write Hello World java application with no tools (Requires: text editor)
```
mkdir scratch
cd scratch/
mkdir src
vi src/HelloWorld.java
```
* Compile your application (Requires: javac from the JDK) (javac -verbose HelloWorld.java)
```
javac src/HelloWorld.java 
```
* Run your Application (Requires: java from JRE)
```
java -cp ./src HelloWorld
```
* -verbose option:
```
javac -verbose src/HelloWorld.java 
java -verbose -cp ./src HelloWorld
``` 
* [PATH and CLASS_PATH](http://docs.oracle.com/javase/tutorial/essential/environment/paths.html) 


##Java Platform Basics
* JDK - [Java Development Kit](http://en.wikipedia.org/wiki/Java_Development_Kit) (Tools)
* JRE - Java Runtime Environment (JVM + Class Libraries)
* JVM - Java Virtual Machine 

##Java Build Tools - Maven
* Generate a template application with Maven (App + AppTest)
* Use Maven to Build and Package a Java Application
* Use Maven to run JUnit Unit Tests for your code
* Import a maven project into Eclipse (Requires: Maven Integration for Eclipse)
* Know how to use Eclipse to develop Java Applications

##Java Language Skills
* Understand and use [Expressions, Statements and Block](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/expressions.html)  
* Understand and use [Class Methods (static)]
* Understand and use [Java Data Types](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)
* Understand and use [Object References](http://docs.oracle.com/javase/tutorial/java/data/index.html)
* Understand and use Comments rest-of-line, in-line and javadoc
* Understand and use [Local Variables](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/variables.html)
* Understand [Java Array](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html) behaviour
* Know how to instantiate and use Java Objects such as [String](http://docs.oracle.com/javase/tutorial/java/data/strings.html)
* Control Flow [if](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/if.html) and [switch](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/switch.html)
* Loops [while / do-while](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/while.html) and [for](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/for.html)
* Understand Java Exceptions and [How to handle Exceptions](http://docs.oracle.com/javase/tutorial/essential/exceptions/handling.html)
* Understand argument passing and method invokation
  * Everything is passed by value, the value passed is either a primitive data type or an __object reference__
  * Objects themselves are always stored in the heap, and we only ever have a reference to that space
* Understand and Use [Streams IO](http://docs.oracle.com/javase/tutorial/essential/io/streams.html)
* Understand and Use [Java 6 File IO](http://www.mkyong.com/tutorials/java-io-tutorials/)
    

##Java Platform Differences
* Know the difference between [JavaSE and JavaEE](http://docs.oracle.com/javaee/6/firstcup/doc/gkhoy.html)
* [Java Platform Versions](http://javapapers.com/core-java/java-features-and-history/)
* [JavaSE 6 Overview](http://docs.oracle.com/javase/6/docs/technotes/guides/)
* We are only looking at a subset of JavaSE but you should be aware of:
  * [JavaEE](http://docs.oracle.com/javaee/6/firstcup/doc/gcrkq.html)
  * [JavaME vs Android API](http://en.wikipedia.org/wiki/Comparison_of_Java_and_Android_API)
  * [JavaFX](http://www.oracle.com/technetwork/java/javase/overview/javafx-overview-2158620.html)
 
##Eclipse Skills 
* Know to use Eclipse effectively, including how to:
  * Configure Project Settings
  * Consistently Format Code
  * Run or Debug your code
  * Set Debug Breakpoints
  * View and edit runtime variable values
  
##OO Principals in Platform Libraries
* Understand some Object Oriented Principles wrt built in Classes
  * [http://docs.oracle.com/javase/tutorial/java/concepts/index.html](http://docs.oracle.com/javase/tutorial/java/concepts/index.html)
  * Understand Encapsulation (StringBuffer)
  * Understand and use the Java 6 Collection Types
  * Understand Polymorphism (Streams)
  
   
##Writing YOur Own Java Classes   
* Know how to write Java Classes
  * Constructors
    * super
    * this
  * Class Methods
    * static
  * Instance Methods
  * Java Access Modifiers
 
##Class Inheritance in Java 
* Understand Class inheritance and how to implement it
  * Overriding
  * Abstract
  * Final (classes, methods, variables, parameters)
  * Final Classes

##Interfaces in Java  
* Understand Interfaces and how to use them
  * [http://docs.oracle.com/javase/tutorial/java/IandI/index.html](http://docs.oracle.com/javase/tutorial/java/IandI/index.html) 
* Understand Abstract Classes and how to define them

##Throwing Exceptions
* Understand How and When to Throw exceptions
  *[Throwing Exceptions](http://docs.oracle.com/javase/tutorial/essential/exceptions/throwing.html) 
  * Checked vs Unchecked Exceptions 
  
##The Java Collections Framework and Generics
* [Collections Overview](http://docs.oracle.com/javase/tutorial/collections/)
* [generics_collections.html](https://thenewcircle.com/static/bookshelf/java_fundamentals_tutorial/generics_collections.html)
* Using Generics in your own classes
  * [Bounded and Unbounded](http://docs.oracle.com/javase/tutorial/java/generics/bounded.html)

##Topics
* [IO / NIO differences](http://docs.oracle.com/javase/tutorial/essential/io/legacy.html)
* [Auto-boxing and Unboxing](http://docs.oracle.com/javase/tutorial/java/data/autoboxing.html)
* [Writing Annotations](https://code.google.com/p/cliche/source/browse/src/asg/cliche/Command.java) and [Reading Annotations](https://code.google.com/p/cliche/source/browse/src/asg/cliche/Shell.java#176)
* [Math](http://docs.oracle.com/javase/tutorial/java/data/beyondmath.html)
* [hashCode and equals](http://docs.oracle.com/javase/6/docs/api/java/lang/Object.html#hashCode) (Use Eclipse)
* [Enumerations](http://docs.oracle.com/javase/6/docs/api/java/util/StringTokenizer.html) (StringTokenizer)
* [Java HTTP Networking](http://docs.oracle.com/javase/tutorial/networking/)
  * [java.net.HttpURLConnection](http://docs.oracle.com/javase/6/docs/api/java/net/HttpURLConnection.html)

##Advanced Debugging
* Debug to a _remote_(local) application using Java Platform Debugger Architecture (JPDA) from Eclipse
  * [agentlib options](http://docs.oracle.com/javase/6/docs/technotes/guides/jpda/conninv.html)

##JDBC
* Know how to connect your application to a database with JDBC
* Know how to execute SQL statements: 
  * CREATE TABLE, SELECT, INSERT, UPDATE, DELETE, DROP TABLE
* autoCommit - Basic Transactions
* [Batching Statements](http://viralpatel.net/blogs/batch-insert-in-java-jdbc/)  

  
###JDBC Project
* A project which reads a CSV File from disk and imports some of the data into a database
* When the file is imported a second time existing records are updated and new records are added

##(Bonus)CSV Files
* [OpenCSV](http://viralpatel.net/blogs/java-read-write-csv-file/)
* [Via Maven](http://mvnrepository.com/artifact/net.sf.opencsv/opencsv/2.3)

##(Bonus)JUnit
* Know how to write JUnit test cases to Unit Test Your Code   
* Pick a Mock Framework  

##(Bonus)JSON
* [The Object Model API vs The Streaming API](http://www.oracle.com/technetwork/articles/java/json-1973242.html)
* Strings in Switch were only added in java 7 :(

##(Bonus)Logging API
* See boxes/jsonweather

##(Bonus)Java Thread Locks
* Java Processes
  * ```jps```
* Java Thread Dump
  * ```jstack```
* JConsole
  * ```jconsole```
  * [JConsole](http://docs.oracle.com/javase/6/docs/technotes/guides/management/jconsole.html)
  * Threads -> Detect Deadlock (com/skillbox/boxes/threads/LockerApp)

##(Bonus)Reading XML (SAX vs DOM)
* [XML Processing](https://thenewcircle.com/static/bookshelf/java_fundamentals_tutorial/xml_processing.html)

##(Bonus)Garbage Collection OPtions
* [Pete Freitag](http://www.petefreitag.com/articles/gctuning/)

##(Bonus)JavaDoc
* [Simple example](https://github.com/stujo/java_boxes/tree/master/docsample)

##(Bonus)Applets
* [Applets](http://docs.oracle.com/javase/tutorial/deployment/applet/index.html)

##(Bonus)Environment
* [Properties](http://docs.oracle.com/javase/tutorial/essential/environment/properties.html)
* [System Properties](http://docs.oracle.com/javase/tutorial/essential/environment/sysprop.html)

#Final Project
When you have completed all phases you will have a Java Application which performs these tasks (in order):
* The order is read from a JSON file
* An ```Order``` object from the read data 
* The ```OrderManager``` ```process```es the order as follows:
  * Tests that the items are in stock in a database by calling the ```InventoryManager```'s ```stockLevel(productId)``` 
  * If the stock on hand is >= the required quantity for the line item then
    * Decrements the stock level by calling the ```InventoryManager```'s ```decrementStock(productId)``` 
  * Otherwise it marks the ```LineItem``` as out_of_stock  
* Once the order and all the line items have been processed:
* The ```Order``` is passed to the ```ReceiptPrinter``` and a nicely formatted reciept is printed

##Sample Input
```
{
"timestamp":"20140709194738",
"store":{"id":"42", "name":"San Francisco" },
"customer":{ "first_name":"Bob", "last_name":"Williams", "rewards_number":"Y18123AS"},
"items":[
  { "id":"12", "name":"Flat Screen TV", "price":500, "quantity":1 },
  { "id":"14", "name":"Playstation 4", "price":399, "quantity":1 },
  { "id":"13", "name":"Playstation Controller", "price":29, "quantity":4 }
]
}
```

##Sample Output
```
Bob Williams (Y18123AS)
San Francisco (42)
July 9th, 2014
 ----------------


```




##Final Project Breakdown (Phases)
  * Phase 1: Read in a hardcoded JSON file (as text) and output the raw contents to STDOUT
  * Test Phase 1: How could we test this? - Class discussion - Suggestion create a ```generateReceipt``` method  which takes an ```InputStream``` and an ```OutputStream``` performs the task and write a test for that
  
  * Phase 2: Update the app to write the contents of the input file to a hard coded receipt file
  * Test Phase 2: How could we test this? - Class discussion
  
  * Phase 3: Update the app to extract the file names from the command line invokeation and display an usage / error message if the usage is incorrect
  * Test Phase 3: How could we test this? - Suggestion: Refactor code into a ```CommandLineParser``` to populate a ```JobConfigurationBean``` with ```orderFilename``` and ```recieptFilename``` and write tests for that.
  
  * Phase 4: Update the app to display error messages if the relevant files cannot be written or read
  * Test Phase 4: How could we test this? - Suggestion: Code a  ```Logger``` interface and `SimpleLogger` class implementation that writes to STDOUT or STDERR. Refactor ```generateReceipt``` to get the logger to use from teh ```JobConfigurationBean``` and write tests which invoke ```generateReceipt``` with various ```JobConfigurationBean``` 
  
  * Phase 5: Update the app to parse the JSON into ```org.json.JSONObject```s and output the results for toString on these objects to the output file
  * Test Phase 5: How can we test this? - Suggestion: Refactor code into a ```OrderFileParser``` which has the single responsibility of converting a json text ```InputStream``` into ```JSONObject```s.
  
  * Phase 6: Create JavaBean Classes to represent each of ```Order```, ```Customer```, ```StoreInfo```, ```LineItem```, ```Product```
  * Test Phase 6: How can we test this? - Suggestion: Write tests for the to ensure they have working getters and setters for all the fields we want to read from the JSON. For example ```Order``` should have fields for ```customer```, ```storeInfo```, ```lineItems```. ```LineItem``` should have ```product``` and ```quantity```
  
  * Phase 7: Create an ```OrderFactory``` with a method which takes a populated  ```JSONObject``` as a parameter and returns a correctly populated instance of the ```Order``` JavaBean defined in the previous phase. The JSON objects in the sample file 
  * Test Phase 7: How can we test this?
  




* Expectations
  * Create a populate a local database with data from a CSV file
  * Write Unit Tests for the components
  * Package the Application into Executable Jar File format

  * Takes two command line arguments
    * orderfile - The file to read
    * recieptfile - The file to write 
  * Reads in _orderfile_ a  customer_order.json JSON File (representing a customer order)
    * Find and use an available Parser
  * Creates Order Related Objects Based on the JSON File Contents
    * Order 
      * Customer
      * StoreInfo 
      * LineItem Array
        * Product 
        * Quantity
    * Create an Object Factory (based on _Type_ from JSON)
    * Loads StoreInfo data from the database
    * Loads Product data from 
  * Writes out _receiptfile_ a nicely formatted receipt describing the order
  * Has JUnit tests for
     * 
     






 
  


#Topics
* Introducing Java

* Java Development Tools Overview

* Your First Java Application

* Classes and Objects

* Data Types

* Arrays and Collections

* Looping Structures

* Returning Values and Passing Arguments

* Branching Structures

* Code Short-cuts and Formatting Rules

* Encapsulation

* Constructors

* Static versus Instance

* Inheritance

* Polymorphism

* Abstraction (Interfaces)

* Exception Handling

* Streams

* Java and Databases, Introduction to JDBC

* 



#Bonus Topics
* [Stand-alone Web Service](http://www.ibm.com/developerworks/webservices/tutorials/ws-eclipse-javase1/ws-eclipse-javase1.html)
  * [wsgen](http://docs.oracle.com/javase/6/docs/technotes/tools/share/wsgen.html) 
* [Stand-alone Web Client](http://www.ibm.com/developerworks/webservices/tutorials/ws-jse/index.html)
  * [wsimport](http://docs.oracle.com/javase/6/docs/technotes/tools/share/wsimport.html) 
* Java Threads
* XML Parsing
 


#Not Including
* Concurrent
* GUIs, awt, swing
* Applets
