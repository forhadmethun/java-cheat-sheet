##### Why So Popular
 platform independent, OOP, Security, rich API, IDEs, Web, Mobile, micro-services 
 
##### Platform Independence 
 Build once, run everywhere 
   Java Code - Bytecode - Run - JVM - OS instruction
 
 > Bytecode is just like Shorthand language that store each keyword of java as a sign. and each sign takes 1 byte of memory in RAM. Hence the name called as Bytecode file.
##### JDK vs JVM Vs JRE
  - JVM( Java Virtual Machine ) ( interpreter )
        - runs the java bytecode
  - JRE
        - JVM + Libraries + Other Components ( to run applets & other java applications) 
  - JDK 
        - JRE + Compiler + Debugger
        
#####ClassLoader  
  - Find and Loads Java Classes!
  - 3 types   
    - System  - Loads all application classes from CLASSPATH
    - Extension  - Loads all classes from extension directory 
    - Bootstrap - Loads all the java core files 
        
       
        
#####First Java Program

```java

public class Main {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```
Notes: 
  - Every line of code written in Java is part of Class. 
  - all the codes are inside public class Main
  - when program runs Java knows that the main method need to be executed first 
    > java is case  sensitive 
    

##### java & javac command 
 - javac Main.java 
   - It creates a class file which contains java bytecode  
 - java Main
    - the command run the bytecode using JVM. It shows "Hello World!" as output in console. 
    
##### Class and Object 
   - object is an instance of a class
   - with the object the method of a class can be invoked
    
##### Variable
   - The value of a variable changes during the course of a program execution 
```
    int number; 
    number = 5; 
    System.out.println(number);// prints 5
    number = number + 2; 
    System.out.println(number); // prints 7 

```


- Variable is declared as - 
  - type variableName; 
  > multiple variable can be declared in a single line 
  
  > all six numeric types in Java are signed 
  
##### Primitive Variable 
int, float, char, boolean, byte, short, int, long, double - for these primitive data types java is not considered as a pure Object Oriented Language 

> in value = 5; 
```
    int i = 15; 
    long longValue = 10000000000l; 
    byte b = (byte) 254; 
    float f = 26.012f;
    boolean isDone = true; 
    boolean isGood = false; 
    char ch = 'a'; 
    char ch2 = ';'; 

```
##### Reference Variables
 - when any object is created it actually refer to the object created in the memory. 
``` 
Animal cat = new Animal(); 
Animal kitty = new Animal(); 
cat  = kitty; 
    
``` 
##### Identifiers 
 - Class Name, method, variables are called identifiers. 
   - Legal Identifier Naming convention
     - combination of letters, numbers, $ and _
     - cannot start with number
     - cannot be a keyword
     - no limit on length of identifier 
##### Java Keywords
- Primitive Data Types: byte, short, int, long, float, double, char, boolean
- Flow Control: if, else, for, do, while, case, switch, default, break, continue, return
- Modifiers: private, public, protected, final, static, native, abstract, synchronized, transient, volatile, stictfp
- Exception Handling: try, catch, finally, throws, assert
- Class related: class, interface, package, extends, implements, import
- Literals: true, false, null, 
- Others: void, enum
- Unused: goto, const

#####Literals
 any primitive data type value in source code is called Literal.  
 Four Types of literals - 
  - Integer & Long
    - decimal: 334, 23
    - octal: place 0 before number, ex- 070
  - Floating Point
    - double d=123.12;
    - float f = 123.12f;// floating point literals are double by default
  - Boolean
    - true and false
    - TRUE, FALSE, True, False are invalid
  - Character
    - char a = 'a'
    - char letterA = '\u0041'; 
    
```
    int eight = 010;
    int nine  = 011; 
    int invalid = 089;//8 not in octal 
    int sixteen = 0x10;
    int fifteen = 0xF; 
    int fourteen = 0xe; 
    int x = 23,000;
    long a = 123123l;
    long b = 0x9ABCDEFGH;
    long c = 0123123342L; 
    
    float f = 123.1233;//error as double cannot assigned to float
    boolean b = true; 
    boolean b = 0;//error 
    char ch = a;
    char a = 97; 
    char ch1 = 66000;//error
```    
    
### Assignment Operator
##### basic examples
``` 
    int a = 5;
    int b = a; 
    b = 10;// doesn't change value of a
```
##### basic puzzles
``` 
    Person firstPerson = new Person();
    firstPerson.setName("Me");
    
    Person secondPerson = firstPerson;
    secondPerson.setName("We"); // changes value of firstPerson
```

### Casting - Implicit and Explicit
 Conversion of one data type to another.
 - int is by default int
 - float is by default double 
 ``` 
 
 ```
