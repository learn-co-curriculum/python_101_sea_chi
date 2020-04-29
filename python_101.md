---
title: LessonPlanTemp
layout: post
weight: 10
hidden: true
---


Lesson Plan Template:
===


**Course**: [DS Immersive]   <br/>
**Mod**:   Mod 1    <br/>
**Topic**: Python 101                  <br/>
**Amount of time**: 1 hour <br/>
**Author**: JMB


***

#### Topic:
This lesson will cover the basics of Python programming. 

    * Python as a caculator
    * Data types
    * Lists/dictionaries/tuples/sets
    * casting
    * If/elif/for loops
    
#### Learn.co material:

#### materials
(python_101_repo)[https://github.com/learn-co-curriculum/python_101_sea_chi]

#### Prerequisite knowledge/ Prework:
Be able to open a Jupyter notebook

#### Learning goals for this lesson:
Greg
    * SWBAT use Python as a caculator
    * SWBAT differentiat between different data types
Max
    Learning Goal 1 [16 min]: Students will be able to understand the difference between and use lists/dictionaries/tuples/lists
    Learning Goal 2 [2 min]: Students will be able to cast objects as other types
    Learning Goal 3 [3 min]: Students will be able to code if/else statements
    Learning Goal 4 [3 min]: SWBAT execute for loops


Part 1: 
Greg will do Python as a calculator and Data Types [20 minutes]

Part 2: Max 

##################################################
**Step**: Learning Goal 1: Students will be able to use lists  <br/>
**Time**: [5] min

We have spoken about the essential single value builtin data types: integers, floats, strings, and booleans.  Now we will look at objects that contain other objects [container_objs](https://docs.python.org/3/c-api/concrete.html#sequence-objects). The first of these containers is the list object.  It is essential, and you will always use them.  How do you define a list? Square brackets. You can define an empty list with an open an close bracket. We then populate the list with other objects: here we have 4 data types in the list.  This makes clear one list can have multiple datatypes.

    * Question to students: Pose question to students about zero indexing of list.

If we have the same values in a list, and we set them equal to eachother using the double equals evuivalency operator, we are returned the value, false. 
    * Question to students: Order matters.  This is an essential difference between lists an dictionaries. 
    
Lists are mutable.  That is, they can be changed.  A few common methods associated with lists are append, remove, and pop.

    * Skill Check
       -    In the cell below, write a line of code that displays the type of the last index of random list

##################################################

**Step**: Learning Goal 1: Students will be able to understand and use dictionaries  <br/>
**Time**: [5] min

Dictioanaries are the second type of object which contains other objects which we will encounter.  They are bit more difficult to use, but are incredibly useful once you are comfortable with them.  

Dictionaries are unordered, and are accessed using key/value pairs.  
We define dictionaries using curly braces, and each key/value is associated to one another with a colon, and separated by a comma.

We can access the keys using the keys() method and the values with the values() method.

The items method returns both keys and values together.
We can access values in a keys object using list.
We can reset the values of a dictioanry using the key.

##################################################

**Step**: Learning Goal 1: Students will be able to understand and use tuples and sets <br/>
**Time**: [2] min

Tuples are similar to lists, but they are immutable.
We define them with open and closed parens.
Tuples are hashable [https://docs.python.org/3/glossary.html#term-hashable]. An object is hashable if its value does not change over time.

Sets are like lists, but all the values are unique. They are defined with curly braces
We see instantiating a set with duplicate values shrinks down the set to the unique values.

##################################################

**Step**: Learning Goal 2: Students will be able to cast objects as different types <br/>
**Time**: [2] min

Casting is changing the type of an object from one type to another.  This will be very useful in your data cleaning, as your data will be imported in a way that you can't always control.

If your code is breaking, it's a good idea to check the type of the data.

One common transformation is taking a string and turning it into a float or an integer.

##################################################

**Step**: Learning Goal 3: Students will be able to code if, statements<br/>
**Time**: [3] min

if statements have a condition, which, if it is met, runs the indented code after the colon.

In this if statement, if the number is divisible by 4, we enter into the code block, and print yes.  
If we change the number to something not divisible by 4, we don't enter into the block.

We can have multiple blocks within an if else statement.  The interpreter checks each criteria in order, and if the criteria is met, then we enter into the block.  Once the criteria is met, we exit out of the if statement, and none of the remaining criteria are checked.

##################################################
**Step**: Learning Goal 4: Students will be able to code for loops<br/>
**Time**: [3] min

For loops enter iterate through a set of values, and do something to each set of those values.


##################################################

Integration:

Exercises:

Put pairs in breakout rooms for 5 minutes and have them work through the exercises at the bottom of the notebook.
