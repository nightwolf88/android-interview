##String, StringBuffer, StringBuilder

||String | StringBuffer | StringBuilder|
-----|------|------|--------
**Storage area** | Constant String Pool | Heap | Heap 
**Modifiable** | No (immutable) | Yes (mutable) | Yes (mutable)
**Thread Safe** | Yes | Yes | No
**Performance** | Fast | Very slow | Fast

##Java collection
1. **Basic interfaces of Java Collections Frameworks**

	Java collection which represents a group of objects know as its elements
	
	|Interface|Brief Description| Derived class|
	|-----|-----|-----|
	|Set|Which is a collection that cannot contain duplicate elements|HashSet, LinkedHashSet, TreeSet|
	|List|Which is an ordered collection and can contain duplicate elements|ArrayList, LinkedList, Vector|
	|Queue|Collection with rule: First in - First out|PriorityQueue|
	|Map|Which is an object that maps keys to values and cannot contain duplicates keys|HashMap, LinkedHashMap, HashTree, HashTable|

1. **ArrayList & LinkedList**

	ArrayList and LinkedList both implements List interface and maintains insertion order. Both are non synchronized class.
	
	But there are many differences between ArrayList and LinkedList class that are given below:
	
	ArrayList|LinkedList
	----------- | ------------
	ArrayList uses dynamic array to store the elements| LinkedList uses double linked list to store the elements.
	Manipulation with ArrayList is slow because it internally uses array. If any element is removed from the array, all the bits are shifted in memory| Manipulation with LinkedList is faster than ArrayList because it uses doubly linked list so no bit shifting is required in memory
	ArrayList class can act as a list only because it implements List only| LinkedList class can act as a list and queue both because it implements List and Deque interfaces.
	ArayList is better for storing and accessing data| LinkedList is better for manipulating data

1. **HashSet, TreeSet (HashMap, TreeMap)**

	HashSet/HashMap | TreeSet/Treemap
	--- | ---
	Performance better | Performance slower
	Non ordered | Ordered
	Compare element to dertemite unique using compare value | Compare using Comparator or Comparaable

1. **Differences between HashMap and HashTable**

	HashMap | HashTable
	--- | ---
	Non synchronized | Synchronized
	Allows one null key and multiple null values | Doesn't allow any null key or value
	Fast | Slow
	Traversed by Iterator | Traversed by Enumerator and Iterator

1. **Iterator**

	Iterator using for iterate collection with structure complex as Tree (Iterate by index do not work).

	The differences between Iterator and ListIterator
	
	Iterator | ListIterator
	--- | ---
	Uses to traverse the Set and List Collections | Uses to iterate only over List
	Traverse a collection only in forward direction | Travarse a List in both directions
	
###Type of memory areas allocated by JVM

* ***Heap memory:*** which is the storage for Java objects and arrays. Heap memory for objects is reclaimed by garbage collector. The heap
* ***Non-Heap memory:*** which is used by Java to store, loaded classes and other meta-data, primitive data
	

### Garbage collector

Là bộ quản lý: cấp phát, thu hồi bộ nhớ. Khi một đối tượng tạo ra, GC sẽ cấp phát bộ nhớ cho đối tượng đó, và khi đối tượng không tham chiếu nào đến nữa, GC sẽ thu hồi bộ nhớ đã cấp phát cho đối tượng đó.

### Các loại tham chiếu trong Java
1. **Strong Reference:** là kiểu tham chiếu thường dùng nhất với kiểu phép gán =. Đối với Strong Reference là một liên kết mạnh, khi mà đối tượng còn có một tham chiếu đến nó thì đối tượng đó không thể giải phóng với bất kì hình thức nào
2. **Soft Reference:** là kiểm tham chiếu mà đối tượng sẽ bị giải phóng khi thiếu bộ nhớ. Kiểu tham chiếu này thường dùng để cache đối tượng
3. **Weak Reference:** 
4. **Phantom Reference:**

###Synchronized

Một phương thức chỉ được gọi một lần duy nhất tại một thời điểm, multiple thread, thread safe

###Thread

Thread là một tiến trình tách ứng dụng ra một hoặc nhiều luồng khác nhau để cùng thực hiện nhiều nhiệm vụ cùng một lúc. Khi lập trình, công việc nào tốn nhiều time thì tách ra một thread riêng để main thread không bị gián đoạn.

###Exception

Một exception là một vấn đề phát sinh trong quá trình thực hiện chương trình, có thể xảy ra với nhiều lí do khác nhau. Khi một exception như vậy xảy ra nếu không được xử lý thì sẽ làm cho chương tình ngừng hoạt động, không cho kết quả thực thi như mong muốn.