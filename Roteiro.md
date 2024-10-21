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

https://www.oracle.com/java/technologies/javase/codeconventions-introduction.html

## Working with Java Data Types
## Working with Java Operator
## Working with the String Class
## Using Decision Statements
## Java Methods
## Using Looping Statements
## Arrays and ArrayLists
## Classes and Constructors