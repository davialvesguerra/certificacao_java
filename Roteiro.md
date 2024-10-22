Iniciando o tutorial com o primeiro tópico abordado na ementa:

## Java Basics

### links alura
- [Java Basicos](https://unibb.alura.com.br/course/java-primeiros-passos)

## What is Java


1) Características do Java

- [Características do Java] (https://www.javatpoint.com/features-of-java)

Abaixo cabe destacar algumas das características da linguagem Java:

 - Programação orientada a objetos: Java é uma linguagem orientada a objetos.  Everything in Java is an object. Object-oriented means we organize our software as a combination of different types of objects that incorporate both data and behavior.
 - Plataforma Independente:  One of Java’s most significant advantages is its platform independence. Java programs are compiled into bytecode, which can run on any device equipped with a Java Virtual Machine (JVM). 
 - Secure: Java provides a secure environment for developing applications. It includes features like bytecode verification, secure class loading, and a security manager to protect against unauthorized access and threats
 - Robustez:  Java is known for its reliability. It has strong memory management, exception handling, and type checking mechanisms that help prevent errors and crashes. Java provides automatic garbage collection which runs on the Java Virtual Machine to get rid of objects which are not being used by a Java application anymore.


2) Aplicações do mundo real
- [Aplicações do Java no mundo real]()

text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text text

 - Enterprise Software Development
 - Android Application Development
 - Scientific and Data Analysis Applications
 - Internet of Things (IoT) Development
 - Financial Applications
 - E-commerce Platforms
 - Gaming
 - Educational Applications
 - Telecommunications
 - Cloud Computing
 
Java EE (Enterprise edition)

https://www.alura.com.br/apostila-java-web/o-que-e-java-ee?srsltid=AfmBOopwF-sN-6lSsxOiVjNtlQmgNMwDrb2_w2dzdTT-snwO8BZEe8l0



## Java Basics

### 1) JDK and JRE

<h4> Java Development Kit (JDK) </h4>

The JDK is a comprehensive suite of tools for Java developers. It includes everything needed to write, compile, and debug Java applications. Here are some key components:

- Java Compiler (javac): Converts Java source code into bytecode.
- Java Debugger (jdb): Helps in debugging Java programs.
- Java Runtime Environment (JRE): Included within the JDK, it allows you to run Java applications.
- Development Tools: Various tools for monitoring, profiling, and managing Java applications12.

<h4>Java Runtime Environment (JRE)</h4>
The JRE is a subset of the JDK and is focused solely on running Java applications. It includes:

- Java Virtual Machine (JVM): Executes Java bytecode.
- Core Libraries: Essential libraries required for running Java applications.
- Other Components: Such as Java Plug-in for running applets in browsers34.

In summary, the JDK is essential for Java development, providing tools for writing and testing code, while the JRE is necessary for running Java applications on your system.

### 2) Describe the components of object-oriented programming

#### Encapsulation

Encapsulation is the concept of wrapping data (variables) and methods (functions) that operate on the data into a single unit, known as a class. It helps in protecting the data from outside interference and misuse. In Java, encapsulation is achieved using access modifiers like private, protected, and public.

#### Inheritance

Inheritance allows a new class to inherit properties and behaviors (methods) from an existing class. The new class, called the subclass or derived class, can use and extend the features of the parent class. This promotes code reusability. In Java, inheritance is implemented using the extends keyword.

#### Polymorphism

Polymorphism means “many forms” and it allows one interface to be used for a general class of actions. The specific action is determined by the exact nature of the situation. In Java, polymorphism is mainly achieved through method overriding (runtime polymorphism) and method overloading (compile-time polymorphism).

#### Abstraction

Abstraction is the concept of hiding the complex implementation details and showing only the essential features of the object. It helps in reducing programming complexity and effort. In Java, abstraction is achieved using abstract classes and interfaces.

#### Exemplo

