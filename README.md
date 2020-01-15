# Java Awesome Interview

Here some interview questions and some ridiculously complete answers, to impress your interviewers

---

## What is Java?

Java is a general-purpose, high-level programming language. Java is mainly Object Oriented, despite is possible to do functional and structured oriented software.
Java runs in WORA (Write Once Run Anywhere), JVM (Java Virtual Machine) has different implementations on different Operational Systems, but the code, once compiled run exactly in the same way on any machine.

Source files have `.java` extension but when this file is compiled it turns into `.class` file.

Here an example of a Hello World in Java:

```Java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World!");
        // Prints the string to the console.
    }
}
```

### a little bit of syntax

Java uses brackets to open/close code structures and semicolon to close code lines.

The keyword `public` in class declaration, denotes that this class can be accessed from all application's scope and hierarchy, `private` keyword means that this class and it's methods only can be accessed in it's own context, `package` keyword allows access on the current package and can be omitted from code once it is the default access status, and finally `protected` allows extending this class from any application context and access methods from extended class, but not the protected class directly.

The keyword `static` indicate that this class will no be instantiated, it is the implementation itself, so the static methods inside of it can be invoked directly. Non static classes can have static methods, in that case, the method belongs to the class, not to the instance of the class, it can be accessed directly by other classes but cannot be accessed by an instance of it's class.

Methods must have a return indicator keyword, if your method does not return any value, it must me set as `void`, but if it returns any kind of Object of Primitive Value, it must be set before method name, like `String` on HelloWorld example.

After method name, inside parenthesis, you can send parameters to the method, this parameters are not required, but when applied must have type specified and then a given name. Multiple parameters, must be separated by comma.

## Can you list some Java features?

Java is strongly made up on OOP concepts like Inheritance, Encapsulation, Polymorphism and Abstraction, despites the fact that can implement Functional Programming too. It's Platform Independent, so you can run the exactly same code in different OSs and Hardwares. It has High Performance thanks to JIT (Just In Time compiler) and it is Multi-threaded, so a flow of execution can perform multiple activities in parallel.

## You told about JIT, can you explain it to us?

JIT (Just In Time compiler) is a component of JRE that improves the performance do Java application ai run time converting instructions into bytecode, and then this bytecode is converted to native machine code, then hardware can read it faster, leading performance to application. JIT compilation require a huge amount of processor and memory, but only on the first time application runs.

## Explain the difference between JRE, JDK, JVM and SDK.

Hierarchically:

`JVM` (Java Virtual Machine) is the core os Java Programming Language, when a program runs, JVM responsible to convert bytecode to machine code. JVM assures that your code will run in any machine as it is, because JVM has a different implementation for different OS and Hardware, but ir reads your code in the same way and compile ir to machine code as it needs. JVM works as manager of resources too, cause it handles with memory usage and optimization too.

`JDK` (Java Development Kit) it provides all the tools needed to run, debug and compile Java code.

`JRE` (Java Runtime Environment) it is the platform that execute Java Programs, it contains JVM binaries ena some Core classes needed to run any Java Application.

## What is a Class?

A Class ins an Entity that determines a behave of an Object, the structure and type of the information that it will contains. An Object is an instance of a class that have behavior inherited com the referred Class and mutable information.

## What is a Constructor?

The constructor is a method that has the same name as class name, inside this constructor you can enable some logic that will be executed as soon as the class is instantiated, you can create many constructors as you want but they need to have different signatures (parameters set). If you do not create any constructor, a default empty constructor will be created.

Here an example of a Constructor in Java:

```Java
public class User {

    String userName;

    // empty constructor
    public User() {
        System.out.println("Your User has no name");
    }

    // constructor with signature
    public User(String name) {
        System.out.println("Welcome " + name);
        this.userName = name;
    }
}
```

## What is OOP?

OOP (Object Oriented Programming) is a programming paradigm that base all data flow in Objects, i other words, every entity that can perform actions or can store data on the application is an Object. OOP typically use some concepts to make code more `readable`, `reusable`, `trackable` and `extensible`, this concepts are:

- Inheritance
- Encapsulation
- Polymorphism
- Abstraction

### explaining each of them.

#### Inheritance

Allows new classes adopt properties (attributes and methods) from another. It is a time saving feature. If you you have many Entities with a lot of properties in common, you can write a Class with all of this properties and create new Classes extending the first one adding only non common properties to them.

Here an example of a Inheritance in Java:

```Java
// Here we have the "model class" that have common properties
public class Person {
    String name;
    Integer age;

    public Person(String name, Integer age) {
        this.name = name;
        this.age = age;
    }

    public void introduce(String name, Integer age) {
        System.out.println("Hello my name is " + name + " and I'm "+ age);
    }
}
```

```Java
// Here we have Developer Class that is a extension from Person
public class Developer extends Person {
    String ide;
    String language;

    public Developer(String name, Integer age, String ide, String language) {
        super(name, age); // name and age are inherited properties
        this.ide = ide;
        this.language = language;
    }

    public void code() {
        introduce(this.name, this.age);
        System.out.println("I'm a Developer");
        System.out.println("I use " + this.ide + " to work with " + this.language);
    }
}
```

```Java
// Here we have Desinger Class that is a extension from Person
public class Designer extends Person {
    String editor;
    String modeler;

    public Designer(String name, Integer age, String editor, String modeler) {
        super(name, age); // name and age are inherited properties
        this.editor = editor;
        this.modeler = modeler;
    }

    public void create() {
        introduce(this.name, this.age);
        System.out.println("I'm a Designer");
        System.out.println("I use " + this.editor + " to edit and " + this.modeler + " to create prototypes.");
    }
}
```
