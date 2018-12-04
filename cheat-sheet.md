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

```

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
    
```
##### basic puzzles
``` 

```

### Casting - Implicit and Explicit
##### Implicit Casting
##### Explicit Casting

### Operator
##### Assignent
##### Remainder
##### Conditional
###Passing Variable to Methods 

###Types of Variables

###Scope of Variable

### Variable Initialization

### Wrapper Class
####Wrapper Class Utility Methods
 - valueOf
 - xxxValue
 - parseXxx
 - toString
###String Class 
##### String are Immutable
### String vs StringBuffer vs StringBuilder
Immutable - String  
Thread Safe - String, StringBuffer
Performance - StringBuilder

#####String Manipulation methods 
String object cannot be modified. When any of the following methods are called, they return a new String with modified value. The original String remains unchanged. 
- concat
- replace
- toLowerCase
- toUpperCase
- trim

#####String Concatenation Rule
 - Expressions are evaluated from left ro right except if there are parenthesis 
 
 #####Increment and Decrement Operation
 
 #####Relational Operators
 #####Logical Operators
 ###Arrays
 ```
     int[] marks;
     marks = new int[5];
     int marks2[] = new int[5];
     Arrays.fill(marks,100);
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
#####loops
#####break & continue
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
##### Inheritance and Polymorphism
Same code having Different Behavior

    
###Class, Object, State & Behavior
Class - template
Object- instance of class
State - value 
Behavior - supported method
#####toString method
- used to print content of an object

#####equals method
#####hashCode method

###Abstract Class
- abstract class cannot be instantiated
- abstract class can contain instance and static variable 
- abstract method does not contain body
- abstract method can be declared only in Abstract class
- abstract class can contain no-abstract methods
- a concrete sub class should implement all abstract methods
- an abstract sub class need not implement all abstract methods
- variable cannot be abstract
- abstract methods cannot be paired with final or private access modifier
###Constructors
#####default constructors
#####creating constructor
#####no argument constructor
#####calling super class constructor
A constructor can invoke another constructor, or a super class constructor
    
    
    
    
    
    
    
    
    
    