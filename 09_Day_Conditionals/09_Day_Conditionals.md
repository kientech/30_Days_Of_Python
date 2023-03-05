<div align="center">
  <h1> 30_Days_Of_Python: 09_Day_Conditionals</h1>
  <a class="header-badge" target="_blank" href="https://duongtrungkien.netlify.app/">
  </a>


<sub>Author:
<a href="https://www.facebook.com/duongtrungkien062003"> Duong Trung Kien</a><br>
<small>October, 2022</small>
</sub>

</div>

[<< Day_08](../08_Day_Dictionaries/08_Day_Dictionaries.md) | [Day_10 >>](../10_Day_Loops/10_Day_Loops.md)

![30DaysOfPython](https://camo.githubusercontent.com/59a720eaa51a6bbc45ba76313bf53a4f2c84dde994c947809a49b41f3c828ef2/68747470733a2f2f7374617469632e636f64696e67666f72656e7472657072656e657572732e636f6d2f6d656469612f70726f6a656374732f33302d646179732d707974686f6e2d33382f696d616765732f73686172652f33305f446179735f6f665f507974686f6e5f2d5f53686172652e6a7067)

- [📘 Day_09](#-day-9)
  - [Conditionals](#conditionals)
    - [If Condition](#if-condition)
    - [If Else](#if-else)
    - [If Elif Else](#if-elif-else)
    - [Short Hand](#short-hand)
    - [Nested Conditions](#nested-conditions)
    - [If Condition and Logical Operators](#if-condition-and-logical-operators)
    - [If and Or Logical Operators](#if-and-or-logical-operators)
  - [💻 Exercises: Day_09](#-exercises-day-9)
    - [Exercises: Level_01](#exercises-level-1)

# 📘 Day_09

## Conditionals

By default, statements in Python script are executed sequentially from top to bottom. If the processing logic require so, the sequential flow of execution can be altered in two way:

- Conditional execution: a block of one or more statements will be executed if a certain expression is true
- Repetitive execution: a block of one or more statements will be repetitively executed as long as a certain expression is true. In this section, we will cover _if_, _else_, _elif_ statements. The comparison and logical operators we learned in previous sections will be useful here.

### If Condition

In python and other programming languages the key word _if_ is used to check if a condition is true and to execute the block code. Remember the indentation after the colon.

```py
# syntax
if condition:
    this part of code runs for truthy conditions
```

**Example: 1**

```py
a = 3
if a > 0:
    print('A is a positive number')
# A is a positive number
```

As you can see in the example above, 3 is greater than 0. The condition was true and the block code was executed. However, if the condition is false, we do not see the result. In order to see the result of the falsy condition, we should have another block, which is going to be _else_.

### If Else

If condition is true the first block will be executed, if not the else condition will run.

```py
# syntax
if condition:
    this part of code runs for truthy conditions
else:
     this part of code runs for false conditions
```

**Example: **

```py
a = 3
if a < 0:
    print('A is a negative number')
else:
    print('A is a positive number')
```

The condition above proves false, therefore the else block was executed. How about if our condition is more than two? We could use _ elif_.

### If Elif Else

In our daily life, we make decisions on daily basis. We make decisions not by checking one or two conditions but multiple conditions. As similar to life, programming is also full of conditions. We use _elif_ when we have multiple conditions.

```py
# syntax
if condition:
    code
elif condition:
    code
else:
    code

```

**Example: **

```py
a = 0
if a > 0:
    print('A is a positive number')
elif a < 0:
    print('A is a negative number')
else:
    print('A is zero')
```

### Short Hand

```py
# syntax
code if condition else code
```

**Example: **

```py
a = 3
print('A is positive') if a > 0 else print('A is negative') # first condition met, 'A is positive' will be printed
```

### Nested Conditions

Conditions can be nested

```py
# syntax
if condition:
    code
    if condition:
    code
```

**Example: **

```py
a = 0
if a > 0:
    if a % 2 == 0:
        print('A is a positive and even integer')
    else:
        print('A is a positive number')
elif a == 0:
    print('A is zero')
else:
    print('A is a negative number')

```

We can avoid writing nested condition by using logical operator _and_.

### If Condition and Logical Operators

```py
# syntax
if condition and condition:
    code
```

**Example: **

```py
a = 0
if a > 0 and a % 2 == 0:
        print('A is an even and positive integer')
elif a > 0 and a % 2 !=  0:
     print('A is a positive integer')
elif a == 0:
    print('A is zero')
else:
    print('A is negative')
```

### If and Or Logical Operators

```py
# syntax
if condition or condition:
    code
```

**Example: **

```py
user = 'James'
access_level = 3
if user == 'admin' or access_level >= 4:
        print('Access granted!')
else:
    print('Access denied!')
```

🌕 You are doing great.Never give up because great things take time. You have just completed day 9 challenges and you are 9 steps a head in to your way to greatness. Now do some exercises for your brain and muscles.

## 💻 Exercises: Day_09

### Exercises: Level_01

1.  Get user input using input(“Enter your age: ”). If user is 18 or older, give feedback: You are old enough to drive. If below 18 give feedback to wait for the missing amount of years. Output:
    ```sh
    Enter your age: 30
    You are old enough to learn to drive.
    Output:
    Enter your age: 15
    You need 3 more years to learn to drive.
    ```
2.  Compare the values of my_age and your_age using if … else. Who is older (me or you)? Use input(“Enter your age: ”) to get the age as input. You can use a nested condition to print 'year' for 1 year difference in age, 'years' for bigger differences, and a custom text if my_age = your_age. Output:
    ```sh
    Enter your age: 30
    You are 5 years older than me.
    ```
3.  Get two numbers from the user using input prompt. If a is greater than b return a is greater than b, if a is less b return a is smaller than b, else a is equal to b. Output:

```sh
Enter number one: 4
Enter number two: 3
4 is greater than 3
```

### Exercises: Level_02

   1. Write a code which gives grade to students according to theirs scores:
   
        ```sh
        80-100, A
        70-89, B
        60-69, C
        50-59, D
        0-49, F
        ```
1. Check if the season is Autumn, Winter, Spring or Summer. If the user input is:
    September, October or November, the season is Autumn.
    December, January or February, the season is Winter.
    March, April or May, the season is Spring
    June, July or August, the season is Summer
2.  The following list contains some fruits:
    ```sh
    fruits = ['banana', 'orange', 'mango', 'lemon']
    ```
    If a fruit doesn't exist in the list add the fruit to the list and print the modified list. If the fruit exists print('That fruit already exist in the list') 

    ### Exercises: Level 3

   1. Here we have a person dictionary. Feel free to modify it!
   
```py
        person={
    'first_name': 'Duong',
    'middlename': 'Trung',
    'last_name': 'Kien',
    'age': 19,
    'country': 'Quang Ngai',
    'is_marred': False,
    'skills': ['JavaScript', 'React', 'Node', 'MongoDB', 'Python'],
    'address': {
        'street': 'No.5 Street',
        'zipcode': '00000'
    }
    }
```

🎉 CONGRATULATIONS ! 🎉

[<< Day_08](../08_Day_Dictionaries/08_Day_Dictionaries.md) | [Day_10 >>](../10_Day_Loops/10_Day_Loops.md)