##### Implicit Casting
- directly done by compiler
``` 
    byte b= 5; //byte b = (int) 10; 
    int value = 100;
    long number = value;//implicit casting 
    float f = 100;//implicit casting 
```
##### Explicit Casting
- Programmer need to cast 
``` 
long longNumber = 256784;
int intNumber = (int) longNumber; 

int x = (int) 35.35; 


//float avg = 2.4;//COMPILER ERROR as by default double!!
float avg = (float)2.4; 
float pi = 3.1516f;//F is also fine;

```

### Operator
##### Assignment 
 - +=, -=, *=
##### Remainder
 - %
##### Conditional
- Ternary Operator 
    - booleanCondition ? ResultIfTrue : ResultIfFalse
    
###Passing Variable to Methods 
 - all variable, primitives and references can be passed as a parameter
 - primitive variables don't modify value in method but reference variables do
 - null is a valid return for Object, void cannot return anything
###Types of Variables
 - Instance Variable
    - declared inside a class & outside any method
    - called member value, field, property
 - Local Variables
    - declared inside method
    - if name is same as an instance variable it results shadowing 
 - Member Variables
    - defined at class level without static keyword
 - Static Variables 
    - defined at class level with static keyword
    - can be accessed through a) Class Name b) Object Reference(not recommended) 
    Example - 
``` 

``` 

###Scope of Variable
- static variable can be accessed anywhere 
- member variable can be used any non-static method
- local variable can be used only it's scope
- block variable {} can be used only in the block  
Example - 
``` 

```


### Variable Initialization
- member/ static variables are always  initialized with default value
- default value of numeric is 0, floating point is 0.0, char is '\u0000', object is null
- local variables are not initialized
- before initializing using local variable causes compiler error
- assigning null is valid for reference variable  
Example - 
``` 

```

### Wrapper Class
 - wraps a data type and gives it an object apperance
    - Wrapper: Boolean, Byte, Character, Double, Float, Integer, Long, Short
    - Primitive: boolean, byte, character, double, float, Integer, long, short
####Wrapper Class Utility Methods
 - valueOf (create wrapper object)
    ``` 
        Integer seven = Integer.valueOf("111",2);// binary 111 is converted to 7
    ```
 - xxxValue(create primitive)
    ``` 
        int primitiveSeven = seven.intValue();
    ```
 - parseXxx(same as value of but create primitive)
 - toString
##### Auto Boxing
  - 
  ``` 
  Integer ten = new Integer(10);
  Integer nine = 9;
  ```

###String Class 
  - sequence of characters
  - not primitive in java
  
##### String are Immutable
  - 
  ``` 
    String str = "value1";
    str.concat("value2");
    System.out.println(str) ; //prints "value1"
    
    String concat = str.concat("value2"); //now concat is "value1value2"
    
  ```
  
  - String literals are stored in "String constant pool". String object is created in heap. 
  ``` 
  String myString = new String("hello");
  //1. String Literal "hello" - created in the "String constant pool"
  //2. String Object - created on the heap
  ```
### String vs StringBuffer vs StringBuilder
Immutable - String  
Thread Safe - String, StringBuffer
Performance(a number of modification needed when) - StringBuilder
##### String Method
  - variableName.charAt(positionNumber) 
  - length()
  - toString()
  - "ABC".equalsIgnoreCase("abc")
  - "abcdefghij".substring(3,7)) ; //defg
  - "abcdefghij".substring(3); //cdefghi
  

#####String Manipulation methods 
String object cannot be modified. When any of the following methods are called, they return a new String with modified value. The original String remains unchanged. 
- concat
- replace
- toLowerCase
- toUpperCase
- trim

#####String Concatenation Rule
 - Expressions are evaluated from left ro right except if there are parenthesis 
 - number + number = number
 - number + String = String 
 
#####Increment and Decrement Operation
  - ++, --
   
#####Relational Operators
  - >, <, >=, <=, ==, !=
#####Logical Operators
  - &&, ||, ^, !, &, |
 ###Arrays
 ```
     int[] marks;
     marks = new int[5];
     int marks2[] = new int[5];
     Arrays.fill(marks,100);// all values will be 100
     String[] daysOfWeek={"Sat","Sun","..."};
```
```
    int[][] matrix = {{1,2,3},{4,5,6}};
    int[][] matrixA = new int[5][6];
    //loop through
    for(int[] array: matrix){
        for(int number: array){
              //sout number
        }
    } 
    System.out.println(Arrays.deepToString(matrix)); 
    //Arrays.equals(arr1,arr2);
    //Arrays.sort(arr);
    //Arrays.toString(arr);
    //The first dimension of 2d array is mandatory
```
#####if-else
  - if, else, else if, switch, case, default, break
