
# Python Fundamentals

## Objectives

After this lesson, students will be able to:

- distinguish and use objects of different datatypes;
- use 'if' and 'else' statements;
- slice into strings, lists, and tuples;
- construct a for-loop.

Python can perform arithmetic calculations:


```python
2 + 2 * 10
```


```python
523678 * 1097253
```


```python
375 % 5
```

But it can do so much more than this!

## Data Types

Objects in Python come in different types.

The types to be aware of are strings (```str```), integers (```int```), floats (```float```), Booleans (```bool```), lists (```list```), and dictionaries (```dict```).

### Strings

Strings are pieces of text. In order for the computer to understand a string as such, it must be placed in single or double quotes:


```python
'This is a string'
```


```python
This is not a string
```


```python
fav_string = 'Here\'s my favorite string'
fav_string
```

Triple quotes are useful for creating code blocks (that can themselves contain single or double quotes).


```python
print("""
Hey y'all. Where's the "party"?
""")
```

Often we want to use and store values in variables.
To declare a variable, simply write the name of the variable, followed by an '=', followed by the value you want to store in the variable.


```python
favorite_string = 'python'
```


```python
favorite_string
```


```python
type(favorite_string)
```

If you make a mistake ...


```python
name = 'gref'
```

just re-assign it:


```python
name = 'greg'
```

Strings can be sliced, if you want to make use of only part of a given string:


```python
name[2]
```


```python
name[2:3]
```


```python
name[::-5] == name[::-100]
```

Python strings are immutable, which means that you can't reassign any part of one:


```python
name[3] = 'f'
```


```python
name.replace('eg', 'ef')
```

For more on what you can do with strings, just type ```help(str)```!


```python
help(str)
```

### Integers and Floats

Integers and floats are numeric types in Python. Floats have decimal points and integers do not.


```python
type(0)
```


```python
type(0.)
```


```python
type(0.789)
```

Python DOES allow arithmetic across these two types:


```python
10 + 15.35
```


```python
10 % 6 / 6
```

Python ```int```s are _coerced_ into ```float```s for these calculations.

The keyword 'range' can be used to specify an interval of integers.


```python
bob = range(8)
```


```python
bob
```


```python
list(bob)
```


```python
len(bob)
```


```python
list(range(2, 10, 2))
```

### Booleans

There are only two values of a Boolean: True and False.


```python
type(False)
```


```python
type('false')
```


```python
type(false)
```

Booleans are useful when you want to check to see whether some condition has been satisfied.

### Lists

A list is an ordered collection of objects. Use square brackets for lists.


```python
empty_list = []
```


```python
numeric_list = [1,2,3,4]
```

One list can have multiple data types


```python
random_list = [1, 'alan', 8.5, True]
```

Lists can be sliced, just like strings:


```python
random_list[1:]
```




    ['alan', 8.5, True]



### Question
What does the output of the above cell tell you about how lists are indexed?



```python
random_list_2 = ['alan', 8.5, True, 1]
```


```python
random_list == random_list_2
```




    False



### Question
What does the output of the above cell suggest about what Python considers in order to deterimine if a list is unique?

Lists are mutable:


```python
random_list[2] = '85'
random_list
```




    [1, 'alan', '85', True]




```python
random_list.append('85')
random_list
```




    [1, 'alan', '85', True, '85']




```python
random_list.remove('alan')
```


```python
random_list
```




    [1, '85', True, '85']




```python
random_list.pop()
```




    '85'




```python
random_list
```




    [1, '85', True]




```python
We can also add two lists together with the plus operatore
```


```python
random_list + random_list_2
```




    [1, '85', True, 'alan', 8.5, True, 1]



### Skill Check
In the cell below, write a line of code that displays the type of the last index of random_list




```python
# Your code here
```

### Dictionaries

A dictionary is an unordered collection of _paired_ elements, just like an English dictionary is a pairing of words and definitions.

The first elements of the pairs are called "keys"; the second elements are called "values".

Use braces for dictionaries.


```python
max_ = {'name': 'Max', 'occupation': 'data_scientist',
            'HP': 140, 'favorite_color': 'blue', 'weakness':'caffeine dependency'}
```


```python
type(max_)
```




    dict




```python
max_.keys()
```




    dict_keys(['name', 'occupation', 'HP', 'favorite_color', 'weakness'])




```python
max_.values()
```




    dict_values(['Max', 'tick_tock_professional', 140, 'blue', 'caffeine dependency'])




```python
max_.items()
```




    dict_items([('name', 'Max'), ('occupation', 'tick_tock_professional'), ('HP', 140), ('favorite_color', 'blue'), ('weakness', 'caffeine dependency')])



