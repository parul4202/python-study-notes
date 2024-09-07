# Data structures:
Data Structures are a way of organizing data so that it can be accessed more efficiently depending upon the situation.we'll use these containers to store our data for aggregation, order, sorting, and more. Python provides several container sequences such as lists, sets, and tuples



## List 
hold an ordered collection of items, and lists allow us to do just that. Lists are mutable so we can add or remove data from them. Lists also allow us to access an individual element within them using an index


### One dimentional list

``` 
list_1 = ['a', 'b', 'c']

```

### Multidimentional list

```
List2 = [['Best', 'For'], ['Python']] 
print("\nMulti-Dimensional List: ") 
print(List2) 

```

### Append d in list

```
list = ['a', 'b', 'c']
list.append('d')
print(list)
```

### Find the index of c

```
list.index[2]
print(list)

or 

print(list[2])

```


### Combining lists:
#### using operators we can combine to list 

```
list_1 = ['a', 'b', 'c']
list_2 = ['d', 'e', 'f']

combined = list_1 + list_2
print(combined)

```

### zip method

```
list_1 = ['a', 'b', 'c']
list_2 = ['d', 'e', 'f']

zipped = zip(list_1, list_2)
print(zipped)

```

### extend() method

 use the .extend() method on the list to combine two lists effectively appending all the values from a second list
    >>- extend method take only one argument or one list.

```
list_1 = ['a', 'b', 'c']
list_2 = ['d', 'e', 'f']
lists = list_1.extend(list_2)
print(lists)

or

list_1.extend(['d', 'e', 'f'])
print(list_1)

```

## Finding elements in a list
>- .index() method locate the position of element in the data or list

```
list_1 = ['a', 'b', 'c']
lists = list_1.index('c')
print(lists)

```
-------------------------------------------------------------------
## Removing elements in a List
knowing index of the element help us to remove elemets from thee list 
>- using .pop() method
>- .pop() use with the main list 
```
list_2 = ['d', 'e', 'f']
list_2.pop('e)

```


## Iterating over lists
list comprehension is the common way to iterate over a list to perform some action.e.g. [action for item in list]
>- Here I want to print each cookie name in title case I've eaten this week. So I use a list comprehension to loop over each cookie in the cookies list, convert it to title case with the dot-title() method and print it

```
titlecase_cookies = [cookie.title() for cookie in cookies]

print(titlecase_cookies)
```
or 

```
baby_names = [name[3] for name in records]

print(sorted(baby_names))

```
----------------------------------------------------------------------

## Sorting lists
sorted() function sorts data in numerical or alphabeticalorder and returns a new list.sorted() function to sort the data in a list from lowest to highest in the case of numbers and alphabetical order.The sorted() function returns a new list and does not affect the list you passed into the function

```
sorted_cookies = sorted(cookies)

print(sorted_cookies)

output : ['Tirggel', 'chocolate chip', 'peanut butter']

```
