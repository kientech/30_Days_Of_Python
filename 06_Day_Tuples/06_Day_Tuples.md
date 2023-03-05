<div align="center">
  <h1> 30_Days_Of_Python: 06_Day_Tuples</h1>
  <a class="header-badge" target="_blank" href="https://www.linkedin.com/in/asabeneh/">
  </a>


<sub>Author:
<a href="https://www.facebook.com/duongtrungkien04062003"> Duong Trung Kien</a><br>
<small>October, 2022</small>
</sub>

</div> 

[<< Day_05](../05_Day_Lists/05_Day_Lists.md) | [Day_07 >>](../07_Day_Sets/07_Day_Sets.md)

![30DaysOfPython](https://camo.githubusercontent.com/59a720eaa51a6bbc45ba76313bf53a4f2c84dde994c947809a49b41f3c828ef2/68747470733a2f2f7374617469632e636f64696e67666f72656e7472657072656e657572732e636f6d2f6d656469612f70726f6a656374732f33302d646179732d707974686f6e2d33382f696d616765732f73686172652f33305f446179735f6f665f507974686f6e5f2d5f53686172652e6a7067)

- [Day_06:](#day-6)
  - [Tuples](#tuples)
    - [Creating a Tuple](#creating-a-tuple)
    - [Tuple length](#tuple-length)
    - [Accessing Tuple Items](#accessing-tuple-items)
    - [Slicing tuples](#slicing-tuples)
    - [Changing Tuples to Lists](#changing-tuples-to-lists)
    - [Checking an Item in a Tuple](#checking-an-item-in-a-tuple)
    - [Joining Tuples](#joining-tuples)
    - [Deleting Tuples](#deleting-tuples)
  - [💻 Exercises: Day_06](#-exercises-day-6)
    - [Exercises: Level_01](#exercises-level-1)
    - [Exercises: Level_02](#exercises-level-2)

# Day_06:

## Tuples

A tuple is a collection of different data types which is ordered and unchangeable (immutable). Tuples are written with round brackets, (). Once a tuple is created, we cannot change its values. We cannot use add, insert, remove methods in a tuple because it is not modifiable (mutable). Unlike list, tuple has few methods. Methods related to tuples:

- tuple(): to create an empty tuple
- count(): to count the number of a specified item in a tuple
- index(): to find the index of a specified item in a tuple
- + operator: to join two or more tuples and to create a new tuple

### Creating a Tuple

- Empty tuple: Creating an empty tuple
  
  ```py
  # syntax
  empty_tuple = ()
  # or using the tuple constructor
  empty_tuple = tuple()
  ```

- Tuple with initial values
  
  ```py
  # syntax
  tuples = ('item1', 'item2','item3')
  ```

  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  ```

### Tuple length

We use the _len()_ method to get the length of a tuple.

```py
# syntax

tuples = ('item1', 'item2', 'item3')
len(tuples)
```

### Accessing Tuple Items

- Positive Indexing
  Similar to the list data type we use positive or negative indexing to access tuple items.

  ```py
  # Syntax
  tuples = ('item1', 'item2', 'item3')
  first_item = tuples[0]
  second_item = tuples[1]
  ```

  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  first_fruit = fruits[0]
  second_fruit = fruits[1]
  last_index =len(fruits) - 1
  last_fruit = fruits[last_index]
  ```

- Negative indexing
  Negative indexing means beginning from the end, -1 refers to the last item, -2 refers to the second last and the negative of the list/tuple length refers to the first item.


  ```py
  # Syntax
  tuples = ('item1', 'item2', 'item3','item4')
  first_item = tuples[-4]
  second_item = tuples[-3]
  ```

  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  first_fruit = fruits[-4]
  second_fruit = fruits[-3]
  last_fruit = fruits[-1]
  ```

### Slicing tuples

We can slice out a sub-tuple by specifying a range of indexes where to start and where to end in the tuple, the return value will be a new tuple with the specified items.

- Range of Positive Indexes

  ```py
  # Syntax
  tuples = ('item1', 'item2', 'item3','item4')
  all_items = tuples[0:4]         # all items
  all_items = tuples[0:]         # all items
  middle_two_items = tuples[1:3]  # does not include item at index 3
  ```

  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  all_fruits = fruits[0:4]    # all items
  all_fruits= fruits[0:]      # all items
  orange_mango = fruits[1:3]  # doesn't include item at index 3
  orange_to_the_rest = fruits[1:]
  ```

- Range of Negative Indexes

  ```py
  # Syntax
  tuples = ('item1', 'item2', 'item3','item4')
  all_items = tuples[-4:]         # all items
  middle_two_items = tuples[-3:-1]  # does not include item at index 3 (-1)
  ```

  ```py
  fruits = ('banana', 'orange', 'mango', 'lemon')
  all_fruits = fruits[-4:]    # all items
  orange_mango = fruits[-3:-1]  # doesn't include item at index 3
  orange_to_the_rest = fruits[-3:]
  ```

### Changing Tuples to Lists

We can change tuples to lists and lists to tuples. Tuple is immutable if we want to modify a tuple we should change it to a list.

```py
# Syntax
tuples = ('item1', 'item2', 'item3','item4')
lists = list(tuples)
```

```py
fruits = ('banana', 'orange', 'mango', 'lemon')
fruits = list(fruits)
fruits[0] = 'apple'
print(fruits)     # ['apple', 'orange', 'mango', 'lemon']
fruits = tuple(fruits)
print(fruits)     # ('apple', 'orange', 'mango', 'lemon')
```

### Checking an Item in a Tuple

We can check if an item exists or not in a tuple using _in_, it returns a boolean.

```py
# Syntax
tuples = ('item1', 'item2', 'item3','item4')
'item2' in tuples # True
```

```py
fruits = ('banana', 'orange', 'mango', 'lemon')
print('orange' in fruits) # True
print('apple' in fruits) # False
fruits[0] = 'apple' # TypeError: 'tuple' object does not support item assignment
```

### Joining Tuples

We can join two or more tuples using + operator

```py
# syntax
tpl1 = ('item1', 'item2', 'item3')
tpl2 = ('item4', 'item5','item6')
tpl3 = tpl1 + tpl2
```

```py
fruits = ('banana', 'orange', 'mango', 'lemon')
vegetables = ('Tomato', 'Potato', 'Cabbage','Onion', 'Carrot')
fruits_and_vegetables = fruits + vegetables
```

### Deleting Tuples

It is not possible to remove a single item in a tuple but it is possible to delete the tuple itself using _del_.

```py
# syntax
tuples = ('item1', 'item2', 'item3')
del tuples

```

```py
fruits = ('banana', 'orange', 'mango', 'lemon')
del fruits
```

🌕 You are so brave, you made it to this far. You have just completed day 6 challenges and you are 6 steps a head in to your way to greatness. Now do some exercises for your brain and for your muscle.

## 💻 Exercises: Day_06

### Exercises: Level_01

1. Create an empty tuple
2. Create a tuple containing names of your sisters and your brothers (imaginary siblings are fine)
3. Join brothers and sisters tuples and assign it to siblings
4. How many siblings do you have?
5. Modify the siblings tuple and add the name of your father and mother and assign it to family_members

### Exercises: Level_02

1. Unpack siblings and parents from family_members
1. Create fruits, vegetables and animal products tuples. Join the three tuples and assign it to a variable called food_stuff_tp.
1. Change the about food_stuff_tp  tuple to a food_stuff_lt list
1. Slice out the middle item or items from the food_stuff_tp tuple or food_stuff_lt list.
1. Slice out the first three items and the last three items from food_staff_lt list
1. Delete the food_staff_tp tuple completely
1. Check if an item exists in  tuple:

- Check if 'Estonia' is a nordic country
- Check if 'Iceland' is a nordic country

  ```py
  nordic_countries = ('Denmark', 'Finland','Iceland', 'Norway', 'Sweden')
  ```

🎉 CONGRATULATIONS ! 🎉 

[<< Day_05](../05_Day_Lists/05_Day_Lists.md) | [Day_07 >>](../07_Day_Sets/07_Day_Sets.md)
