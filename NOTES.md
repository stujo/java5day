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

``$ java -version``

```
java version "1.7.0_60"
Java(TM) SE Runtime Environment (build 1.7.0_60-b19)
Java HotSpot(TM) 64-Bit Server VM (build 24.60-b09, mixed mode)
```

* Verify maven installation

``$ mvn -version``

```
Apache Maven 3.2.1 (ea8b2b07643dbb1b84b6d16e1f08391b666bc1e9; 2014-02-14T09:37:52-08:00)
Maven home: /usr/local/Cellar/maven/3.2.1/libexec
Java version: 1.6.0_65, vendor: Apple Inc.
Java home: /System/Library/Java/JavaVirtualMachines/1.6.0.jdk/Contents/Home
Default locale: en_US, platform encoding: MacRoman
OS name: "mac os x", version: "10.9.3", arch: "x86_64", family: "mac"
```

* Verify GIT installation

```
$ git --version
git version 2.0.0
```

* Verify Eclipse Installation
  * Start Eclipse
  * Go to Preferences -> Java -> Installed JREs
  * Verify that the installed JRE is show in the list 


##Java Development Skills
* Explain the Java Development Workflow
  * ``.java`` File
  * ``javac``
  * Compile-Time ``CLASSPATH``
  * ``.class`` file 
  * ``java``
  * Run-Time ``CLASSPATH``
  * Hello World!
  
