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

