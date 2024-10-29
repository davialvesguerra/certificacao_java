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

### 3) Declare and initialize a String variable

https://www.baeldung.com/java-string-initialization
https://www.baeldung.com/java-string-pool

#### Creation 

We can use the new keyword or the literal syntax:

```java
String usingNew = new String("baeldung");
String usingLiteral = "baeldung";
```



#### String Declaration 

```java 
public class StringInitialization {

    String fieldString;

    void printDeclaredOnlyString() {
        String localVarString;
        
        // System.out.println(localVarString); -> compilation error
        System.out.println(fieldString);
    }
}
```
As we can see, if we try to use localVarString before giving it a value, we’ll get a compilation error. On the other hand, the console will show “null” for fieldString‘s value.

See, member variables are initialized with a default value when the class is constructed, null in String‘s case. But, we have to initialize local variables ourselves.

If we give localVarString a value of null, we’ll see that the two are, indeed, now equal:

#### String Initialization Using Literals

Let’s now create two Strings using the same literal:

```java
String literalOne = "Baeldung";
String literalTwo = "Baeldung";
assertTrue(literalOne == literalTwo);
```



The reason for this harks back to the fact that Strings are stored in a pool. literalOne adds the String “baeldung” to the pool, and literalTwo reuses it.

#### String Initialization Using new


We’ll see some different behavior, though, if we use the new keyword.

```java
String newStringOne = new String("Baeldung");
String newStringTwo = new String("Baeldung");

assertFalse(newStringOne == newStringTwo);
```

#### Empty Strings

```java
String emptyLiteral = "";
String emptyNewString = new String("");
String emptyNewStringTwo = new String();
```


As we know by now, the emptyLiteral will be added to the String pool, while the other two go directly onto the heap.

Although these won’t be the same objects, all of them will have the same value:

#### null Values 

Let’s declare and initialize a null String:

```java
String nullValue = null;
```

If we printed nullValue, we’d see the word “null”, as we previously saw. And, if we tried to invoke any methods on nullValue, we’d get a NullPointerException, as expected.


## Working with Java Operator

### 1) Use basic arithmetic operators to manipulate data including +, -, *, /, and %

![alt text](image-1.png)

### 2) Use the increment and decrement operators

https://www.javatpoint.com/increment-and-decrement-operators-questions-in-java

#### 2.1 Increment Operator (++):

The increment operator in Java is denoted by ++. It adds 1 to the current value of a variable. There are two ways to use the increment operator:


```java
int x = 5;  
x++;   // Equivalent to x = x + 1;  
```
or

```java
int x = 5;  
++x;   // Equivalent to x = x + 1;  
```

Both of these statements increase the value of x by 1. However, there is a subtle difference between the two when used as part of a larger expression, which we will explore later.

##### 2.1.1 Prefix Increment Operator:

When the increment operator is placed before the variable (++x), it increments the value of the variable before the value is used in the expression. For example:

```java
int a = 3;  
int b = ++a;  // Now, a is 4 and b is also 4  
```
In this case, a is incremented before its value is assigned to b.

##### 2.1.2 Postfix Increment Operator:

When the increment operator is placed after the variable (x++), it increments the value of the variable after its current value is used in the expression. For example:

```java
int c = 3;  
int d = c++;  // Now, c is 4, but d is 3  
```

Here, d is assigned the current value of c before c is incremented.


#### 2.2 Decrement Operator (--):

The decrement operator in Java is denoted by --. It subtracts 1 from the current value of a variable. Similar to the increment operator, there are two ways to use the decrement operator:

