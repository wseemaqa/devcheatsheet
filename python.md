---
Title: Python
Description: Python cheatsheet containing useful code snippets and documentation.
---

## Basics

### Display
```py
print("Hello World")
```
### Comments

* `#` is used to comment a line in Python

## Data Types

|Category|Data Types|
|----|------|
|Text |str|
|Number|int, float, complex|
|Boolean|bool|
|Binary|bytes, bytearray, memoryview|
|Set|set, frozenset|
|Sequence|list, tuple, range|
|Mapping|dict|

* type() is used to know the data type of a variable

### Type casting

|Constructor function| Description|
|-----|----|
|int()| constructs an integer from any form of data like string, float or integer|
|float()|constructs a float number from any form of data like string, float or integer|
|str()|constructs a string from any form of data like string, float or integer|

## Variables

In Python, declaring variables is not required.

## Operators

|Type|Operators|
|----|----|
| Arithmetic Operators| +  -  *  /  %  **  //|
| Relational Operators| ==  !=   >  >=  <  <=|
| Bitwise Operators| &  ^  \| ^ ~ << >> |
| Logical Operators| &&  \|\| ! |
| Assignment Operators|=  +=  -=  *=  /=  %=  **=  //=|
| Membership Operators| in, not in |
| Identity Operators | is, is not|


## Functions

```py
# declaring a function
def function-name(parameters){ # parameters are optional
    #code
}
function-name(parameters) # calling a function
```
## Collections

### 1. List

List is ordered collection of items and can be changed. `[]` are used to represent lists. List is mutable.

### Example
```py
mylist=["Mango","Banana","Apple"]
print(mylist[1]) # prints Banana
print(mylist[7]) # throws IndexError : list index out of range
print(mylist[-3]) # prints Mango
```
### Operations

|Operation|Description|
|----|----|
|lst.append(val)| add an item to list at end|
|lst.extend(seq)| add sequence of items to list at end|
|lst.insert(index,val)| insert an item at given index|
|lst.remove(val) | remove first item with value val|
|lst.pop(`[index]`)→value| remove & return item at index|
|lst.sort()| sort the given list items|
|lst.reverse() |reverse the given list items|

### 2. Tuple

Tuple is ordered collection of items and can't be changed. `()` are used to represent Tuples. Tuple is immutable.

### Example

```py
myTuple = ["iPhone","Pixel","Samsung"]
print(myTuple[0]) # prints iPhone
print(myTuple[7]) # throws IndexError: tuple index out of range
print(myTuple[-1]) # prints Samsung
```

### 3. Set

Set is unordered collection of items and it is unindexed. `{}` are used to represent sets. Set is mutable.

### Example

```py
mySet = {"iPhone", "Pixel", "Samsung"}
mySet.add('OnePlus')
print(mySet) # prints {'iPhone', 'Samsung', 'OnePlus', 'Pixel'}
```
### Operations

|Method | Description | Usage |
|----|----|----|
|add() | to add an element to the set |mySet.add('value')|
|clear()| to remove all the elements from the set | mySet.clear()|
|pop() | to remove last element from the set| mySet.pop()|
|remove() | to remove a specified element from the set|mySet.remove("value")|
|del()| to delete a set| del myset|
|copy()	| to return a copy of the set| copySet = mySet.copy()|
|union() |	to return a set containing the union of sets|  mySet3 = mySet1.union(mySet2)|
|update() | to update the set with the union of this set and others| mySet1.update(mySet2)|

### 4. Dictionary
Dictionary is a collection of key value pairs which is unordered, can be changed, and indexed. They are written in curly brackets with key - value pairs. Dictionary is mutable.

### Example
```py
mydict = {
    "brand" :"iPhone",
    "model": "iPhone 11"
}
val = mydict["brand"]
print(val) # prints iPhone
```
|Operation|Description|
|----|----|
|`d[key]`=value| To add a new key-value pair to dictionary or to change it's value if key is existing|
|d.copy()| Returns a copy of the dictionary|
|d.keys()|Returns a list containing all the dictionary's keys|
|d.values()|Returns a list of all the values in the dictionary|
|d.items()|Removes the element with the specified key|
|d.clear()| To empty the dictionary items.|
|del `d[key]`| To remove an item from a dictionary.
|d.pop(key)|To remove an item from a dictionary.|
|d.popitem()|removes the item that was last inserted into the dictionary|
|d.get(key)| Returns the value of the specified key|
|d.setdefault(key)|Returns the value of the specified key. If the key does not exist then returns the default value provided|

## Conditional Statements

### 1. If

```py
if conditional-expression :
    #code
```
### 2. If-else
```py
if conditional-expression :
    #code
else :
    #code
```
### 3. If-elif-else Ladder

```py
if conditional-expression :
    #code
elif conditional-expression :
    #code
else :
    #code
```

## Loops

### 1. For
For loop is used to iterate over arrays(list, tuple, set, dictionary) or strings.

### Syntax
```py
for variable in arrays :
    #code
```
### 2. While
```py
while condition : 
    #code 
```
## String Methods
||||
|----|----|----|
|str.strip()|str.lower()|str.upper()|
|str.replace("str to be replaced","new string to replace")|str.split("seperator")|len(str)|
|+ for concatenation|str.count(substr)|str.find(substr)|
|str.index(substr, start, end)|str.join(array)|str.partition(substr)|
|str.zfill(len)|str.swapcase()|str.isdecimal()|
|str.isdigit()|str.islower()|str.isupper()|
|str.endswith(value, start, end)|str.startswith(value, start, end)|str.isspace()|