```Java

// Encapsulation
public class Car {
    private String model;
    private int year;

    public Car(String model, int year) {
        this.model = model;
        this.year = year;
    }

    public String getModel() {
        return model;
    }

    public int getYear() {
        return year;
    }
}

// Inheritance
public class ElectricCar extends Car {
    private int batteryLife;

    public ElectricCar(String model, int year, int batteryLife) {
        super(model, year);
        this.batteryLife = batteryLife;
    }

    public int getBatteryLife() {
        return batteryLife;
    }
}

// Polymorphism
public class Main {
    public static void main(String[] args) {
        Car myCar = new ElectricCar("Tesla", 2023, 500);
        System.out.println(myCar.getModel()); // Tesla
    }
}

// Abstraction
abstract class Animal {
    abstract void makeSound();
}

class Dog extends Animal {
    void makeSound() {
        System.out.println("Bark");
    }
}


```

### 3) Describe the components of a basic Java program

#### Package Declaration

If your class is part of a package, you declare it at the very beginning of your file. Packages help organize your classes and avoid naming conflicts.

```Java
package com.example.myapp;
```

https://refreshjava.com/java/packages-in-java

#### Import Statements

These are used to import other Java classes and packages that your class depends on. This allows you to use classes from the Java API or other libraries.

```Java
import java.util.Scanner;
```

#### Class Declaration

This is where you define your class. Every Java program must have at least one class definition. The class name should match the filename.

```Java
public class HelloWorld {
    // Class body
}
```
https://refreshjava.com/java/classes-in-java

#### Main Method

The main method is the entry point of any Java application. It’s where the program starts execution. The signature of the main method is always the same.
```Java
public static void main(String[] args) {
    // Code to be executed
}
```

#### Variables and Methods

Inside the class, you can declare variables and methods. Variables store data, and methods define the behavior of the class.

```Java
public class HelloWorld {
    // Variable declaration
    private String message;

    // Constructor
    public HelloWorld(String message) {
        this.message = message;
    }

    // Method
    public void printMessage() {
        System.out.println(message);
    }

    // Main method
    public static void main(String[] args) {
        HelloWorld hello = new HelloWorld("Hello, World!");
        hello.printMessage();
    }
}
```

https://refreshjava.com/java/structure-of-java-program


### 4) Compile and execute a Java program

#### Compile the Java program


Use the javac command to compile your Java file. This will generate a .class file.

```java
javac HelloWorld.java
```

Use the java command to run the compiled Java program.

```Java
java HelloWorld
```

## Basic Java Elements

### 1) Identify the conventions to be followed in a Java program

#### Packages

The prefix of a unique package name is always written in all-lowercase ASCII letters and should be one of the top-level domain names, currently com, edu, gov, mil, net, org, or one of the English two-letter codes identifying countries as specified in ISO Standard 3166, 1981.
Subsequent components of the package name vary according to an organization's own internal naming conventions. Such conventions might specify that certain directory name components be division, department, project, machine, or login names.

```Java 
com.sun.eng
com.apple.quicktime.v2
edu.cmu.cs.bovik.cheese
```

#### Classes

Class names should be nouns, in mixed case with the first letter of each internal word capitalized. Try to keep your class names simple and descriptive. Use whole words-avoid acronyms and abbreviations (unless the abbreviation is much more widely used than the long form, such as URL or HTML).	

```Java
class Raster;
class ImageSprite; 
```

#### Interfaces

Interface names should be capitalized like class names.	

```Java 
interface RasterDelegate;
interface Storing;
```

#### Methods

Methods should be verbs, in mixed case with the first letter lowercase, with the first letter of each internal word capitalized.

```Java 
run();
runFast();
getBackground();
```

#### Variables

