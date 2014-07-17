5 Day Java 6 Introduction
----------------------

#Intro
* About this Basics
 * 5 Days - Intro to Java Programming
 * 10am-6pm
 * Lunch at 1:30

* About Me
* About this Class
 * Java is a vast ocean
 * Learning how to find answers is key
* Each Java Topic
 * No Slides
 * Chat and Code Demo - Ask Questions!
 * Do - Pretend I'm the PdM
 * Review Volunteer Together
 * JUnit Tests where feasible
* Final Project (flexible)
* About the Book
* About You
* Questions?


#Learning Objectives

* Get Set Up for JavaSE 6 Development
* Know how to compile, run and debug Java applications
* Know how to create an application from scratch
* Understand the following java topics:
 * Classes and Objects
 * Primitive Data Types
 * Arrays 
 * Collections
 * Loop Structures
 * Returning Values
 * Passing Arguments
 * Branching Structures
 * Exception Handling
 * Basic File Access
 * Stream based IO
* Understand the following Object Oriented Concepts:
 * Abstraction
 * Encapsulation
 * Constructors
 * Static versus Instance
 * Inheritance
 * Polymorphism
* Understand how to use Eclipse IDE for Java
 * Code Short-cuts
 * Formatting Rules
* Understand How To use JDBC to:
 * Connect to a Database
 * Query a Database
* Understand How To use JUnit 4:
 * Test existing code
 * Test First with TDD
 * Code Coverage


#Set up for Java Development
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

* __CHECKPOINT:__ Get Set Up for JavaSE 6 Development

#Java Development Skills
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

* __CHECKPOINT:__ Know how to create an application from scratch

