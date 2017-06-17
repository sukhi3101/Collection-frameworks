# Collection-frameworks my first presentation given to Sakthi sir.
                       COLLECTION FRAMEWORKS.

In this word document we are going to look into collection frameworks to try and understand what its all about.

Arrays- An array is a collection of similar type of elements stored in                           continuous memory locations

Types
one dimensional arrays
 multi dimensional arrays

One Dimensional Arrays
Declaration
syntax
datatype[] arrayname;
  or
datatype arrayname[];

eg:
int[] n;
int n[];

int n[5];//Error

Memory Allocation
int[] n = new int[5];

Note:
In Java if we try to access an array out of index, then it will throw an
exception (runtime error)

In Java arrays are passed as call-by-reference
eg:
main()
{
   int[] n = {10,20,30,40,50};
   change(n);
   SOP(n[2]);//25
}
change(int[] n)
{
  n[2] = 25;
}

Multidimensional arrays
- It is used to collect the elements in the form of rows and columns
- In Java multidimensional arrays are also known as array of arrays
Declaration
syntax
datatype[][] arrayname;
  or
datatype arrayname[][];
  or
datatype[] arrayname[];

eg:
int[][] n;
int n[][];
int[] n[];

int n[3][3];//Error

Memory Allocation
int[][] n = new int[3][3];

labelled break and continue
eg:
x:
SOP("xx");//Error
while(cond)
{
    .....
    ....
    while(cond)
    {
	...
	...
	break x;
        ...
	...
    }
    .....
    .....
}

x:
while (cond)
{
    ....
    ....
    while (cond)
    {
	...
	...
	continue x; 
	...
	...
    }
    ....
    ....
}


Note:
After label we can have only the loop statements
Collections Framework
Collections are used to collect the elements of variable size (not fixed)

Arrays vs Collections

- Arrays are used to collect the elements of fixed size where as collections are used to collect the elements of variable size
- In Arrays we can collect only similar type of elements where as in Collections we can collect different type of elements
- In Arrays we can collect primitive type as well as reference type of elements where as in Collections we can collect only reference type of elements

Collection vs Map
 Collection is a collection of elements where as Map is a collection of key-value pairs
 Collection allows duplicate elements where as Map does not allow duplicate keys

List vs Set
List is ordered where as Set is unordered
             List allows duplicate elements where as Set does not allow duplicate elements

ArrayList vs LinkedList

 In ArrayList the elements are stored in continuous memory locations where as in LinkedList the elements are stored in non-continuous memory locations
 The cost of insert and delete operations are more in ArrayList where as the cost these operations are less in LinkedList

Stack
               A Stack is a collection of elements in the form of Last In First Out(LIFO)

Operations on Stack
 push() - inserts an element at top into the stack
 pop() - deletes an element at the top of the stack
 peek() - returns the top element of the stack
 empty() - returns true if stack is empty

ArrayList vs Vector

 In ArrayList the methods are not synchronized where as in Vector the methods are synchronized
 ArrayList is not thread-safe where as Vector is thread-safe

HashSet

 HashSet is unordered and no duplicate elements

LinkedHashSet
             LinkedHashSet is ordered and no duplicate elements

TreeSet
             TreeSet is sorted and no duplicate elements

HashMap
 HashMap is unordered based on keys and no duplicate keys

HashMap vs Hashtable

In HashMap the methods are not synchronized where as in Hashtable the      methods are synchorized
- HashMap is not thread-safe where as Hashtable is thread-safe
  LinkedHashMap
 LinkedHashMap is ordered based on keys and no duplicate keys
TreeMap
             TreeMap is sorted based on keys and no duplicate keys

Methods of List interface

- boolean add(Object) - adds an element at the last
- void add(int,Object) - adds an element at the given index/position
- void set(int,Object) - modifies an element at the given index
- boolean remove(Object) - deletes the given element
- Object remove(int) - deletes an element at the given index
- Object get(int) - returns the element at the given index
- int size() - returns the number of elements

             Additional Methods in LinkedList
             - addFirst()
- addLast()
- removeFirst()
- removeLast()

Traversing-
Accessing every element of list/set is called as traversing
Iterator interface-
Iterator interface is used to traverse the elements of list/set from first to last
Methods-
- boolean hasNext()
- Object next()

ListIterator interface
             - ListIterator extends Iterator
- ListIterator interface is used to traverse the elements from first to last as well as last to first

Methods
- boolean hasPrevious()
- Object previous()

            Using Generics in Collections
             - Generics are used to manage different data types
- Using Generics in collections we can store only similar type of elements
- When Generics are used in collections we can traverse the elements of list/set using Enhanced for loop

Stack class-
             Stack is a collection of elements in the form of Last In First Out (LIFO) operations

Methods of Stack class
            - push() - inserts an element at the top of the stack
             - pop()  - deletes the element at the top of the stack
- peek() - returns the top element from the stack
- empty()- returns true if the stack is empty

            Vector class
             - Vector is a collection of elements stored in continuous memory locations
- The methods in Vector are synchronized

Enumeration interface
             - It is used to traverse the elements of list/set
- The methods present in Enumeration are synchronized

Methods
             - boolean hasMoreElements()
- Object nextElement()

Set interface
- Set is used to collect the elements and these elements are unordered
- Set does not allow duplicate elements

Classes under Set
- HashSet => unordered and no duplicate keys
- LinkedHashSet => ordered and no duplicate keys
- TreeSet => sorted and no duplicate keys

Note:

In TreeSet all the elements should be same type else it will throw     ClassCastException

In order the arrage the elements in TreeSet, it uses binary search tree

Map interface
- Map is used to collect the elements in the form of key-value pairs
- Map does not allow duplicate keys

Classes under Map interface
- Hashtable - unordered based on keys and no duplicates, synchronized
- HashMap - unordered based on keys and no duplicate keys
- LinkedHashMap - ordered based on keys and no duplicate keys
- TreeMap - sorted based on keys and no duplicate keys

Iterating Maps
- Convert Map into Set
	eg:
	HashMap hm = new HashMap();
	Set s = hm.entrySet();//converts Map into Set

	One key-value pair of Map will convert as one element in Set

- Iterate the converted Set
	Iterator iter = s.iterator();
	while (iter.hasNext())
	   SOP(iter.next());

Map.Entry interface
- This interface is used to get the keys and values from the converted Set

Methods
- getKey()
- getValue()
Comparator interface
- Comparator interface is used to arrage the elements of TreeSet in binary search tree.

interface Comparator 
{
   int compare(Object o1,Object o2);
}

class TreeSet implements Comparator
{
   public int compare(Object o1,Object o2)
   {}
}

	

Utility Classes

- Arrays
- StringTokenizer
- Date
- Calendar

Arrays class

- It is used to for the following
	- sorting the elements of array
	- searching an element in the array
	- to convert an array into list

Methods

- sort()
- binarySearch()
- asList()

	
StringTokenizer class
- It is used to divide the given string into sub strings (tokens)based on given symbol/char
- StringTokenizer implements Enumeration interface


     Date and Calander classes
     - These classes are used to manage the dates and times
