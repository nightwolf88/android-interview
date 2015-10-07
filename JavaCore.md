##String, StringBuffer, StringBuilder
* *String:* is immutable String, it cannot change
* *StringBuffer:* is mutable String, it synchronized (safe thread)
* *StringBuilder:* is mutable String, it not synchronized (not safe thread)

##Java collection

Dynamic array for storing the elements, can contain duplicate elements, can maintain insert order, non synchronized, allow random access.

1. **ArrayList & LinkedList**

	ArrayList and LinkedList both implements List interface and maintains insertion order. Both are non synchronized class.
	
	But there are many differences between ArrayList and LinkedList class that are given below:
	
	| ArrayList | LinkedList |
	|-----------|------------|
	|ArrayList uses dynamic array to store the elements| LinkedList uses double linked list to store the elements.|
	|Manipulation with ArrayList is slow because it internally uses array. If any element is removed from the array, all the bits are shifted in memory| Manipulation with LinkedList is faster than ArrayList because it uses doubly linked list so no bit shifting is required in memory|
	|ArrayList class can act as a list only because it implements List only| LinkedList class can act as a list and queue both because it implements List and Deque interfaces.|
	|ArayList is better for storing and accessing data| LinkedList is better for manipulating data|
	

* *ArrayList:* 
* *LinkedList:*


###Type of memory areas allocated by JVM

### Garbage collector

###Synchronized

### Java networking

###Thread

###IO

###Exception

###Concurrency