#Java Platform Basics
* JDK - [Java Development Kit](http://en.wikipedia.org/wiki/Java_Development_Kit) (Tools)
* JRE - Java Runtime Environment (JVM + Class Libraries)
* JVM - Java Virtual Machine

#Java Build Tools - Maven
* Generate a template application with Maven (App + AppTest)
 * ``mvn archetype:generate``
* Use Maven to Build and Package a Java Application
* Use Maven to run JUnit Unit Tests for your code
* Import a maven project into Eclipse (Requires: Maven Integration for Eclipse)

#Java Language Skills
##Class Methods (Java Language)
* Understand and use [Class Methods (static) esp. main]
 * No instance needed - We'll get to Instance Methods later
 * ``String[] args``
 * ``System.out.println()``
 * ``public static void`` - Access Modifiers

##Packages (Java Language)
* Understand [Java Packages](http://docs.oracle.com/javase/tutorial/java/package/packages.html) ~ Namespace and Folder Name
* __EXERCISE:__ Move your HelloWorld class to a package using eclipse

##Data Types (Java Language)
* Understand and use [Java Data Types](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/datatypes.html)

##Local Variables (Java Language)
* Understand and use [Local Variables](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/variables.html)
* Variable initialization rules

##Printing Out Values (Java Platform)
* [System.out.printf](http://www.java2s.com/Code/JavaAPI/java.lang/System.out.printf.htm)
* [Formatter](http://docs.oracle.com/javase/6/docs/api/java/util/Formatter.html#syntax)
* [Cheat Sheet](http://alvinalexander.com/programming/printf-format-cheat-sheet)

###Exercise
* __EXERCISE:__ Create a new folder called ``datatypes`` and a main application class called ``DataTypeApp``. Put the ``DataTypeApp`` in an appropriate ``package``. In DataTypeApp.main method, add a local variable of each of the built in data types and print out the values on separate lines, hint: ``%n`` translates to a new line

* __CHECKPOINT:__ Primitive Data Types

##Expressions, Statements and Blocks (Java Language)
* Understand and use [Expressions, Statements and Block](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/expressions.html)
* Expression - evaluates to a value
* Statement - (expression, declaration or control flow)
* Blocks - a group of zero or more statements, hint at scope

##Operators (Java Language)
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

## Comments (Java Language)
* Understand and use Comments rest-of-line, in-line (and javadoc later)

##Random Number Generator Code Sample
This code is used in the next examples, we'll learn what all the pieces do later, for now just use this code in your exercises

```
Random random = new java.util.Random();
int randomIntBetween0and99 = random.nextInt(100);
/*
nextInt(int n)
Returns a pseudorandom, uniformly distributed int value between 0 (inclusive) and the specified value (exclusive), drawn from this random number generator's sequence.
*/
```

##if (Control Flow)
Simplest Control flow if-then

* [if](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/if.html)
* ``else``
* ``else if``
* Recommendation: Always use blocks

###Exercise
* __EXERCISE:__ Write an application which prints HEADS 50% of the time and TAILS 50% of the time to the console and exits

##switch (Control Flow)
* [switch](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/switch.html)
* ``break``
* ``default``

###Exercise
* __EXERCISE:__ Write an application called ``LuckyDay`` which randomly selects a number between 0 and 6 (inclusive) and uses a ``switch`` statement to print out a day of the week in the format "This week, 'Wednesday' is your lucky day!". Where the day of the week printed is determined by the random number (Sunday is 0..Saturday is 6)

* __CHECKPOINT:__ Branching Structures

##Basic Arrays (Java Language)
* Understand [Java Array Usage](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/arrays.html)
* Allocate an array with the literal syntax
* Assign and access individual elements in the array
```
int[] anArray = {
    100, 200, 300,
    400, 500, 600,
    700, 800, 900, 1000
};
```
* ``array.length``
* ``System.arraycopy()``

###Exercise
* __EXERCISE:__ Re-write the ``LuckyDay`` application to use an array

##Arrays and Array
Array Utilities
* [Arrays](http://docs.oracle.com/javase/6/docs/api/java/util/Arrays.html)


##Command Line Arguments (Java Language)
Enough hard coding! Let's read in some arguments

* ``public static void main(String[] args)``
* How can we access args?

###Exercise
* __EXERCISE:__ Write a simple application in ``sorter`` which takes multiple command line arguments, puts them into an array, sorts the array and prints out the sorted array

* __CHECKPOINT:__ Arrays

###Converting Values
* __DEMO:__ Parsing Strings into primitive Types
* __EXERCISE:__ Write a simple application in ``cladder`` which takes two command line arguments, checks that they are present, converts them into double values, multiplies them together and prints out the answer to two decimal places.

##while (Control Flow)
* [while / do-while](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/while.html)

###Exercise
* __EXERCISE:__ Write an application called ``HighRoller`` which utilizes one of these loop types to count the number of dice rolls required to reach ``25``. Each dice roll is a random number between ``1`` and ``6`` inclusive. At the end, print out, the total score and how many rolls it took. If the player rolls exactly ``25`` then print out the special message ``YOU ARE A HIGH ROLLER!!!``

##for (Control Flow)
* [for loop](http://docs.oracle.com/javase/tutorial/java/nutsandbolts/for.html)

```
for(int i=0; i < limit; i++)
{
}

for(;;)
{
  // Runs forever :) and this is a comment
}
```

###Exercise
* __EXERCISE:__ Write an application called ``RandomArrayer``. The application should generate a random number between ``10`` and ``20`` (inclusive). Then allocate a new array of ``int``s. The use a for loop to assign each ``int`` in the array to a random number. Use [java.util.Arrays.sort()](http://docs.oracle.com/javase/6/docs/api/java/util/Arrays.html#sort%28int[]%29) to sort the array of ``int``s in ascending order and then another for loop to print out the numbers to the console

##for each (Control Flow)
* [for each](http://docs.oracle.com/javase/6/docs/technotes/guides/language/foreach.html)

###Exercise
* __EXERCISE:__ Rewrite one of the loops in ``RandomArrayer`` to use the for each loop syntax

##break in loops (Control Flow)
* Shortcut exit loop

##continue in loops (Control Flow)
* Shortcut next iteration

* __CHECKPOINT:__ Loop Structures

#Java Platform Classes
##Strings (Java Platform)
* [String](http://docs.oracle.com/javase/tutorial/java/data/strings.html) is a special case object in that you can use a literal notation ``"my string contents"`` and get an object reference
* [StringBuilder](http://docs.oracle.com/javase/tutorial/java/data/buffers.html)

#More Java Language
##Returning Values (Methods)
* ``return``
* void
* types
* Recommendation: Single Return Statement is preferred

* __CHECKPOINT:__ Returning Values

##Method Names (Methods)
* camelCase beginning with lowercase

##Passing Parameters (Methods)
* Understand argument passing and method invokation
 * Everything is passed by value, the value passed is either a primitive data type or an __object reference__
 * Objects themselves are always stored in the heap, and we only ever have a reference to that space

* __CHECKPOINT:__ Passing Arguments

##Class Methods (Methods)
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


##Instance Methods (Methods)
* If you have an Object Reference to an ``instanceof`` a ``Class`` you can call it's instance methods
* ``String myString = "Contents of String";``
* ``myString.contains(" of ");``
* Explore [``String``](http://docs.oracle.com/javase/6/docs/api/java/lang/String.html)
* How can you change a value of a ``String``?
* __EXERCISE:__ Use ``mvn archetype:generate`` and select ``maven-archetype-quickstart`` to generate and app template. In your ``App`` class write a class method called ``reverseUpperCase`` which takes a ``String`` parameter and uses some instance methods of the String class to return its contents in reversed UPPERCASE as a new ``String``. Call your ``reverseUpperCase`` method 5 times from your main method with some different arguments including "" and print out the results
* __EXERCISE:__ Add a Test!



#TDD - Test Driven Development
* Red / Green / Refactor
* Write Tests before coding or refactoring

##Looking Back at RandomArrayer (TDD)
###Exercise
Use Test Driven Development to help you with these refactoring tasks:
* __EXERCISE:__ Refactor the 'print out array' loop of ``RandomArrayer`` into a separate function - what would be a good return type/value?
* __EXERCISE:__ Refactor the 'sorting' statement ``RandomArrayer`` into a separate function - what would be a good return type/value?

#Self Study
##Java Koans (General)
A Testy way to learn Java....
* [Java Koans](https://github.com/matyb/java-koans)
When you hit something we haven't covered we'll talk about it in class

#More Java Platform
##Java Platform Differences
* Know the difference between [JavaSE and JavaEE](http://docs.oracle.com/javaee/6/firstcup/doc/gkhoy.html)
* [Java Platform Versions](http://javapapers.com/core-java/java-features-and-history/)
* [JavaSE 6 Overview](http://docs.oracle.com/javase/6/docs/technotes/guides/)
* We are only looking at a subset of JavaSE but you should be aware of:
 * [JavaEE](http://docs.oracle.com/javaee/6/firstcup/doc/gcrkq.html)
 * [JavaME vs Android API](http://en.wikipedia.org/wiki/Comparison_of_Java_and_Android_API)
 * [JavaFX](http://www.oracle.com/technetwork/java/javase/overview/javafx-overview-2158620.html)

#Eclipse Skills
##Using Eclipse Effectively (Tools)

* Configure Project Settings
* Select a JRE
* Consistently Format Code
* Clean up!
* Refactor
 * Get/Setter
 * Extract...
* [Eclipse Tips](ECLIPSE.md)
* __CHECKPOINT:__ Code Short-cuts

##Debugging (Tools)

* Run or Debug your code
* Set Debug Breakpoints
* View and edit runtime variable values
* Debug Your Tests

* __CHECKPOINT:__ Know how to compile, run and debug Java applications

##Code Coverage (Tools)
* Install [Eclemma](http://www.eclemma.org/)
* Run your tests with coverage as...
* __CHECKPOINT:__ Code Coverage

##Profiles (Tools)
* Shared Java Formatting Profiles
* Always Format the same way to minimize conflicts
* __CHECKPOINT:__ Formatting Rules

# More Java Platform Classes
##Numbers (Java Platform)
* For the built in numeric primitive data types we have [wrapper types](http://docs.oracle.com/javase/tutorial/java/data/numberclasses.html)

###Exercise
* __EXERCISE:__ Investigate how to convert "1.61803398875" into a double value
* __EXERCISE:__ What is AutoBoxing and Unboxing? Write a method which uses it.

###Review
* [Autoboxing](http://docs.oracle.com/javase/tutorial/java/data/autoboxing.html)

#Object Oriented Coding
##OO Principals in Java
* Understand the following Object Oriented Concepts:
 * Classes
 * Objects
 * Inheritance
 * Abstraction and Encapsulation
 * Constructors, ``new`` and ``super``
 * Static versus Instance
 * Polymorphism
##OO Overview
* [Overview](http://docs.oracle.com/javase/tutorial/java/concepts/index.html)
[What Is an Object?](http://docs.oracle.com/javase/tutorial/java/concepts/object.html)
[What Is a Class?](http://docs.oracle.com/javase/tutorial/java/concepts/class.html)
[What Is Inheritance?](http://docs.oracle.com/javase/tutorial/java/concepts/inheritance.html)
[What Is an Interface?](http://docs.oracle.com/javase/tutorial/java/concepts/interface.html)
[What Is a Package?](http://docs.oracle.com/javase/tutorial/java/concepts/package.html)
[What Is Composition?](http://javarevisited.blogspot.com/2013/06/why-favor-composition-over-inheritance-java-oops-design.html)

##Classes and Objects
If ``Object`` instances are Cookies then ``Class``es are the cookie cutters

* [Overview](http://docs.oracle.com/javase/tutorial/java/javaOO/)
* Class definitions define:
 * How instances must be created and initialized (Constructors, or other creation pattern)
 * What instances can do - behaviour - (their interfaces, instance methods)
 * How they do it - implementation
 * What data they store internally - instance data
 * Who can access what
 * Any Class specific data, constants or behaviours (``static``)

##Inheritance and Classes
###Exercise
* __EXERCISE:__ Group discussion, select and brainstorm on domain
* __LIVE CODE:__ examples of``extends``, ``class``
* __EXERCISE:__ Now on your own in groups of two. Pick a domain and make some notes:
 * Describe Domain (package name)
 * Find Classes (``class``)
 * Find Inheritance (``extends``)
 * Draft up classes on paper
* __DISCUSSION:__ Review of examples


##Writing Your Own Java Classes
##Class Definitions (Java Language)
* One public class per .java file
* Must Match path with package
* Must Match Class name with Filename
* Constructors
 * ``new``
 * ``super``
 * ``this``
* Fields
* Getters and Setters
* Review Class Methods and Class Variables
 * ``static``
* Instance Methods and Instance Variables
 * non-``static``
 
* __EXERCISE:__  Implement the basics of your classes from the previous exercise. 

* __CHECKPOINT:__ Constructors


##Object Equality (Java Language)
* [``equals``](http://docs.oracle.com/javase/7/docs/api/java/lang/Object.html#equals%28java.lang.Object%29) and [``hashCode``](http://docs.oracle.com/javase/7/docs/api/java/lang/Object.html#hashCode%28%29)
* __EXERCISE:__ Write a Java class called ``Employee`` with fields for ``firstName``, ``lastName`` and  . Override ``toString`` in a meaningful way. Now try and implement equals and hashCode according to the documentation provided

* __EXERCISE:__ Write some ``@Test``s for your ``equals`` code

* __DEMO:__ Eclipse Generators

##Dates and Calendars (Java Platform)
* For this exercise [``GregorianCalendar.html#GregorianCalendar(int, int, int)``](http://docs.oracle.com/javase/6/docs/api/java/util/GregorianCalendar.html#GregorianCalendar%28int, int, int%29) might be handy
* __EXERCISE:__ Add ``dateOfBirth`` as ``java.util.Date`` to your Employee Class
* __DISCUSSION:__ GregorianCalendar - Allows you to create dates and Calendar - Date Math
* __EXERCISE:__ Run your tests again from the previous exercise

* __CHECKPOINT:__ Classes and Objects

##Access Modifiers (Java Language)
* [Access Modifiers](http://docs.oracle.com/javase/tutorial/java/javaOO/accesscontrol.html)
* ``public``
* ``private``
* 'package' - The default
* ``protected``

* __EXERCISE:__  Discuss with your partner the appropriate access modifiers for parts of your class system

##More Inheritance in Java (Java Language)
* Understand Class inheritance and how to implement it
 * Overriding
 * Abstract classes and methods
 * Final (classes, methods, variables, parameters)
* Recommendation: use ``final`` where you don't intend a value to change and avoid coding errors

##Interfaces in Java
* Understand Interfaces and how to use them
 * [http://docs.oracle.com/javase/tutorial/java/IandI/index.html](http://docs.oracle.com/javase/tutorial/java/IandI/index.html)
* Understand Abstract Classes and how to define them
* Interfaces are entirely abstract but can contain constants

##Abstraction, Encapsulation and Interfaces
When you turn the steering wheel, the front wheels turn, you don't care how it works
* Use [StringBuilder](http://docs.oracle.com/javase/6/docs/api/java/lang/StringBuilder.html) as an example
* Abstraction (Interface / Observable Behaviour / Exposed)
* Encapsulation (Implementation / Hidden)
* 'The way you use it' is well defined
 * ``interface`` or ``class`` definition
* Clearly defined interfaces allow _Polymorphism..._

* __CHECKPOINT:__ Abstraction
* __CHECKPOINT:__ Encapsulation


##Polymorphism
When you rent a car, it doesn't matter what model it is, you can still drive it
* [Polymorphism](http://docs.oracle.com/javase/tutorial/java/IandI/polymorphism.html)
* Share some common nature but differ in implementation or additional behaviours
 * Interfaces with multiple implementations
 * ``@Override``s of instance methods
 * Implementations of ``abstract`` methods
* [WikiPedia](http://en.wikipedia.org/wiki/Polymorphism_(computer_science))

##The Java Collections Framework and Generics
* [Collections Overview](http://docs.oracle.com/javase/tutorial/collections/)
* Interfaces
 * [Overview](http://docs.oracle.com/javase/tutorial/collections/interfaces/collection.html)
 * [List](http://docs.oracle.com/javase/6/docs/api/java/util/List.html)
 * [Map](http://docs.oracle.com/javase/6/docs/api/java/util/Map.html)
 * [Set](http://docs.oracle.com/javase/6/docs/api/java/util/Set.html)
* Concrete Implementations (Many we'll only cover the basics)
 * [ArrayList](http://docs.oracle.com/javase/6/docs/api/java/util/ArrayList.html)
 * [HashMap](http://docs.oracle.com/javase/6/docs/api/java/util/HashMap.html)
 * [HashSet](http://docs.oracle.com/javase/6/docs/api/java/util/HashSet.html)
 * __NOTE:__ If you want to use your own classes as keys or in unique collections ``hashCode`` and ``equals`` will need to be implemented (later)
* [Generics](http://docs.oracle.com/javase/tutorial/java/generics/) - you may have noticed something new: ``<E>``
* [generics_collections.html](https://thenewcircle.com/static/bookshelf/java_fundamentals_tutorial/generics_collections.html)

* Additional Note: [unmodifiableCollection](http://docs.oracle.com/javase/6/docs/api/java/util/Collections.html#unmodifiableCollection%28java.util.Collection%29)
 * ``UnsupportedOperationException``

* __CHECKPOINT:__ Polymorphism

###Exercise
* __EXERCISE:__ Group discussion on collections
* __EXERCISE:__ Write a java method which generates an ArrayList<Integer> of the Fibonacci series numbers starting with 0 and 1, up to and including the first value which exceeds ``limit`` where ``limit`` is a parameter. Recommendation use __TDD__ and if the problem is unclear, ask your instructor to clarify

* __CHECKPOINT:__ Collections

##Object Basics (Java Objects)
* Every class extends ``Object``
* ``toString`` -> type plus hashCode
* ``getClass()`` -> ``Class``
* ``instanceof``casting - A lot less of it now we have Generic Collections
* ``clone`` - ``Cloneable`` Marker interface
* [``hashCode`` and ``equals`` contract](http://www.ibm.com/developerworks/library/j-jtp05273/)

* __LIVE DEMO:__ Using ``String`` as an example

##Class Class Basics (Java Objects)
* ``Class`` extends ``Object``
* ``getName()`` -> Useful for resources, jdbc drivers and loggers to avoid hard coding
* ``getClassLoader()``
* ``Class.forName()`` -> ``Class``

* __LIVE DEMO:__ Using ``String.getClass`` as an example

##More Class Implementation (Java Objects)
* Constructors Calling Constructors
* __CHECKPOINT:__ Constructors
* Inheritance Review
* Method Overloading 
* __CHECKPOINT:__ Inheritance
* Static vs Instance Review
* __CHECKPOINT:__ Static versus Instance


#More Java Language
##Exceptions (Java Language)
* Understand Java Exceptions
* Help keep code simple and readable
* Invalid Parameters, unexpected conditions, things outside of your control
* Not for control flow
* Checked vs Unchecked
* [How to handle Exceptions](http://docs.oracle.com/javase/tutorial/essential/exceptions/handling.html)
* Understand How and When to Throw exceptions
 *[Throwing Exceptions](http://docs.oracle.com/javase/tutorial/essential/exceptions/throwing.html)
* Declaring Exceptions
 * Checked vs Unchecked Exceptions
* Exception Type Hierarchy
  *  __TODO__ 

###Exercise
* __EXERCISE:__ Catch Exception - Create and catch an [``ArrayIndexOutOfBoundsException.html``](http://docs.oracle.com/javase/6/docs/api/java/lang/ArrayIndexOutOfBoundsException.html)
* __EXERCISE:__ Throw Exception - Example Check for null and throw a NullPointerException, document it

* __CHECKPOINT:__ Exception Handling

#Files
##Files (JavaSE6 Platform)
* [File](http://www.tutorialspoint.com/java/java_file_class.htm)

###Exercise
* __EXERCISE:__ Check File exists, list files in directory, check permissions, delete file

* __CHECKPOINT:__ Basic File Access

#Stream Based IO
##Streams (Java Platform)
* (NOT TO BE CONFUSED WITH Java8 Streams for Functional Programming)
* [Streams IO](http://docs.oracle.com/javase/tutorial/essential/io/streams.html)
 * byte streams
 * character streams
 * Blocking
 * Use ``try`` and ``finally`` to close streams when done
 * Notices that the streams are declared and initialized to ``null`` outside of the ``try`` and ``null`` is tested in the ``finally`` block

##Canonical Example: File Byte Stream (Java Platform)

```
import java.io.FileInputStream;
import java.io.FileOutputStream;
import java.io.IOException;

public class CopyBytes {
    public static void main(String[] args) throws IOException {

        FileInputStream in = null;
        FileOutputStream out = null;

        try {
            in = new FileInputStream("source.jpg");
            out = new FileOutputStream("target.jpg");
            int c;

            while ((c = in.read()) != -1) {
                out.write(c);
            }
        } finally {
            if (in != null) {
                in.close();
            }
            if (out != null) {
                out.close();
            }
        }
    }
}
```

* __EXERCISE:__ Implement a byte based file copy application which takes two paramters on the command line

##Canonical Example: File Character Stream (Java Platform)


```
import java.io.*;

public class CopyFile {
   public static void main(String args[]) throws IOException
   {
      FileReader in = null;
      FileWriter out = null;

      try {
         in = new FileReader("source.txt");
         out = new FileWriter("target.txt");

         int c;
         while ((c = in.read()) != -1) {
            out.write(c);
         }
      }finally {
         if (in != null) {
            in.close();
         }
         if (out != null) {
            out.close();
         }
      }
   }
}
```

* __EXERCISE:__ Implement a character based file copy application which takes two paramters on the command line


##BufferedStreams

* bytes: ``BufferedInputStream`` and ``BufferedOutputStream``
* character: ``BufferedReader`` and ``BufferedWriter``
* ``flush``



* __EXERCISE:__ Implement a character based file copy application which takes two paramters on the command line using ``BufferedReader`` and ``BufferedWriter``



##Appending to a File
* ``new FileWriter("filename", true)``

* __EXERCISE:__ Use your file copy application as a basis for new utility function which takes a text file and converts all the uppercase letters to lowercase and vice versa. All other characters remain unchanged.
* Recommendation: write a utility method which applies the transformation to a given string first, and test it using TestCases. Then use that method in your app.
* @see ``Character.isUpperCase()``

* __CHECKPOINT:__ Stream based IO

#More Java
##Sorting and Searching (Java Platform)
* [Natural Ordering](http://docs.oracle.com/javase/tutorial/collections/interfaces/order.html)
* [Comparator vs Comparable](http://javarevisited.blogspot.com/2011/06/comparator-and-comparable-in-java.html)
* [Arrays Search](http://docs.oracle.com/javase/6/docs/api/java/util/Arrays.html#binarySearch%28T[],%20int,%20int, T,%20java.util.Comparator%29)


##Scope and Shadowing (Java Language)
* Understand variable scope and shadowing - com.skillbox.boxes.scope.ScopeExample
* mXXX, sXXX or other naming conventions can assist in avoiding this

###Exercise
* __EXERCISE:__  Write a sample class that demonstrates variable shadowing and then make a promise to yourself not to do it again!
* __QUESTION:__ What is the scope of the variables declared in a for loop?


##Generics In your Classes (Java Platform)
* [Bounded and Unbounded](http://docs.oracle.com/javase/tutorial/java/generics/bounded.html)

###Exercise
* __EXERCISE:__   Given this Interface:

Save it as _IGenericStack.java_
```
interface GenericStack<T> {
  void push(T obj) throws StackFullException;
  T pop() throws StackEmptyException;
}
```
In separate files define both ``StackEmptyException`` and a working implementation of ``IGenericStack`` called ``GenericStack``. ``GenericStack`` should have a single constructor which takes an ``int`` parameter which is the size of the fixed array to be used to back up the Stack. We are looking for a _LIFO_ : _Last in First Out_ stack.
Before you start coding your implementation, write a JUnit 4 TestCase called ``GenericStackTest`` which Test the behaviour.
Use ``@Test(expected = StackEmptyException.class)`` to annotate some of your tests

##Enums
* ``.values()`` ``for each``
* ``switch``
* ``toString``

##Additional Topics
* [Auto-boxing and Unboxing](http://docs.oracle.com/javase/tutorial/java/data/autoboxing.html)
* [Math](http://docs.oracle.com/javase/tutorial/java/data/beyondmath.html)
* [hashCode and equals](http://docs.oracle.com/javase/6/docs/api/java/lang/Object.html#hashCode) (Use Eclipse)
* [Enumerations](http://docs.oracle.com/javase/6/docs/api/java/util/StringTokenizer.html) (StringTokenizer)

#Developer Skills
##Advanced Debugging
* Debug to a _remote_(local) application using Java Platform Debugger Architecture (JPDA) from Eclipse
 * [agentlib options](http://docs.oracle.com/javase/6/docs/technotes/guides/jpda/conninv.html)

#JDBC
##JDBC Connections (Java Platform)
* Know how to connect your application to a database with JDBC
*
* Know how to execute SQL statements:
 * CREATE TABLE, SELECT, INSERT, UPDATE, DELETE, DROP TABLE
* autoCommit - Basic Transactions
* close ``Connection`` when done (if you opened it)
* [Batching Statements](http://viralpatel.net/blogs/batch-insert-in-java-jdbc/)


##JDBC Project
* A project which reads a CSV File from disk and imports some of the data into a database
* [DataSource](http://docs.oracle.com/javase/6/docs/api/javax/sql/DataSource.html)
* When the file is imported a second time existing records are updated and new records are added
* [OpenCSV](http://viralpatel.net/blogs/java-read-write-csv-file/)
* [Via Maven](http://mvnrepository.com/artifact/net.sf.opencsv/opencsv/2.3)

* __CHECKPOINT:__ Connect to a Database
* __CHECKPOINT:__ Query a Database

#Testing
##JUnit
* Know how to write JUnit test cases to Unit Test Your Code
* [http://www.mkyong.com/tutorials/junit-tutorials/](http://www.mkyong.com/tutorials/junit-tutorials/)
* Pick a Mock Framework
 * [Mockito](http://www.vogella.com/tutorials/Mockito/article.html)

* __CHECKPOINT:__ Test existing code
* __CHECKPOINT:__ Test First with TDD

#Extras
##CSV Parsing
* [opencsv](http://opencsv.sourceforge.net/)
```
		<dependency>
			<groupId>net.sf.opencsv</groupId>
			<artifactId>opencsv</artifactId>
			<version>2.3</version>
		</dependency>
```

##JSON Parsing
* [json.org](http://json.org/java/)
```
		<dependency>
			<groupId>org.json</groupId>
			<artifactId>json</artifactId>
			<version>20140107</version>
			<scope>compile</scope>
		</dependency>
```


##Logging API
* [java.util.logging]()
* ``mLogger = Logger.getLogger(App.class.getName());``
* See boxes/jsonweather

##DbUnit
* Help test your database code with DbUnit
* [Getting Started](http://dbunit.sourceforge.net/howto.html)
* Allows importing of data and schemas easily
```
		<dependency>
			<groupId>org.dbunit</groupId>
			<artifactId>dbunit</artifactId>
			<version>2.5.0</version>
			<scope>test</scope>
		</dependency>
```

##H2 Database
* Simple in memory database very useful for testing!
* ``static final String JDBC_DRIVER = org.h2.Driver.class.getName();``
* ``static final String JDBC_URL = "jdbc:h2:mem:inventory;DB_CLOSE_DELAY=-1";``
```
		<dependency>
			<groupId>com.h2database</groupId>
			<artifactId>h2</artifactId>
			<version>1.4.179</version>
			<scope>test</scope>
		</dependency>
```



##JSON
* [The Object Model API vs The Streaming API](http://www.oracle.com/technetwork/articles/java/json-1973242.html)
* Strings in Switch were only added in java 7 :(


#Final Project
When you have completed all phases you will have a Java Application which performs these tasks (in order):
* Loads _stock_level.csv_ into a inventory system, in a persistent database of your choice
* The order is read from a JSON file (_order.json_)
* An ``Order`` object from the read data
* The ``OrderManager`` ``process``es the order as follows:
 * Tests that the items are in stock in a database by calling the ``InventoryManager``'s ``stockLevel(productId)``
 * If the stock on hand is >= the required quantity for the line item then
   * Decrements the stock level by calling the ``InventoryManager``'s ``decrementStock(productId)``
 * Otherwise it marks the ``LineItem`` as out_of_stock (all or nothing for each line item)
* Once the order and all the line items have been processed:
* The ``Order`` is passed to the ``ReceiptPrinter`` and a nicely formatted reciept is printed (_reciept.txt_)
* Exports _stock_level_updated.csv_ to the file system with the updated stock levels read from the database


##Sample Stock Data
_stock_level.csv_
```
PRODUCT_ID,STOCK_LEVEL
12,3
14,2
13,2
```

##Sample Input
_order.json_
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
_reciept.txt_
```
  Bob Williams (Y18123AS)
  San Francisco (42)
  July 9th, 2014
  ---------------
  $500.00 - SOLD: 1 @ Flat Screen TV
  $399.00 - SOLD: 1 @ Playstation 4
  OUT_OF_STOCK: 4 @ Playstation Controller
  --------------
  Order Total: $899.00
  --------------
  Thank you for your business

```

* Expectations
 * Create a populate a local database with data from a CSV file (_stock_level.csv_)
 * Write Unit Tests for the components
 * Package the Application into Executable Jar File format (Research Required)
 * Takes two command line arguments
   * orderfile - The file to read
   * recieptfile - The file to write
 * Reads in _orderfile_ (_order.json_) JSON File (representing a customer order)
   * Find and use an available Parser
 * Creates Order Related Objects Based on the JSON File Contents
   * Order ? and what else might you need?
 * Writes out _receiptfile_ a nicely formatted receipt describing the order
 * Has JUnit tests
    * Unit tests: for functional Units
    * Try you hand at an integration test
 * Bonus: Using Logging

#Learning Objectives Review
* Get Set Up for JavaSE 6 Development
* Know how to compile, run and debug Java applications
* Know how to create an application from scratch
* Understand the following java topics:
 * Classes and Objects
 * Primitive Data Types
 * Arrays 
 * Collections
 * Loop Structures
 * Returning Values
 * Passing Arguments
 * Branching Structures
 * Exception Handling
 * Basic File Access
 * Stream based IO
* Understand the following Object Oriented Concepts:
 * Abstraction
 * Encapsulation
 * Constructors
 * Static versus Instance
 * Inheritance
 * Polymorphism
* Understand how to use Eclipse IDE for Java
 * Code Short-cuts
 * Formatting Rules
* Understand How To use JDBC to:
 * Connect to a Database
 * Query a Database
* Understand How To use JUnit 4:
 * Test existing code
 * Test First with TDD
 * Code Coverage


##Bonus Topics

##(Bonus)Connect to Oracle
* [Maven?](http://stackoverflow.com/questions/1074869/find-oracle-jdbc-driver-in-maven-repository#1074971)
* [System Dependency](http://stackoverflow.com/questions/1074869/find-oracle-jdbc-driver-in-maven-repository#9779295)
* [Get Drivers](http://www.oracle.com/technetwork/database/features/jdbc/index-091264.html)

##(Bonus)Annotations
* [Writing Annotations](https://code.google.com/p/cliche/source/browse/src/asg/cliche/Command.java)
* [Reading Annotations](https://code.google.com/p/cliche/source/browse/src/asg/cliche/Shell.java#176)

##(Bonus)Reading XML (SAX vs DOM)
* [XML Processing](https://thenewcircle.com/static/bookshelf/java_fundamentals_tutorial/xml_processing.html)

##(Bonus)NumberFormat
* [Jenkov NumberFormat](http://tutorials.jenkov.com/java-internationalization/numberformat.html)

##(Bonus)Regular Expressions
* [Patterns](http://docs.oracle.com/javase/6/docs/api/java/util/regex/Pattern.html)
* [String#matches](http://docs.oracle.com/javase/6/docs/api/java/lang/String.html#matches%28java.lang.String%29)

##(Bonus)BigDecimal
* [BigDecimal](http://docs.oracle.com/javase/6/docs/api/java/math/BigDecimal.html)
* [Usage](http://www.javaworld.com/article/2075315/core-java/make-cents-with-bigdecimal.html)

##(Bonus)Locales i18n
* Demo boxes/externalstrings
* [ResourceBundles](http://tutorials.jenkov.com/java-internationalization/resourcebundle.html)
* [NumberFormat](http://tutorials.jenkov.com/java-internationalization/numberformat.html)
* [DecimalFormat](http://tutorials.jenkov.com/java-internationalization/decimalformat.html)

##(Bonus)Java Thread Locks
* Java Processes
 * ```jps```
* Java Thread Dump
 * ```jstack```
* JConsole
 * ```jconsole```
 * [JConsole](http://docs.oracle.com/javase/6/docs/technotes/guides/management/jconsole.html)
 * Threads -> Detect Deadlock (com/skillbox/boxes/threads/LockerApp)

##(Bonus) Recursion
* Rewrite the Fibonacci Exercise with recursion

##(Bonus)Environment
* [Properties](http://docs.oracle.com/javase/tutorial/essential/environment/properties.html)
* [System Properties](http://docs.oracle.com/javase/tutorial/essential/environment/sysprop.html)

##(Bonus)Serialization
* [Object Streams](http://docs.oracle.com/javase/tutorial/essential/io/objectstreams.html)
* [``Serializable`` Marker interface](http://docs.oracle.com/javase/6/docs/api/java/io/Serializable.html)

##(Bonus)Networking
* [Java HTTP Networking](http://docs.oracle.com/javase/tutorial/networking/)
 * [java.net.HttpURLConnection](http://docs.oracle.com/javase/6/docs/api/java/net/HttpURLConnection.html)

##(Bonus)Web Service
* [Stand-alone Web Service](http://www.ibm.com/developerworks/webservices/tutorials/ws-eclipse-javase1/ws-eclipse-javase1.html)
 * [wsgen](http://docs.oracle.com/javase/6/docs/technotes/tools/share/wsgen.html)
##(Bonus)Web Client
* [Stand-alone Web Client](http://www.ibm.com/developerworks/webservices/tutorials/ws-jse/index.html)
 * [wsimport](http://docs.oracle.com/javase/6/docs/technotes/tools/share/wsimport.html)

##(Bonus)JavaDoc
* [Simple example](https://github.com/stujo/java_boxes/tree/master/docsample)

##(Bonus) Multiple Threads
* Where possible simplify your life by using your custom objects on single threads, otherwise:
* [Concurrency](http://docs.oracle.com/javase/tutorial/essential/concurrency/)
* ``synchronized`` - Ensure only a single thread is active at a given time
* ``notify`` and ``wait``
* When threads are holding the object's monitor (Inside a ``synchronized`` block)...
* [Example](http://www.journaldev.com/1037/java-thread-wait-notify-and-notifyall-example)
* [wait() and notify()](http://stackoverflow.com/questions/2536692/a-simple-scenario-using-wait-and-notify-in-java#2537117)

##(Bonus)Garbage Collection Options
* [Pete Freitag](http://www.petefreitag.com/articles/gctuning/)

##(Bonus)Applets
* [Applets](http://docs.oracle.com/javase/tutorial/deployment/applet/index.html)

##(Bonus) NIO/IO Java 7
* [IO / NIO differences](http://docs.oracle.com/javase/tutorial/essential/io/legacy.html)


