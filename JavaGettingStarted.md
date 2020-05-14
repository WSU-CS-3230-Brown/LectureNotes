# Java - Getting Started #

## Class Basics ##

* In java, everything is a class
* Java requires at least 1 class
* classes can be instantiated into objects
* classes combine data and behavior

## The main Method ##

```[java]
public static void main(String[] args) {
    // code here
}
```
* The main method is the entry point to the application
* `public` - access modifer
* `static` - the main method is static. Static methods belong to the class not any one instance of the class.
* `void` - the return type, void means no return
* `main` - the method name. The main method always is named `main`
* `String[]` - indicates an array of `String` objects
* `args` - the name of the parameter for the method

## Compiling Java Code ##

```
> javac Class.java
```
* Java code is compiled into a intermediate language called *ByteCode* (.class files)
* Java uses the JVM (Java Virtual Machine) to execute java programs

## Executing Java Code ##

```
> java Class
```

* the JVM runs on the host computer and reads java ByteCode in order to exectue java applications
* JVM uses *JIT Compilation* (Just-In-Time)
  * This means that the ByteCode is compiled down to the native machine code on the fly as needed
  * This is what allows java code to be so portable and run on multiple platforms

## Java Jars ##

* Java ARchive - a package of all the code and resources for your program
* In order for a JAR to be executable it needs a manifest file
* The manifest has different piece of metadata that let java know how to run it.
* The critical piece of data it needs is the Main-Class

Example Manifest (Hello.mf):
```
Manifest-Version: 1.0
Main-Class: Hello
```
Create the Jar:
```
> jar cmf Hello.mf Hello.jar Hello.class Hello.java
```
> Note: the .java files are not needed to execute the jar only the .class files are. If you are distributing the jar to people who don't need the source code you would leave out the .java files.

Run it:
```
> java -jar Hello.jar
```