If we would like to access a value of dict values, we can turn it into a list using the built-in operator and then use list indexing:



```python
list(max_.values())[0]
```




    'Max'



To access a "definition", just look up the word!


```python
max_['occupation'] = 'tick_tock_professional'
```


```python
max_['occupation']
```




    'tick_tock_professional'



Dictionaries share some methods with lists:


```python
max_occupation = max_.pop('occupation')
```




    'tick_tock_professional'




```python
max_
```




    {'name': 'Max',
     'HP': 140,
     'favorite_color': 'blue',
     'weakness': 'caffeine dependency'}




```python
greg = {}
```


```python
type(greg)
```




    dict



## Knowledge Check
Given the two dictionaries below, what do you expect the out put of dict_1==dict_2 to be?


```python
dict_1 = {'bi': 2, 'hi':1}
dict_2 = {'hi':1, 'bi':2}
dict_1==dict_2
```

### Tuples and Sets

Tuples are similar to lists, but they are immutable.
We define them with open an closed parens


```python
type((1, 2, 4))
```




    tuple



Tuples are [hashable](https://docs.python.org/3/glossary.html#term-hashable)


```python
hash((1, 2, 3))
```




    2528502973977326415




```python
hash(random_list)
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-85-d76751d0c8cc> in <module>
    ----> 1 hash(random_list)
    

    TypeError: unhashable type: 'list'


Sets are like lists, but all the values are unique. They are defined with curly braces


```python
type({1, 2, 3})
```




    set




```python
# We see instantiating a set with duplicate values shrinks down the set to the unique values.
{1,1,2,3}
```




    {1, 2, 3}



### Casting

Sometimes we want to turn an object of one data type into another, and we have to tell Python to do it:


```python
float('8.9')
```




    8.9




```python
str(8)
```




    '8'




```python
int(8.9)
```




    8




```python
bool(0)
```




    False




```python
bool(2)
```




    True




```python
2 == True
```




    False




```python
1 == True
```




    True




```python
0 == False
```




    True




```python
type(0)
```




    int




```python
type(False)
```




    bool



## 'If' - Statements

'if'-statements are very powerful tools in Python. Simply put, they check to see if some condition is true or not.

Useful comparison operators:

'>', '<=', '=='


```python
num = 76
if num % 4 == 0:
    print('yes')
```

    yes


### 'Else' - and 'Elif' - Statements

The keyword 'else' is used to cover the other cases where the 'if'-statement is false.

Sometimes we want to consider more than just two possibilities, and we can use 'elif' ("else-if") for this.


```python
num = 74
if num % 4 == 0:
    print('yes')
else:
    print('no')
```


```python
num = 134567
if num % 3 == 0:
    print('multiple of 3')
elif num % 3 == 1:
    print('one more than a multiple of 3')
else:
    print('two more than a multiple of 3')
```

    two more than a multiple of 3


## 'For' - Loops

A 'for'-loop is way of performing a set of related tasks automatically. Suppose, for example, that I want to print out every number between 1 and 7, inclusive.


```python
for val in range(1, 8):
    print(val)
```

The combination of 'for'-loops with 'if'-statements is especially powerful.


```python
for val in range(1, 8):
    if val >= 4:
        print(val)
```


```python
# This is a comment.
```


```python
for elem in max_:
    if type(elem) == str:
        print(elem)
```

    name
    HP
    favorite_color
    weakness


# Skill check:
How would I print out all the values of the max_ dictionary:


```python
# your code here
```

A common application of a for loop is instantiating a list outside of the for loop, and appending values to that list


```python
even_numbers = []

for _ in range(1,9):
    if _ % 2 == 0:
        even_numbers.append(_)

even_numbers
```




    [2, 4, 6, 8]



## Exercises:

1. Build a list of the integers from 1 to 20. And then, for each number in your list, print it out if it's even; otherwise print out its double.

Note that we could just use an iterator object without building the whole list!


```python

```

2. Here is a dictionary of the classmembers' names:


```python
cohort = {'timothy': 5, 'daihong': 4, 'hamza': 6, 'jarod': 5, 'kyle': 9,
         'luis': 4, 'mihir': 5, 'sam': 3, 'calvin': 10}
```

Print out each key whose value is not equal to the length of the key.


```python
# Your answer here
```

3. Either I'm going to lunch or to the park. If I go to lunch I'll definitely take my wallet, but if I go to the park then I'll only take my wallet if I want to stop by the store. <br/> Use conditionals to construct a piece of code that will return the appropriate (Boolean) value of take_wallet under the right conditions. Test your code!


```python
# Sample conditions

lunch = True
park = True
store = False

```


```python
# Test your code!

take_wallet
```




    True




```python

```