#####loops
  - while, for, do while, for( type variableName: variableList){},
#####break & continue
  - break, continue
###Enum
 - a list of valid values for a type
 ``` 
 enum Season{
    WINTER, SPRING, SUMMER, FALL
 };
 
 //inside methods
 
 Season season = Season.valueOf("FALL");
 System.out.println(season.name());
 System.out.println(season.FALL.ordinal());//3
 
 Season season1 = Season.AFLL; 
 for(Season s: Season.values()){
    System.out.println(s.name());
 }
 
 enum SeasonCustomized{
    WINTER(1){
        public int getExpectedMaxTemp(){
            return 5;
        }
    }
    
 }
 //this feature is called constant class
 ```
 ``` 
 enum Ids {
   OPEN(100),
   CLOSE(200);
 
   private int value;    
 
   private Ids(int value) {
     this.value = value;
   }
 
   public int getValue() {
     return value;
   }
 }
 ```
 
 ###Inheritance 
 
```
public class Actor{

}
public class Hero extends Actor{

}
public class Comedian extends Actor{

}

//inside method
Actor actor1 = new Actor();
Actor actor2 = new Comedian();
//Super class reference variable can hold an object of sub class

//Object is super class of all classes. So, an Object reference variable can hold an instance of any class

Object object = new Hero();

//subclass method cannot be invoked by superclass reference variable
```
  > Super Class can hold an object of subclass - cannot invoke sub class method with super class reference variable 
    
  > Multiple inheritance is not possible so create an inheritance chain
  
  
  
  
##### Inheritance and Polymorphism
Same code having Different Behavior
  ``` 
    Animal animal = new Animal();
    Animal dogAnimal = new Dog();
  ```

    
###Class, Object, State & Behavior
Class - template
Object- instance of class
State - value 
Behavior - supported method
#####toString method
- used to print content of an object

#####equals method
- used to check if two objects have same content
  ``` 
    Client client1 = new Client(25);
    Client client2 = new Client(25);
    
    client1.equals(client2);// true
  
  ```

#####hashCode method
  - used in hashing to decide which group(or bucket) an object should be placed into

###Abstract Class
- abstract class cannot be instantiated
- abstract class can contain instance and static variable 
- abstract method does not contain body
- abstract method can be declared only in Abstract class
- abstract class can contain no-abstract methods
- a concrete sub class should implement all abstract methods
  - an abstract sub class need not implement all abstract method
- an abstract sub class need not implement all abstract methods
- variable cannot be abstract
- abstract methods cannot be paired with final or private access modifier
###Constructors
  - invoked whenever an instance(object) of a class is created
#####default constructors
#####creating constructor
#####no argument constructor
#####calling super class constructor
A constructor can invoke another constructor, or a super class constructor, but only as first statement in the constructor
> super() // must be first statement in constructor
 - super class no argument constructor is called automatically 
 - this() must be first statement in constructor
 
### Coupling
  - how a class is dependent on other class
  - there should be minimal dependencies between classes
   
### Cohesion
  - measure of how related the responsibilities of a class are. A class must be cohesive i.e. its responsibilities should highly related to one another. 
  ``` 
    class DownloadAndStore{
        void downloadFileFromInternet();
        void parseData();
        void storeIntoDatabase();
    }
    
    // ------------ as the responsibility of the classes are not related ------------------
    // better way of approaching would be using classes have their own responsibility
    
    class InternetDownloader{ void downloadFileFromInternet();}
    class parsedData{ void parsedData();}
    class storeIntoDatabase{ void storeIntoDatabase();}
    
    class DownloadAndStore{
        void doEverything(){
          new InternetDownloader().downloadFileFromInternet();
          new parseData().parseData();
          new storeIntoDatabase().storeIntoDatabase();
        }
    }
    
  ```    
    
### Encapsulation 
 - in class we can use get, set so that there is no necessity to know that there is a variable
##### Interface 
 - defines a contract for responsibilities( method ) of a class. 
 - interface can contain abstract method - not true any more
 ```java
 public abstract interface Flyable{public abstract void fly();} 
 public class Aeroplane implements Flyable{@override public void fly(){System.out.println("Aeroplane Flying");}}
 public class Bird implements Flyable{@override public void fly(){System.out.println("Bird flying");}}
 
 //------------------ An interface reference variable can hold objects of any implementation of interface 
 Flyable flyable1 = new Bird();
 Flyable flyable2 = new Aeroplane();
 
 ```
 - variables in interface are always public, static, final
 - methods in interface are by default public abstract 
 - one interface can extend another interface 
 - class implementing multiple interface need to implement all the methods of all interface unless the class is an abstract class. 
 
##### Method Overloading
    
    
    
    
    
    
    
    
    