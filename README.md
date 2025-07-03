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

