# FIT1045 Week 3 PASS Session 
Video link: 

## Recap Week 1 - 3
- **Data Types**
    - String: "Hello", "Uhhh"
    - Integer: 0, 1, 2, 3333, 11111
    - Float: 0.1, 3123.2, 21.22
    - Boolean: True, False

- **Data Structures**
    - List []
    - Dictionary {}
    - Tuple ()

- **Operators and Operands**
    - x + y
        - 3 + 5 = 8
        - 3.0 + 5 = 8.0
        - "H" + "E" = "HE"
        - "H" + 3 = Error! --> "H" + str(3) = "H3"
    - x - y
        - 6 - 2 = 4
        - 9.0 - 2.0 = 7.0
    - x * y
        - x multiply by y
        - We can do more! "H" * 5 = "HHHHH"
    - x / y : x divided by y (always float)
    - x // y : floor division 
    - x ** y : x to the power of y 
    - Add bracket for precedence (x + y) // 2
- **Variables**
```Python
x = 3
y = 4
print(x + y) # 7

x = "How"
y = "are you"
print(x + y) # Howare you
print(x, y) # How are you

name = "CH"
uni = "Monash"
print(f"Hi my name is {name} and I am from {uni}")
```
- **Functions**
```Python
def profile(name, age, school):
    print(f"Name: {name}\nAge: {age}\nSchool: {school}\n")

profile("CH", 18, "Monash")
profile("BB", 21, "MIT")
```

- **Type Conversion**
    - We can check the type using ```type()``` function
        - ```print(type("HI"))``` # string
    - ```float(), int(), str()```

- **List**
```Python
lst = [["a"], 1, 2, True]
print(1 in lst) # True
print("a" in lst) # False
print(lst[0]) # ["a"]
print(lst[-1]) # True
print(lst.index(2)) # 2
lst.append(3) # lst = [["a"], 1, 2, True, 3]
```

- **Conditionals**
```Python
x = 3, y = 2
if x > y:
    print("x greater than y")
else:
    print("y greater or equal to x")

if x > y and x < 10:
    print("x greater than y and x is less than 10")
elif x > y or x < 10:
    print("x is greater than y or x is less than 10")
```

- **While Loops**

Avoid infinite loops, make sure you include ```break``` or 
anything updating that can terminate the loop

```Python
while True:
    print("Hi")
    break

x = 1
while x <= 10:
    print(x)
    x += 1

flag = True
# Don't write while flag == True! It is ugly!
while flag:
    name = input("What is your name")
    if name == "CH":
        flag = False
    print("Hmm")
```

- **For Loops**
```Python
for i in range(5):
    print(i) # 0 1 2 3 4

for i in range(1, 6):
    print(i) # 1 2 3 4 5

for i in range(5, 0, -1):
    print(i) # 5 4 3 2 1

lst = ["a", 1, 2, 3]
for item in lst:
    print(item) # "a" 1 2 3

for ch in "Hello":
    print(ch) # H e l l o

lst = [1, 2, 3, 4, 5]
total = 0
for num in lst:
    total += num # 15

lst = ["A", "B", "C"]
for i, word in enumerate(lst): 
    print(f"Position {i} is {word}") # ..0..A ..1..B ..2..C
```

- **Split and Join**
```Python
sentence = "Never gonna give you up"
split_sentence = sentence.split(" ")
print(split_sentence) # ['Never', 'gonna', 'give', 'you', 'up']
join_sentence = ",".join(split_sentence)
print(join_sentence) # Never,gonna,give,you,up
```

## W1 Post-Class
```Python
```

## W2 Post-Class
```Python
```

## W3 Post-Class
```Python
```

## Debug (Print)
- What is always changing?
- Index, current result, is the variable updating correctly?
- Print out the value before and after updating, same as expected?
- Reference problem? 
```Python
# Omg! There are bugs!
lst = [[]] * 3
for i in range(len(lst)):
    lst[i].append(i)
print(lst) # [[0, 1, 2], [0, 1, 2], [0, 1, 2]] Why?

# Find the bugs
lst = [[]] * 3
for i in range(len(lst)):
    print(i) # Correct 
    print(lst[i]) # Wrong, should be []
    lst[i].append(i)
print(lst) # [[0, 1, 2], [0, 1, 2], [0, 1, 2]] Why?

# Fix the bugs
lst = []
for i in range(3):
    lst.append([])
for i in range(len(lst)):
    lst[i].append(i)
print(lst) # [[0], [1], [2]] Yay!
```

## Debug (Breakpoints)
- I will demonstrate this in the video 


## Extra Practices
1. Given an integer n, output the corresponding graph pattern.

Example
For n = 5, the expected output is:
```
     *
    ***
   *****
    ***
     *
```

2. LeetCode 1: Two Sum (https://leetcode.com/problems/two-sum/description/)

We will discuss these two questions in the next session
