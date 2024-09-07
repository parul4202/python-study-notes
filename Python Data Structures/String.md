string
## Strings 
this is the most common type of data type, a string is an immutable array of characters. 
--------------------------------

## Creating formatted strings
f""---> f-string, which is short for formatted string literals

```
name = "sam"
age = "69"

print(f"Are you {name} ? Are you {age} years old?")

```
-------------------------------------------------------
-------------------------------------------------------
## Combining multiple strings
>- using .join()

## Joining with strings

", ".join() uses the string it's called on to join an iterable

```
child_ages = ["3", "4", "7", "8"]
print(", ".join(child_ages))"3, 4, 7, 8"
print(f"The children are ages {','.join(child_ages[0:3])}, and {child_ages[-1]}.")"The children are ages 3, 4, 7, and 8."

```
----------------------------------------------------------
---------------------------------------------------------
## Matching parts of a string

>>- .startswith() and .endswith() methods
 will tell you if a string starts or ends with another character or string

 ```
 boy_names = ["Mohamed", "Youssef", "Ahmed"]
 print([name for name in boy_names if name.startswith('A')])
 ["Ahmed"]

 ```
 -------------------------------------------------------
 -------------------------------------------------------

 ## Searching for things in strings
 The in operator searches for some value in some iterabletype like a string.

```
 "long" in "Life is a long lesson in humility."

 output: True
```

```
 "life" in "Life is a long lesson in humility."

 output: False
 ```


>- life search  is in lower case and in string Life is in capital L"Life". strings are case sensetive.
>>- Be careful as these and most string functions are _case-sensitive_.
-----------------------------------------------------
-----------------------------------------------------
## we can manage this via using lower() method 

```
"life" in "Life is a long lesson in humility.".lower()

output: True

````
------------------------------------------------------