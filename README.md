# Data-Structures
Overview and explanation of data structures in python. This is perfect review material for technical interviews!

Resources:
  - https://realpython.com/python-data-structures/
  - https://docs.python.org/3/tutorial/datastructures.html

# Contents
  - [Lists](#Lists)
  - [Tuples](#Tuples)
  - [Sets](#Sets)
  - [Dictionaries](#Dictionaries)
  - [Linked-Lists](#Linked-Lists)
  - [Stacks](#Stacks)
  - [Queues](#Queues)
  - [Priority Queues](#Priority-Queues)

# Lists

  The list is a most versatile datatype available in Python which can be written as a list of comma-separated values (items) between square brackets. An advantage of using a     list is that iems in a list do not need to be of the same type.
  
  ## Functions:
  ```python
  - list.append(x)
      Add an item to the end of the list. Equivalent to a[len(a):] = [x].


  - list.extend(iterable)
      Extend the list by appending all the items from the iterable. Equivalent to a[len(a):] = iterable.


  - list.insert(i, x)
      Insert an item at a given position. The first argument is the index of the element before 
      which to insert, so a.insert(0, x) inserts at the front of the list, and 
      a.insert(len(a), x) is equivalent to a.append(x).


  - list.remove(x)
      Remove the first item from the list whose value is equal to x. It 
      raises a ValueError if there is no such item.


  - list.pop([i])
      Remove the item at the given position in the list, and return it. If no index is 
      specified, a.pop() removes and returns the last item in the list. (The square brackets 
      around the i in the method signature denote that the parameter is optional, not that
      you should type square brackets at that position. 


  - list.clear()
      Remove all items from the list. Equivalent to del a[:].


  - list.index(x[, start[, end]])
      Return zero-based index in the list of the first item whose value is equal 
      to x. Raises a ValueError if there is no such item.

      The optional arguments start and end are interpreted as in the slice notation 
      and are used to limit the search to a particular subsequence of the list. The
      returned index is computed relative to the beginning of the full sequence 
      rather than the start argument.


  - list.count(x)
      Return the number of times x appears in the list.


  - list.sort(*, key=None, reverse=False)
      Sort the items of the list in place (the arguments can be used for sort 
      customization, see sorted() for their explanation).


  - list.reverse()
      Reverse the elements of the list in place.


  - list.copy()
      Return a shallow copy of the list. Equivalent to a[:].
   ```
  
   ## Examples

  ```python
  # Creating a list
  >>> arr = ["one", "two", "three"]
  >>> arr[0]
  'one'


  # Printing a list 
  >>> arr
  ['one', 'two', 'three']


  # Lists are mutable:
  >>> arr[1] = "hello"
  >>> arr
  ['one', 'hello', 'three']


  # You can easily delete elements from a list with the del command
  >>> del arr[1]
  >>> arr
  ['one', 'three']


  # Lists can hold arbitrary data types:
  >>> arr.append(23)
  >>> arr
  ['one', 'three', 23]
  
  ```
  
  ```python
  >>> fruits = ['orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana']
  >>> fruits.count('apple')
  2
  
  
  >>> fruits.count('tangerine')
  0
  
  
  >>> fruits.index('banana')
  3
  
  
  >>> fruits.index('banana', 4)  # Find next banana starting a position 4
  6
  
  
  >>> fruits.reverse()
  >>> fruits
  ['banana', 'apple', 'kiwi', 'banana', 'pear', 'apple', 'orange']
  
  
  >>> fruits.append('grape')
  >>> fruits
  ['banana', 'apple', 'kiwi', 'banana', 'pear', 'apple', 'orange', 'grape']
  
  
  >>> fruits.sort()
  >>> fruits
  ['apple', 'apple', 'banana', 'banana', 'grape', 'kiwi', 'orange', 'pear']
  
  
  >>> fruits.pop()
  'pear'
 ```
 
 # Tuples
 
  A tuple is a collection of objects which ordered and immutable. Tuples are sequences, just like lists. The differences between tuples and lists are, the tuples cannot be       changed unlike lists and tuples use parentheses, whereas lists use square brackets.
  
  ```python
  #Example useage
  tup1 = ('physics', 'chemistry', 1997, 2000);
  tup2 = (1, 2, 3, 4, 5 );
  tup3 = "a", "b", "c", "d";
  
  
  >>> tup = ("one", "two", "three")
  >>> tup[0]
  'one'


  # Tuples have a nice repr:
  >>> tup
  ('one', 'two', 'three')


  # Tuples are immutable:
  >>> tup[1] = "hello"
  Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
  TypeError: 'tuple' object does not support item assignment


  >>> del tup[1]
  Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
  TypeError: 'tuple' object doesn't support item deletion


  # Tuples can hold arbitrary data types:
  # (Adding elements creates a copy of the tuple)
  >>> tup + (23,)
  ('one', 'two', 'three', 23)
  
  ```
