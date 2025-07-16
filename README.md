Operators:
->Operators are the pre-defined symbols used to perform operations on the operands.
->Operators give 2 types of results: *value and *type of the value

ex: int a = 10, b = 20;
    int c = a + b;
    System.out.println(c);//30

    Here, 30 is the value and type of 30 is int.

Operators can be categorized into 2 types:
->Based on number of operands and
->Based on operations.

	1) Based on number of operands : i) Unary
 					 ii) Binary
       					 iii) Ternary

        2) Based on operations : i) Arithmetic Operations
				ii) Increment/Decrement
     			       iii) Comparision/Relation
	       			iv) Logical Operations
	   			 v) Bitwise Operations
				vi) Compound Assignment Operations

1) Arithmetic Operations: (+,-,*,/,%)
   -> All are binary operators

2) Increment/Decrement:
   -> It is a Unary operator
   -> Basically 2 types of  Increment: post-increment and pre-increment
   	pre-increment: It is incremented before its use.
   	post-increment: It is used and then incremented.

   -> Basically 2 types of  Decrement: post-decrement and pre-decrement
   	pre-decrement: It is decremented before its use.
   	post-decrement: It is used and then decremented.
   
   ex: 
		int a=5,b=7;
		int c= a+++b++ + ++a+b++;
		System.out.println(c);//27
so, when we are incrementing the variables, it first 


Q) Differences between primitive and non-primitive
A)
Primitive data structure	
  Primitive data structure is a kind of data structure that stores the data of only one type.
  Examples of primitive data structure are integer, character, float.	
  Primitive data structure will contain some value, i.e., it cannot be NULL.	
  The size depends on the type of the data structure.	
  It starts with a lowercase character.	
  Primitive data structure can be used to call the methods.	

Non-primitive data structure
  Non-primitive data structure is a type of data structure that can store the data of more than one type.
  Examples of non-primitive data structure are Array, Linked list, stack.
  Non-primitive data structure can consist of a NULL value.
  In case of non-primitive data structure, size is not fixed.
  It starts with an uppercase character.
  Non-primitive data structure cannot be used to call the methods.

Q) Can we have nested blocks in synchronization
A)
  Nested blocks in synchronization can be implemented using locks or mutexes, ensuring consistent locking order and proper resource release. Use try-finally blocks to   guarantee lock release. This approach helps prevent deadlocks and ensures thread safety.

  ex: synchronized (outerLock) {
    // Outer critical section
    synchronized (innerLock) {
        // Inner critical section
    }
}

Q) ARRAY:
A)
  A big amount of memory which consists of sub-divisions. It is homogenous in nature. Array size is immutable.
  ->int[] a= new int[-10];
    System.out.println(a); //Exception in thread "main" java.lang.NegativeArraySizeException: -10
  	at Code/Snippets.A1.main(A1.java:9)

->int[] b= new int['a'];
	System.out.println(b); //[I@378fd1ac

->int[] b= new int["s"];
	System.out.println(b);//CTE

 ->int[] b= new int[0];
	System.out.println(b);//[I@378fd1ac

 ->	int[] b= new int[true];
	System.out.println(b);//CTE

  STRING:
  valueof() is present in String class, it is a static method as it is called from its class and its return type is String.
  char[] c= {'S','R','I','R','A','M'};
System.out.println(c);//SRIRAM
char[] invokes String.valueof(), it traverse the entire [] and concats it into a String
->	
	System.out.println(String.valueOf(b));//[I@378fd1ac

toString()
->System.out.println(Arrays.toString(b));//[0, 0, 0, 0, 0, 0, 0, 0, 0, 0]

TYPE CASTING:


UP-CASTING:
It is nothing but storing the sub class object super class reference
Here all the super class elements are visible and accissible
Is-a-relationship is mandatory 
It is implicit
ex:- Iterator

DOWN-CASTING:
In order to acheive down casting, upcasting is mandotory. Without Up-casting if we perform down casting it results in CLASSCASTEXCEPTION
Here both the super and sub class elements are visible and accissible
It is explicit
ex: Cloneable Interface which is predefinrd

Ex: 
public class Sup1 {
int s1=5;
void eat() {
	System.out.println("EAT");
}
}

public class Sub1 extends Sup1{
int s2=10;
void drink() {
	System.out.println("DRINK");
}
}

public class Renner1 {
public static void main(String[] args) {
	Sup1 s=new Sub1();                //UP CASTING
	System.out.println(s.s1);
	s.eat();

}
}


public class Renner1 {
public static void main(String[] args) {
	Sup1 s=new Sub1();                //UP CASTING
	System.out.println(s.s1);
	s.eat();
	Sub1 sl=(Sub1) new Sup1();                  //DOWN CASTING
	System.out.println(sl.s1);
	System.out.println(sl.s2);
	sl.eat();
	sl.drink();
}
}

Now, if we downcast without upcasting

public class Renner1 {
public static void main(String[] args) {
	Sub1 sl=(Sub1) new Sup1();                  //DOWN CASTING
	System.out.println(sl.s1);
	System.out.println(sl.s2);
	sl.eat();
	sl.drink();
}
}

O/P:Exception in thread "main" java.lang.ClassCastException: class Snippets.Sup1 cannot be cast to class Snippets.Sub1 (Snippets.Sup1 and Snippets.Sub1 are in module Code of loader 'app')
	at Code/Snippets.Renner1.main(Renner1.java:9)


WRAPPER CLASSES:
These are the utility classes used for boxing and unboxing
All these Wrapper classe are implemented by Comparable Interface
Also known as Non primitive data type of the data type
All the primitive data type includes toString(),hashCode(),equals()
There are basically 2 ways to Boxing:

1)By using Wrapper Class:
   public class Wrap1 {
	public static void main(String[] args) {
		int a = 1;
		Integer i = a;
		System.out.println(i);
	}
}

2) By using Constructor:
   package Snippets;

public class Wrap1 {
	public static void main(String[] args) {
		int a = 1;
		Integer i = new Integer(a);
		System.out.println(i);
	}
}