* [](http://www.oracle.com/technetwork/topics/newtojava/downloads/index.html)
* Write Hello World java application with no tools (Requires: text editor)

__EXERCISE:__ Create projects folder

```
mkdir projects
cd projects
```

__EXERCISE:__ Create a HelloWorld Java Application

```
cd projects
mkdir scratch
cd scratch/
mkdir src
vi src/HelloWorld.java
```

* ``public static void`` - Access Modifiers
* ``main``
* ``String[] args``
* ``System.out.println()``
* Compile your application (Requires: javac from the JDK) (javac -verbose HelloWorld.java)

```
javac src/HelloWorld.java 
```
* Run your Application (Requires: java from JRE)

```
java -cp ./src HelloWorld
```
* ``-verbose`` option:

```
javac -verbose src/HelloWorld.java 
java -verbose -cp ./src HelloWorld
``` 

* ``-d`` option

* [Intro CLASS_PATH](http://docs.oracle.com/javase/tutorial/essential/environment/paths.html) 

##Java Platform Basics
* JDK - [Java Development Kit](http://en.wikipedia.org/wiki/Java_Development_Kit) (Tools)
* JRE - Java Runtime Environment (JVM + Class Libraries)
* JVM - Java Virtual Machine 

##Java Build Tools - Maven
* Generate a template application with Maven (App + AppTest)
  * ``mvn archetype:generate`` 
* Use Maven to Build and Package a Java Application
* Use Maven to run JUnit Unit Tests for your code
* Import a maven project into Eclipse (Requires: Maven Integration for Eclipse)

##Java Language Skills
###Class Methods
* Understand and use [Class Methods (static) esp. main]
  * No instance needed - We'll get to Instance Methods later
  * ``String[] args``
  * ``System.out.println()``
  * ``public static void`` - Access Modifiers
  
###Packages  
* Understand [Java Packages](http://docs.oracle.com/javase/tutorial/java/package/packages.html) ~ Namespace and Folder Name
* __EXERCISE:__ Move your HelloWorld class to a package using eclipse

###Data Types
* Understand and use [Java Data Types](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)

###Local Variables
* Understand and use [Local Variables](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/variables.html)
* Variable initialization rules

###Printing Out Values
* [System.out.printf](http://www.java2s.com/Code/JavaAPI/java.lang/System.out.printf.htm)
* [Formatter](http://docs.oracle.com/javase/6/docs/api/java/util/Formatter.html#syntax)

####Exercise
* __EXERCISE:__ Create a new folder called ``datatypes`` and a main application class called ``DataTypeApp``. Put the ``DataTypeApp`` in an appropriate ``package``. In DataTypeApp.main method, add a local variable of each of the built in data types and print out the values on separate lines, hint: ``%n`` translates to a new line

###Expressions, Statements and Blocks
* Understand and use [Expressions, Statements and Block](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/expressions.html) 
* Expression - evaluates to a value
* Statement - (expression, declaration or control flow)
* Blocks - a group of zero or more statements, hint at scope

###Operators
Eclipse will show warnings and errors as you type, pay attention to them to learn how to use these operators

* The Arithmetic Operators
* __EXERCISE:__ Create a new folder called ``operators`` with a class called ``OperatorsApp`` in an appropriate package. For each of the Arithmetic operators ``+``,``-``,``/``,``%``,``++``,``--`` write an example usage and print out the results. Ensure that your app describes the difference between prefix and postfix ``--/++``. 

* The Equality and Relational Operators
* __EXERCISE:__ Create a new app any way you wish. In the main method, write an example expression for each of these operators which prints something out:
  * ==      equal to
  * !=      not equal to
  * &gt;       greater than
  * &gt;=      greater than or equal to
  * <       less than
  * <=      less than or equal to
What data type do these expressions return?


###Random Number Generator Code Sample
This code is used in the next examples, we'll learn what all the pieces do later, for now just use this code in your exercises

```
Random random = new java.util.Random();
int randomIntBetween0and99 = random.nextInt(100);
/*
nextInt(int n)
Returns a pseudorandom, uniformly distributed int value between 0 (inclusive) and the specified value (exclusive), drawn from this random number generator's sequence.
*/
```

###Control Flow 
* [if](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/if.html) 

####Exercise
* __EXERCISE:__ Write an application which prints HEADS 50% of the time and TAILS 50% of the time to the console and exits

* [switch](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/switch.html)

####Exercise
* __EXERCISE:__ Write an application called ``LuckyDay`` which randomly selects a number between 0 and 6 (inclusive) and uses a ``switch`` statement to print out a day of the week in the format "This week, 'Wednesday' is your lucky day!". Where the day of the week printed is determined by the random number (Sunday is 0..Saturday is 6) 

###Array Usage
* Understand [Java Array Usage](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html)
* Allocate an array with the literal syntax
* Assign and access individual elements in the array
 
####Exercise
* __EXERCISE:__ Re-write the ``LuckyDay`` application to use an array

##Use Loops
###[while / do-while](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/while.html) 

####Exercise
* __EXERCISE:__ Write an application called ``HighRoller`` which utilizes one of these loop types to count the number of dice rolls required to reach ``25``. Each dice roll is a random number between ``1`` and ``6`` inclusive. At the end, print out, the total score and how many rolls it took. If the player rolls exactly ``25`` then print out the special message ``YOU ARE A HIGH ROLLER!!!``

###[for loop](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/for.html)

####Exercise
* __EXERCISE:__ Write an application called ``RandomArrayer``. The application should generate a random number between ``10`` and ``20`` (inclusive). Then allocate a new array of ``int``s. The use a for loop to assign each ``int`` in the array to a random number. Use [java.util.Arrays.sort()](http://docs.oracle.com/javase/6/docs/api/java/util/Arrays.html#sort%28int[]%29) to sort the array of ``int``s in ascending order and then another for loop to print out the numbers to the console
  
###[for each](http://docs.oracle.com/javase/6/docs/technotes/guides/language/foreach.html)

####Exercise
* __EXERCISE:__ Rewrite one of the loops in e``RandomArrayer`` to use the for each loop syntax

###Strings (Java Objects)
* [String](http://docs.oracle.com/javase/tutorial/java/data/strings.html) is a special case object in that you can use a literal notation ``"my string contents"`` and get an object reference

###Review Calling Methods
####Returning Values
* ``return`` 
* void
* types
* Single Return Statement is preferred

####Method Names
* camelCase beginning with lowercase

####Passing Parameters
* Understand argument passing and method invokation
  * Everything is passed by value, the value passed is either a primitive data type or an __object reference__
  * Objects themselves are always stored in the heap, and we only ever have a reference to that space
 
####Class Methods
* You don't need to create an instance to call ``Class`` (static) methods
* The instance of the ``Class`` is created when the bytecode is loaded by the ``ClassLoader``
* ``Math.min(a,b);``
* Our app is started when ``main`` is called
* Explore [``Math``](http://docs.oracle.com/javase/6/docs/api/java/lang/Math.html)
* __EXERCISE:__ Use ``mvn archetype:generate`` and select ``maven-archetype-quickstart`` to generate and app template. In your ``App`` class use a loop and the Math library to print out a table with the radius, the area and the circumference of 10 circles with each radius between  ``1`` and ``10`` units. Instead of printing the values out directly, write a ``class`` method called ``getCircleInfo()`` on your application class which takes an ``array`` of radii (type ``double[n]``) and returns a 2 dimensional array ``double[n][3]``, where in each row of the array the 0th element contains the radius, 1st the area, 2nd the circumference.
* __EXERCISE:__ Replace the AppTest generated by the template with this AppTest Class to your Application. Try it out, by running the tests as a JUnit 4 Unit Test Case in eclipse. (The archetype template uses JUnit 3 syntax, so we are upgrading!)

```
package com.skillbox.boxes.circles; 
// You'll need to change this package declaration, eclipse will help!

import static org.junit.Assert.*;
import org.junit.Test;

public class AppTest {
	@Test
	public void testCirclrInfoResultLength() {
		double[] radii = { 1, 2, 3, 4 };
		assertEquals(radii.length, CircleApp.getCircleInfo(radii).length);
	}
}
```


####Instance Methods
* If you have an Object Reference to an ``instanceof`` a ``Class`` you can call it's instance methods
* ``String myString = "Contents of String";``
* ``myString.contains(" of ");``
* Explore [``String``](http://docs.oracle.com/javase/6/docs/api/java/lang/String.html)
* How can you change a value of a ``String``?
* __EXERCISE:__ Use ``mvn archetype:generate`` and select ``maven-archetype-quickstart`` to generate and app template. In your ``App`` class write a class method called ``reverseUpperCase`` which takes a ``String`` parameter and uses some instance methods of the String class to return its contents in reversed UPPERCASE as a new ``String``. Call your ``reverseUpperCase`` method 5 times from your main method with some different arguments including "" and print out the results
* __EXERCISE:__ Add a Test!

###TDD - Test Driven Development
* Red / Green / Refactor
* Write Tests before coding or refactoring

###Looking Back at RandomArrayer with TDD
####Exercise
Use Test Driven Development to help you with these refactoring tasks:
* __EXERCISE:__ Refactor the 'print out array' loop of ``RandomArrayer`` into a separate function - what would be a good return type/value?
* __EXERCISE:__ Refactor the 'sorting' statement ``RandomArrayer`` into a separate function - what would be a good return type/value?

##Java Koans
A Testy way to learn Java....
* [Java Koans](https://github.com/matyb/java-koans)     
When you hit something we haven't covered we'll talk about it in class

-----------

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
  * Select a JRE
  * Consistently Format Code
  * Clean up!
  * Refactor
    * Get/Setter
    * Extract...  
  * [Tips](ECLIPSE.md)
* Debugging
  * Run or Debug your code
  * Set Debug Breakpoints
  * View and edit runtime variable values
  * Debug Your Tests
* Code Coverage
  * Install [Eclemma](http://www.eclemma.org/) 
  * Run your tests with coverage as...
* Profiles
  * Shared Java Formatting Profiles 
  * Always Format the same way to minimize conflicts
  
   
##OO Principals in Platform Libraries
###OO Overview
* [Overview](http://docs.oracle.com/javase/tutorial/java/concepts/index.html)
[What Is an Object?](http://docs.oracle.com/javase/tutorial/java/concepts/object.html)
[What Is a Class?](http://docs.oracle.com/javase/tutorial/java/concepts/class.html)
[What Is Inheritance?](http://docs.oracle.com/javase/tutorial/java/concepts/inheritance.html)
[What Is an Interface?](http://docs.oracle.com/javase/tutorial/java/concepts/interface.html)
[What Is a Package?](http://docs.oracle.com/javase/tutorial/java/concepts/package.html)
[What Is Composition?](http://javarevisited.blogspot.com/2013/06/why-favor-composition-over-inheritance-java-oops-design.html)
###OO In the Java Platform
* Encapsulation (StringBuffer)
* The Java 6 Collection Types
* Polymorphism (Streams)
 
----------------

###Numbers (Java Objects)
* For the built in numeric primitive data types we have [wrapper types](http://docs.oracle.com/javase/tutorial/java/data/numberclasses.html)
* Understand and use [Object References](http://docs.oracle.com/javase/tutorial/java/data/index.html)
* ``getClass()``
* ``instancef of``
####Exercise
* __EXERCISE:__ 



* Know how to instantiate and use other Java Objects such as [StringBuffer]


---------------


* Understand and use Comments rest-of-line, in-line (and javadoc later)

* Understand Java Exceptions and [How to handle Exceptions](http://docs.oracle.com/javase/tutorial/essential/exceptions/handling.html)

* Understand and Use [Streams IO](http://docs.oracle.com/javase/tutorial/essential/io/streams.html)

* Understand and Use [Java 6 File IO](http://www.mkyong.com/tutorials/java-io-tutorials/)
    
      
   
##Writing Your Own Java Classes   
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

##Scope
* Understand variable scope and shadowing - com.skillbox.boxes.scope.ScopeExample
  
##Arrays and Array
* [Arrays](http://docs.oracle.com/javase/6/docs/api/java/util/Arrays.html)
  
##The Java Collections Framework and Generics
* [Collections Overview](http://docs.oracle.com/javase/tutorial/collections/)
* [generics_collections.html](https://thenewcircle.com/static/bookshelf/java_fundamentals_tutorial/generics_collections.html)
* Using Generics in your own classes
  * [Bounded and Unbounded](http://docs.oracle.com/javase/tutorial/java/generics/bounded.html)


##Throwing Exceptions
* Understand How and When to Throw exceptions
  *[Throwing Exceptions](http://docs.oracle.com/javase/tutorial/essential/exceptions/throwing.html) 
  * Checked vs Unchecked Exceptions 
  
  
##Additional Topics
* [Auto-boxing and Unboxing](http://docs.oracle.com/javase/tutorial/java/data/autoboxing.html)
* [Math](http://docs.oracle.com/javase/tutorial/java/data/beyondmath.html)
* [hashCode and equals](http://docs.oracle.com/javase/6/docs/api/java/lang/Object.html#hashCode) (Use Eclipse)
* [Enumerations](http://docs.oracle.com/javase/6/docs/api/java/util/StringTokenizer.html) (StringTokenizer)

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
* [DataSource](http://docs.oracle.com/javase/6/docs/api/javax/sql/DataSource.html)
* When the file is imported a second time existing records are updated and new records are added
* [OpenCSV](http://viralpatel.net/blogs/java-read-write-csv-file/)
* [Via Maven](http://mvnrepository.com/artifact/net.sf.opencsv/opencsv/2.3)

##(Bonus)JUnit
* Know how to write JUnit test cases to Unit Test Your Code   
* Pick a Mock Framework  

##(Bonus)JSON
* [The Object Model API vs The Streaming API](http://www.oracle.com/technetwork/articles/java/json-1973242.html)
* Strings in Switch were only added in java 7 :(

##(BOnus)Networking
* [Java HTTP Networking](http://docs.oracle.com/javase/tutorial/networking/)
  * [java.net.HttpURLConnection](http://docs.oracle.com/javase/6/docs/api/java/net/HttpURLConnection.html)

##(Bonus)Locale

##(Bonus)Logging API
* See boxes/jsonweather

##(Bonus)Annotations
* [Writing Annotations](https://code.google.com/p/cliche/source/browse/src/asg/cliche/Command.java) and [Reading Annotations](https://code.google.com/p/cliche/source/browse/src/asg/cliche/Shell.java#176)

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

##(Bonus) NIO/IO Java 7
* [IO / NIO differences](http://docs.oracle.com/javase/tutorial/essential/io/legacy.html)

##(Bonus)Regular Expressions
* [Patterns](http://docs.oracle.com/javase/6/docs/api/java/util/regex/Pattern.html)
* [String#matches](http://docs.oracle.com/javase/6/docs/api/java/lang/String.html#matches%28java.lang.String%29)

##(Bonus)BigDecimal
* [BigDecimal](http://docs.oracle.com/javase/6/docs/api/java/math/BigDecimal.html)
* [Usage](http://www.javaworld.com/article/2075315/core-java/make-cents-with-bigdecimal.html)

##(Bonus)Locale

#Final Project
When you have completed all phases you will have a Java Application which performs these tasks (in order):
* The order is read from a JSON file
* An ``Order`` object from the read data 
* The ``OrderManager`` ``process``es the order as follows:
  * Tests that the items are in stock in a database by calling the ``InventoryManager``'s ``stockLevel(productId)`` 
  * If the stock on hand is >= the required quantity for the line item then
    * Decrements the stock level by calling the ``InventoryManager``'s ``decrementStock(productId)`` 
  * Otherwise it marks the ``LineItem`` as out_of_stock  
* Once the order and all the line items have been processed:
* The ``Order`` is passed to the ``ReceiptPrinter`` and a nicely formatted reciept is printed

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
  * Test Phase 1: How could we test this? - Class discussion - Suggestion create a ``generateReceipt`` method  which takes an ``InputStream`` and an ``OutputStream`` performs the task and write a test for that
  
  * Phase 2: Update the app to write the contents of the input file to a hard coded receipt file
  * Test Phase 2: How could we test this? - Class discussion
  
  * Phase 3: Update the app to extract the file names from the command line invokeation and display an usage / error message if the usage is incorrect
  * Test Phase 3: How could we test this? - Suggestion: Refactor code into a ``CommandLineParser`` to populate a ``JobConfigurationBean`` with ``orderFilename`` and ``recieptFilename`` and write tests for that.
  
  * Phase 4: Update the app to display error messages if the relevant files cannot be written or read
  * Test Phase 4: How could we test this? - Suggestion: Code a  ``Logger`` interface and ``SimpleLogger`` class implementation that writes to STDOUT or STDERR. Refactor ``generateReceipt`` to get the logger to use from teh ``JobConfigurationBean`` and write tests which invoke ``generateReceipt`` with various ``JobConfigurationBean`` 
  
  * Phase 5: Update the app to parse the JSON into ``org.json.JSONObject``s and output the results for toString on these objects to the output file
  * Test Phase 5: How can we test this? - Suggestion: Refactor code into a ``OrderFileParser`` which has the single responsibility of converting a json text ``InputStream`` into ``JSONObject``s.
  
  * Phase 6: Create JavaBean Classes to represent each of ``Order``, ``Customer``, ``StoreInfo``, ``LineItem``, ``Product``
  * Test Phase 6: How can we test this? - Suggestion: Write tests for the to ensure they have working getters and setters for all the fields we want to read from the JSON. For example ``Order`` should have fields for ``customer``, ``storeInfo``, ``lineItems``. ``LineItem`` should have ``product`` and ``quantity``
  
  * Phase 7: Create an ``OrderFactory`` with a method which takes a populated  ``JSONObject`` as a parameter and returns a correctly populated instance of the ``Order`` JavaBean defined in the previous phase. The JSON objects in the sample file 
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
