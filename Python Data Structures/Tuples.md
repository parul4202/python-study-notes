
## Tuples 
* collection of Python objects much like a list but Tuples are immutable in nature i.e. the elements in the tuple cannot be added or removed once created
* Tuples can also be created with a single element, but it is a bit tricky. Having one element in the parentheses is not sufficient, there must be a trailing ‘comma’ to make it a tuple.
--------------------------------------------------

## Creating a Tuple with the use of ***Strings***

```
Tuple = ('Make', 'Sure')
print("\nTuple with the use of String: ")
print(Tuple)
```

## Creating a Tuple with the use of **List**

```
list1 = [1, 2, 4, 5, 6]
print("\nTuple using List: ")
Tuple = tuple(list1)
```

## Accessing element using indexing
```
print("First element of tuple")
print(Tuple[0])
```
--------------------------------------------------------

 To convert the two list into tuple we use zip() method and after it we can unpack the tuble after looping over the tuple list.
## enumerate():  
The function returns the index of the list item you are currently on in the list and the list item itself.* 
>- Syntax: enumerate(iterable, start=0)

```
l1 = zip(a, b)

using for loop- 
for number, name in enumerate(l1):
    name_a, name_b = unpacked_tuple
print(f'Number {number+1}: {name_a} and {name_b}')

```