## Python
### Get input and print <mark>formatted</mark>input
```
name = input()
print(f"hello, {name}!")
```

### Printing various types of variables
```
i = 28
print(f"i is {i}")

f=2.8
print(f"f is {f}")

b=True
print(f"b is {b}")

n = None
print(f"n is {n}")
```

### Conditions in python
```
x = 28

if x>0:
    print(f"x i.e {x} is positive")
elif x<0:
    print(f"x i.e. {x} is negative")
else:
    print(f"x i.e. {x} is 0")

```
### Different data types in Python
```
name = "Alice"
coordinates = (10.0, 20.0)
names = ["Alice", "Bob", "Charlie"]
print(f"string - {name}, tupple - coordinates, list - {names}")

```

#### 'Sets' datatype in Python
Sets is a particular value in the set or not.
```
s = set()
s.add(1)
s.add(3)
s.add(5)
s.add(3)
print(s)

```
#### Python dictionary
```
ages = {"Alice":22, "Bob": 27}
ages["Charlie"] = 30
ages["Alice"] +=1

print(ages)
```
### For loop in python
```
for i in range(5):
    print(i)
```

```
names = ["Alice", "Bob", "Charlie"]
for name in names:
    print(name)

```
### How to formulate functions in Python
```
def square(x):
    return x*x;

for i in range(10):
    print(f"{i} squared is {square(i)}")
```

Another way of formatting the print statement using {} placeholders
```
def square(x):
    return x*x;

for i in range(10):
    print("{} squared is {}".format(i, square(i)))
```
## How to import functions from one file to another file
The below code import the function 'square' from the file functions.py
```
from functions import square
print (square(10))

```
The output of the above code is long list of squares including the square of 10. This happens because the apart from the 'square' function in functions.py, the other code of for loop is also running.
The code in functions.py is
```
def square(x):
    return x*x;

for i in range(10):
    print("{} squared is {}".format(i, square(i)))
```
To prevent this other code of functions.py from running, there are two solutions.
1. Keep the functions in separate files.
2. or use a main function in the functions.py, such that the for loop below it runs only when the functions.py is run, not when the 'square' functions is called. Alter the functions.py files as follows:

```
def square(x):
    return x*x;
def main():
    for i in range(10):
        print("{} squared is {}".format(i, square(i)))

if __name__=="__main__":
    main()
```
The addition of the following lines in the above functions.py file, tells the program to run the code only from the current file. So, the code included in main() function will not run, if the square function is called from another file.
```
if __name__=="__main__":
    main()
```

## How to define classes in Python
```
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

p = Point(3,5)
print(p.x)
print(p.y)

```