Except for variables, all instance, class, and class constants are in mixed case with a lowercase first letter. Internal words start with capital letters. Variable names should not start with underscore _ or dollar sign $ characters, even though both are allowed.
Variable names should be short yet meaningful. The choice of a variable name should be mnemonic- that is, designed to indicate to the casual observer the intent of its use. One-character variable names should be avoided except for temporary "throwaway" variables. Common names for temporary variables are i, j, k, m, and n for integers; c, d, and e for characters.

```Java 
int             i;
char            c;
float           myWidth;
```

#### Constants

The names of variables declared class constants and of ANSI constants should be all uppercase with words separated by underscores ("_"). (ANSI constants should be avoided, for ease of debugging.)	

```Java 
static final int MIN_WIDTH = 4;
static final int MAX_WIDTH = 999;
static final int GET_THE_CPU = 1;
```

https://www.oracle.com/java/technologies/javase/codeconventions-introduction.html

### 2) Use Java reserved words


Keywords are reserved words in Java that serve as a code key. These words can't be used for anything else because they're predefined. They can't be used as a variable name, object name, or any other identifier. There are 51 reserved terms or keywords in Java.

```Java
abstract, assert, boolean, break, byte, case, catch, char, class, const,
continue, default, do, double, else, enum, extends, final, finally,
float, for, if, implements, import, instanceof, int, interface, long,
native, new, package, private, protected, public, return, short, static,
strictfp, super, switch, synchronized, this, throw, throws, transient, try, void, volatile, while
```

### 3) Use single-line and multi-line comments in Java programs

#### Single-Line Comments

