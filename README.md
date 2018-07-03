# Core-Java
Core Java Concept for Hadoop

Index

1.Basics of java: For Hadoop Developers

✓ -Introduction
✓ -JVM Architecture
✓ -Bytecode format
✓ -Structure of java program
✓ -identifiers, data types, types of variables
✓ -types of methods
✓ -difference b/w static & instance content
✓ -constructors in java

2. Object Oriented Programming Concept that a Hadoop Developer should be aware of


✓ Object
✓ Class
✓ Data Hiding
✓ Data Abstraction
✓ Data Encapsulation
✓ Inheritance
✓ Polymorphism(Over loading & Over riding)
✓ Abstract Classes
✓ Interfaces


3. Exception Handling in Java

✓ Introduction
✓ Types of Exceptions
✓ Handling the Exception


4. Collection Framework

✓ Introduction
✓ Util package interfaces
✓ List(I) and it’s classes
✓ Set(I) and it’s classes
✓ Map(I) and it’s classes

1. Basics Of Java:
==================

Java at a glance:

> Java is a general-purpose computer-programming language that is concurrent, class-based, object-oriented,[15] and specifically designed to have as few implementation dependencies as possible. It is intended to let application developers "write once, run anywhere" (WORA),[16] meaning that compiled Java code can run on all platforms that support Java without the need for recompilation.[17] Java applications are typically compiled to bytecode that can run on any Java virtual machine (JVM) regardless of computer architecture. 

> Designed By James Gouslin in 1995

> Developed By Sun Microsystem first released in 1996 and now owned by Oracle after acquisition of Sun Microsystems in 2009–10 By Oracle Corporation.

> Java is a Programming language and a platform for application development. A platform is a loosely defined computer industry buzzword that typically means some combination of hardware and system software that will mostly run all the same software.

Understanding JVM:
====================
How Java is a Platform: The heart of the Java platform is the concept of a "virtual machine" that executes Java bytecode programs. This bytecode is the same no matter what hardware or operating system the program is running under. ... There is a JIT (Just In Time) compiler within the Java Virtual Machine, or JVM.

JVM (Java Virtual Machine) is an abstract machine. It is a specification that provides runtime environment in which java bytecode can be executed. JVM is the one that actually calls the main method present in a java code.

JVM is platform dependent: With Java, you can compile source code on Windows and the compiled code (bytecode to be precise) can be executed (interpreted) on any platform running a JVM. So yes you need a JVM but the JVM can run any compiled code, the compiled code is platform independent.

Bytecode basics:
==================
The bytecode format: Bytecodes are the machine language of the Java virtual machine. When a JVM loads a class file, it gets one stream of bytecodes for each method in the class. The bytecodes streams are stored in the method area of the JVM. The bytecodes for a method are executed when that method is invoked during the course of running the program. They can be executed by intepretation, just-in-time compiling, or any other technique that was chosen by the designer of a particular JVM.

A method's bytecode stream is a sequence of instructions for the Java virtual machine. Each instruction consists of a one-byte opcode followed by zero or more operands. The opcode indicates the action to take. If more information is required before the JVM can take the action, that information is encoded into one or more operands that immediately follow the opcode. (source:javaworld.com).

Primitive types and JVM: The JVM supports seven primitive data types. Java programmers can declare and use variables of these data types, and Java bytecodes operate upon these data types. The seven primitive types are listed in the following table:


Type	            Definition
byte	    one-byte signed two's complement integer
short	    two-byte signed two's complement integer
int	      4-byte signed two's complement integer
long	    8-byte signed two's complement integer
float	    4-byte IEEE 754 single-precision float
double	  8-byte IEEE 754 double-precision float
char	    2-byte unsigned Unicode character

The primitive types appear as operands in bytecode streams. All primitive types that occupy more than 1 byte are stored in big-endian order in the bytecode stream, which means higher-order bytes precede lower-order bytes. (source:javaworld.com).

Architecture of JVM:
=====================
JVM is divided into 3 parts:

1. class loader
2. Memory area of JVM
3. Excecution ingine

Internal Architecture of JVM:Let's understand the internal architecture of JVM. It contains classloader, memory area, execution engine etc. 

1) Classloader
Classloader is a subsystem of JVM that is used to load class files.

2) Class(Method) Area
Class(Method) Area stores stream of bytecodes for each method per-class structures such as the runtime constant pool, field and method data, the code for methods. 

3) Heap
It is the runtime data area in which objects are allocated.

4) Stack
Java Stack stores frames. It holds local variables and partial results, and plays a part in method invocation and return.
Each thread has a private JVM stack, created at the same time as thread. A new frame is created each time a method is invoked. A frame is destroyed when its method invocation completes.

5) Program Counter Register
PC (program counter) register contains the address of the Java virtual machine instruction currently being executed.

6) Native Method Stack
It contains all the native methods used in the application.

7) Execution Engine
It contains:

1) A virtual processor
2) Interpreter: Read bytecode stream then execute the instructions.
3) Just-In-Time(JIT) compiler: It is used to improve the performance. JIT compiles parts of the byte code that have similar functionality at the same time, and hence reduces the amount of time needed for compilation. Here, the term "compiler" refers to a translator from the instruction set of a Java virtual machine (JVM) to the instruction set of a specific CPU.



Structure of Java:

package <NewpackageName>;
import <ExistingPackageName>;
  
class <any_class_name>       //A User Defined Object/Data Type
{
  //list of data-members/fields/attributes/ declaration       //also known as states of Object/class
  //list of method/function declarations and/or definition    //also called Behavior of Object/class
  
  public static void main(String [] args)
  {
      //Block of Statements
      
  }
}

2. Object Oriented Programming Concept that a Hadoop Developer should be aware of:
==================================================================================
> What is Object?
An Object is a physical entity; it contains some state and related behavior.
