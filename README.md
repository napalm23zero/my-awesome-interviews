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