Single-line comments in Java are used to comment out a single line or a part of it. They begin with two forward slashes (//) and extend to the end of the line. Single-line comments are helpful for brief explanations or notes relevant to the local code. 


```Java 
public class Main {
    public static void main(String[] args) {
        // Declare a variable to store the number
        int number = 10;

        // Calculate the square of the number
        int square = number * number;

        // Print the result
        System.out.println("The square of " + number + " is: " + square);
    }
}
```

#### Multi-Line Comments

Multi-line comments in Java are used to comment out blocks of text spanning multiple lines. They start with /* and end with */. Everything between these markers is considered a comment and is ignored by the Java compiler. Multi-line comments help provide detailed explanations or temporarily disable a block of code during debugging.

```Java 
public class Main {
    public static void main(String[] args) {
        int n = 10; // number of elements in the Fibonacci series

        /* The Fibonacci sequence is a series of numbers where
           a number is the addition of the last two numbers,
           starting with 0, and 1.

           This loop calculates each number in the series
           up to the nth number and prints them. */
        int n1 = 0, n2 = 1;
        System.out.print("First " + n + " terms: ");

        for (int i = 1; i <= n; ++i) {
            System.out.print(n1);

            if (i < n) {
                System.out.print(", ");
            }

            // compute the next term
            int sum = n1 + n2;
            n1 = n2;
            n2 = sum;
        }
    }
}
```

https://www.shiksha.com/online-courses/articles/java-comments/


### 4) Import other Java packages to make them accessible in your code

If you find a class you want to use, for example, the Scanner class, which is used to get user input, write the following code:

In the example above, java.util is a package, while Scanner is a class of the java.util package.

To use the Scanner class, create an object of the class and use any of the available methods found in the Scanner class documentation. In our example, we will use the nextLine() method, which is used to read a complete line:

```Java 
import java.util.Scanner;

class MyClass {
  public static void main(String[] args) {
    Scanner myObj = new Scanner(System.in);
    System.out.println("Enter username");

    String userName = myObj.nextLine();
    System.out.println("Username is: " + userName);
  }
}
```

There are many packages to choose from. In the previous example, we used the Scanner class from the java.util package. This package also contains date and time facilities, random-number generator and other utility classes.

To import a whole package, end the sentence with an asterisk sign (*). The following example will import ALL the classes in the java.util package:

```Java 
import java.util.*;
```

### 5) Describe the java.lang package

https://download.java.net/java/early_access/valhalla/docs/api/java.base/java/lang/package-summary.html

Provides classes that are fundamental to the design of the Java programming language. The most important classes are Object, which is the root of the class hierarchy, and Class, instances of which represent classes at run time.
Frequently it is necessary to represent a value of primitive type as if it were an object. The wrapper classes Boolean, Character, Integer, Long, Float, and Double serve this purpose. An object of type Double, for example, contains a field whose type is double, representing that value in such a way that a reference to it can be stored in a variable of reference type. These classes also provide a number of methods for converting among primitive values, as well as supporting such standard methods as equals and hashCode. The Void class is a non-instantiable class that holds a reference to a Class object representing the type void.

The class Math provides commonly used mathematical functions such as sine, cosine, and square root. The classes String, StringBuffer, and StringBuilder similarly provide commonly used operations on character strings.

Classes ClassLoader, Process, ProcessBuilder, Runtime, SecurityManager, and System provide "system operations" that manage the dynamic loading of classes, creation of external processes, host environment inquiries such as the time of day, and enforcement of security policies.

Class Throwable encompasses objects that may be thrown by the throw statement. Subclasses of Throwable represent errors and exceptions.

## Working with Java Data Types

### 1) Declare and initialize variables including a variable using final

https://www.baeldung.com/java-initialization

#### Declaration vs. Initialization

Declaration is the process of defining the variable, along with its type and name.

Initialization, on the other hand, is all about assigning a value to the variable.

```Java
//declaring a variable
int id;

//initializing a variable
id = 1;

//declaring and initializing a varible simultaneously
int num = 1
```

#### The Final Keyword

The final keyword applied to a field means that the field's value can no longer be changed after initialization. In this way, we can define constants in Java.

Let's add a constant to our User class:

```Java 
private static final int YEAR = 2000;
```
Constants must be initialized either when they're declared or in a constructor.

### 2) Cast a value from one data type to another including automatic and manual promotion

https://www.javatpoint.com/type-casting-in-java

In Java, type casting is a method or process that converts a data type into another data type in both ways manually and automatically. The automatic conversion is done by the compiler and manual conversion performed by the programmer. In this section, we will discuss type casting and its types with proper examples.

![alt text](image.png)

#### Widening Type Casting
Converting a lower data type into a higher one is called widening type casting. It is also known as implicit conversion or casting down. It is done automatically. It is safe because there is no chance to lose data. It takes place when:

- Both data types must be compatible with each other.
- The target type must be larger than the source type.

```Java 
public class WideningTypeCastingExample {  
    public static void main(String[] args) {  
        int x = 7;  
        //automatically converts the integer type into long type  
        long y = x;  
        //automatically converts the long type into float type  
        float z = y;  
        System.out.println("Before conversion, int value "+x);  
        System.out.println("After conversion, long value "+y);  
        System.out.println("After conversion, float value "+z);  
    }  
}  
```

Output

```
Before conversion, the value is: 7
After conversion, the long value is: 7
After conversion, the float value is: 7.0
```

#### Narrowing Type Casting
Converting a higher data type into a lower one is called narrowing type casting. It is also known as explicit conversion or casting up. It is done manually by the programmer. If we do not perform casting then the compiler reports a compile-time error.

```Java 
public class NarrowingTypeCastingExample {  
    public static void main(String args[]) {  
        double d = 166.66;  
        //converting double data type into long data type  
        long l = (long)d;  
        //converting long data type into int data type  
        int i = (int)l;  
        System.out.println("Before conversion: "+d);  
        //fractional part lost  
        System.out.println("After conversion into long type: "+l);  
        //fractional part lost  
        System.out.println("After conversion into int type: "+i);  
    }  
}  
```

Output
```
Before conversion: 166.66
After conversion into long type: 166
After conversion into int type: 166
```
## Working with Java Operator
## Working with the String Class
## Using Decision Statements
## Java Methods
## Using Looping Statements
## Arrays and ArrayLists
## Classes and Constructors