```java
int y = 8;  
y--;   // Equivalent to y = y - 1;  

int y = 8;  
--y;   // Equivalent to y = y - 1;`  
```
Both of these statements decrease the value of y by 1.

##### 2.2.1 Prefix Decrement Operator 

Similar to the increment operator, the prefix decrement operator (--x) decrements the value of the variable before its value is used in the expression.

```java
int m = 7;  
int n = --m;  // Now, m is 6 and n is also 6   
```

##### 2.2.2 Postfix Decrement Operator 

The postfix decrement operator (x--) decrements the value of the variable after its current value is used in the expression.

```java
int p = 7;  
int q = p--;  // Now, p is 6, but q is 7  
```

### 3. Relation Operator in Java 

https://www.digitalocean.com/community/tutorials/relational-operators-in-java

 - == is the equality operator. This returns true if both the operands are referring to the same object, otherwise false.
 - != is for non-equality operator. It returns true if both the operands are referring to the different objects, otherwise false.
 - < is less than operator.
 - \> is greater than operator.
 - <= is less than or equal to operator.
 - \>= is greater than or equal to operator.

#### 3.1 Relational Operators Supported Data Types

 - The == and != operators can be used with any primitive data types as well as objects.
 - The <, >, <=, and >= can be used with primitive data types that can be represented in numbers. It will work with char, byte, short, int, etc. but not with boolean. These operators are not supported for objects.

### 4. Use arithmetic assignment operators

https://www.geeksforgeeks.org/java-assignment-operator-with-examples/


### 5. Use conditional operators including &&, ||, and ? :

#### 5.1 Conditional AND

The operator is applied between two Boolean expressions. It is denoted by the two AND operators (&&). It returns true if and only if both expressions are true, else returns false.

#### 5.2 Conditional OR

The operator is applied between two Boolean expressions. It is denoted by the two OR operator (||). It returns true if any of the expression is true, else returns false.

#### 5.3 Ternary Operator

The meaning of ternary is composed of three parts. The ternary operator (? :) consists of three operands. It is used to evaluate Boolean expressions. The operator decides which value will be assigned to the variable. It is the only conditional operator that accepts three operands. It can be used instead of the if-else statement. It makes the code much more easy, readable, and shorter.

```
variable = (condition) ? expression1 : expression2  
```

The above statement states that if the condition returns true, expression1 gets executed, else the expression2 gets executed and the final result stored in a variable.

https://www.javatpoint.com/conditional-operator-in-java

### 6. Describe the operator precedence and use of parenthesis

https://www.refreshjava.com/java/operator-precedence#:~:text=What%20changes%20the%20precedence%20of,(a%2Bb)*c.

## Working with the String Class

### 1. Develop code that uses methods from the String class

https://www.javatpoint.com/methods-of-string-class

- **charAt(int index)**: retorna o caractere na posição especificada.

- **codePointAt(int index)**: retorna o valor Unicode do caractere na posição especificada.

- **compareTo(String anotherString)**: compara lexicograficamente duas strings.

- **compareToIgnoreCase(String str)**: compara lexicograficamente duas strings, ignorando diferenças entre maiúsculas e minúsculas.

- **concat(String str)**: concatena a string especificada ao final desta string.

- **contains(CharSequence s)**: verifica se a string contém a sequência de caracteres especificada.

- **contentEquals(CharSequence cs)**: compara a sequência de caracteres especificada com esta string.

- **endsWith(String suffix)**: verifica se a string termina com o sufixo especificado.

- **equals(Object anObject)**: compara se esta string é igual ao objeto especificado.

- **equalsIgnoreCase(String anotherString)**: compara se esta string é igual a outra string, ignorando diferenças entre maiúsculas e minúsculas.

- **format(String format, Object... args)**: retorna uma string formatada usando a string de formato e argumentos especificados.

- **indexOf(int ch)**: retorna o índice da primeira ocorrência do caractere especificado.

- **isEmpty()**: verifica se a string está vazia.

- **lastIndexOf(int ch)**: retorna o índice da última ocorrência do caractere especificado.

- **length()**: retorna o comprimento da string.

- **replace(char oldChar, char newChar)**: substitui todas as ocorrências de um caractere especificado por um novo caractere.

- **split(String regex)**: divide a string em uma matriz de substrings em torno das correspondências da expressão regular especificada.

- **startsWith(String prefix)**: verifica se a string começa com o prefixo especificado.

- **substring(int beginIndex, int endIndex)**: retorna uma substring especificada pelos índices de início e fim.

- **toLowerCase()**: converte todos os caracteres em minúsculas usando as regras da localidade padrão.

- **toUpperCase()**: converte todos os caracteres em maiúsculas usando as regras da localidade padrão.

- **trim()**: remove espaços em branco de ambos os lados da string.

### 2. Format Strings using escape sequences including %d, %n, and %s

https://www.geeksforgeeks.org/format-specifiers-in-java/

Format specifiers begin with a percent character (%) and terminate with a “type character, ” which indicates the type of data (int, float, etc.) that will be converted the basic manner in which the data will be represented (decimal, hexadecimal, etc.) The general syntax of a format specifier is

```
% [flags] [width] [.precision] [argsize] typechar
```

The format() method of Formatter class accepts a wide variety of format specifiers. When an uppercase specifier is used, then letters are shown in uppercase. Otherwise, the upper- and lowercase specifiers perform the same conversion. 

| Format specifier |      Conversion applied     |
|:----------------:|:---------------------------:|
|        %d        |       Decimal integer       |
|        %n        | Insert a new line character |
|        %s        |            String           |

## Working with the Random and Math Classes

### 1. Use the Random class 

https://www.geeksforgeeks.org/java-util-random-class-java/
https://www.scaler.com/topics/random-class-in-java/

Random class is used to generate pseudo-random numbers in java. An instance of this class is thread-safe. The instance of this class is however cryptographically insecure. This class provides various method calls to generate different random data types such as float, double, int.

| Método | Descrição |
|---|---|
| `nextBoolean()` | Retorna o próximo valor booleano pseudoaleatório. |
| `nextDouble()` | Retorna o próximo valor double pseudoaleatório. |
| `nextFloat()` | Retorna o próximo valor float pseudoaleatório. |
| `nextGaussian()` | Retorna o próximo valor double pseudoaleatório distribuído de acordo com uma distribuição normal (Gaussiana). |
| `nextInt()` | Retorna o próximo valor int pseudoaleatório. |
| `nextInt(int bound)` | Retorna um valor int pseudoaleatório entre 0 (inclusivo) e o valor especificado (exclusivo). |
| `nextLong()` | Retorna o próximo valor long pseudoaleatório. |
| `setSeed(long seed)` | Define o valor da semente para este gerador de números aleatórios. |
| `nextBytes(byte[] bytes)` | Gera bytes aleatórios e os coloca no array fornecido. |
| `ints()` | Retorna um stream infinito de inteiros pseudoaleatórios. |
| `ints(long streamSize)` | Retorna um stream de inteiros pseudoaleatórios com o tamanho especificado. |
| `ints(int randomNumberOrigin, int randomNumberBound)` | Retorna um stream infinito de inteiros pseudoaleatórios dentro do intervalo especificado. |
| `ints(long streamSize, int randomNumberOrigin, int randomNumberBound)` | Retorna um stream de inteiros pseudoaleatórios com o tamanho especificado dentro do intervalo especificado. |
| `longs()` | Retorna um stream infinito de longos pseudoaleatórios. |
| `longs(long streamSize)` | Retorna um stream de longos pseudoaleatórios com o tamanho especificado. |
| `longs(long randomNumberOrigin, long randomNumberBound)` | Retorna um stream infinito de longos pseudoaleatórios dentro do intervalo especificado. |
| `longs(long streamSize, long randomNumberOrigin, long randomNumberBound)` | Retorna um stream de longos pseudoaleatórios com o tamanho especificado dentro do intervalo especificado. |
| `doubles()` | Retorna um stream infinito de doubles pseudoaleatórios. |
| `doubles(long streamSize)` | Retorna um stream de doubles pseudoaleatórios com o tamanho especificado. |
| `doubles(double randomNumberOrigin, double randomNumberBound)` | Retorna um stream infinito de doubles pseudoaleatórios dentro do intervalo especificado. |
| `doubles(long streamSize, double randomNumberOrigin, double randomNumberBound)` | Retorna um stream de doubles pseudoaleatórios com o tamanho especificado dentro do intervalo especificado. |

### 2. Use the Math class 

The Java Math class has many methods that allows you to perform mathematical tasks on numbers.

| Método | Descrição |
|---|---|
| `abs(double a)` | Retorna o valor absoluto de um valor. |
| `acos(double a)` | Retorna o arco-cosseno de um valor. |
| `asin(double a)` | Retorna o arco-seno de um valor. |
| `atan(double a)` | Retorna o arco-tangente de um valor. |
| `cbrt(double a)` | Retorna a raiz cúbica de um valor. |
| `ceil(double a)` | Retorna o menor valor inteiro maior ou igual ao argumento. |
| `cos(double a)` | Retorna o cosseno de um ângulo. |
| `exp(double a)` | Retorna a constante de Euler elevada à potência do argumento. |
| `floor(double a)` | Retorna o maior valor inteiro menor ou igual ao argumento. |
| `log(double a)` | Retorna o logaritmo natural (base e) de um valor. |
| `log10(double a)` | Retorna o logaritmo de base 10 de um valor. |
| `max(double a, double b)` | Retorna o maior de dois valores. |
| `min(double a, double b)` | Retorna o menor de dois valores. |
| `pow(double a, double b)` | Retorna o valor de a elevado à potência de b. |
| `random()` | Retorna um valor double positivo maior ou igual a 0.0 e menor que 1.0. |
| `round(double a)` | Retorna o valor arredondado de um valor. |
| `sin(double a)` | Retorna o seno de um ângulo. |
| `sqrt(double a)` | Retorna a raiz quadrada de um valor. |
| `tan(double a)` | Retorna a tangente de um ângulo. |


## Using Decision Statements

### 1. Use the decision making statement  (if-then and if-then-else)

#### 1.1 If Statement in Java 

The “if” statement in Java is like a traffic signal that helps your program make decisions. It allows you to run a specific piece of code only if a particular condition is met. It’s like saying, “If something is true, then do this!”

```java 
if(condition){
//code to be executed
}
```

```java 
public class IfStatementExample {
    public static void main(String[] args) {

        int age = 18;
       
        if (age >= 18) {
            System.out.println("You are eligible to vote!");
        }
    }
}
```

#### 1.2 If-Else Statement in Java

Now you may be wondering what if the condition is not true and you want to execute some another block of code. The “if-else” statement in Java is another decision-making statement that allows you to execute different blocks of code based on the condition’s result. It provides an alternative path to take when the condition is not true.

```java 
if(condition){
//code to be executed if the condition is true
} else{
//code to be executed if the condition is false
}
```
Here’s a simple example to illustrate the usage of the “if-else” statement:

```java
public class IfElseStatementExample {
    public static void main(String[] args) {
        int age = 16;
       
        if (age >= 18) {
            System.out.println("You are eligible to vote!");
        } else {
            System.out.println("You are not eligible to vote yet.");
        }
    }
}
```

### 2. Use the switch statement 

Java’s “switch” statement is a decision-making statement that lets you choose which of numerous code blocks to run depending on the value of a certain variable. It offers a practical method for handling various alternatives or scenarios in your code.

```java 
switch(expression)
{
case <value1>:
//code to be executed
break;
case <value2>:
//code to be executed
break;
default:
//code to be defaultly executed
}
```

Imagine you are in a coffee shop and want to order a beverage. You approach the counter, and the barista asks for your order. Instead of using a series of “if” statements to check each possible option, the barista uses a switch statement.

The barista takes your order and checks the value you provide. Based on that value, they can quickly determine which beverage you want and prepare it accordingly. Each possible value represents a different option, such as “coffee,” “tea,” “cappuccino,” or “latte.” The barista can efficiently handle all these options using a switch statement.

Here’s a simple example code that demonstrates the use of the switch statement:

```java 
public class BeverageExample {
    public static void main(String[] args) {
        String beverage = "cappuccino";
        switch (beverage) {
            case "coffee":
                System.out.println("Enjoy your hot coffee!");
                break;
            case "tea":
                System.out.println("Savor the flavor of your tea!");
                break;
            case "cappuccino":
                System.out.println("Indulge in the creamy cappuccino!");
                break;
            default:
                System.out.println("Sorry, we don't have that beverage.");
        }
    }
}
```

#### The break keyword 

When Java reaches a break keyword, it breaks out of the switch block.
This will stop the execution of more code and case testing inside the block.
When a match is found, and the job is done, it's time for a break. There is no need for more testing.
A break can save a lot of execution time because it "ignores" the execution of all the rest of the code in the switch block.

#### The default Keyword

The default keyword specifies some code to run if there is no case match. Note that if the default statement is used as the last statement in a switch block, it does not need a break.


### 3. Compare how == differs between primitives and objects 

Both the equals() method and the == operator are used to compare two objects in Java.

The Java string equals() method, compares two strings and returns true if all characters match in both strings, else returns false.

The == operator compares the reference or memory location of objects in a heap, whether they point to the same location or not.
Whenever we create an object using the operator new, it will create a new memory location for that object. So we use the == operator to check memory location or address of two objects are the same or not.

In general, both equals() and “==” operators in Java are used to compare objects to check equality, but here are some of the differences between the two: 

1. The main difference between the .equals() method and the == operator is that one is a method, and the other is the operator.
2. We can use == operators for reference comparison (address comparison) and .equals() method for content comparison. In simple words, == checks if both objects point to the same memory location whereas .equals() evaluates to the comparison of values in the objects.
3. If a class does not override the equals method, then by default, it uses the equals(Object o) method of the closest parent class that has overridden this method. **See Why to Override equals(Object) and hashCode() method? in detail.

We can apply equality operators for every primitive type, including the boolean type. We can also apply equality operators for object types. 

If we apply == for object types then, there should be compatibility between argument types (either child to parent or parent to child or same type). Otherwise, we will get a compile-time error. 

### 4. Compare two String objects by using the compareTo and equals methods

In String Context:
- compareTo: Compares two strings lexicographically.
- equals: Compares this string to the specified object.

compareTo compares two strings by their characters (at same index) and returns an integer (positive or negative) accordingly.


```java
String s1 = "ab";
String s2 = "ab";
String s3 = "qb";
s1.compareTo(s2); // is 0
s1.compareTo(s3); // is -16
s3.compareTo(s1); // is 16
```

## Java Methods
## Using Looping Statements
## Arrays and ArrayLists
## Classes and Constructors