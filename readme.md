# https://medium.com/@jhankar.mahbub/learn-and-master-python-in-a-month-b1acc94d5f32

## Day -2: for loop

- break
```
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    break
  print(x) 
```
- output
```
apple
```
- continue
```
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    continue
  print(x) 

# W3schools
```
-output
```
apple
cherry
```
- check out the while loop's continue and break from the link https://www.w3schools.com/python/python_while_loops.asp

# Day -2:function

- Arbitrary Arguments, *args .If you do not know how many arguments that will be passed into your function, add a * before the parameter name in the function definition. This way the function will receive a tuple of arguments, and can access the items accordingly:

```
def my_function(*kids):
  print("The youngest child is " + kids[2])

my_function("Emil", "Tobias", "Linus")
```
- output
```
The youngest child is Linus
```
- Keyword Arguments.You can also send arguments with the key = value syntax.
This way the order of the arguments does not matter.
```
def my_function(child3, child2, child1):
  print("The youngest child is " + child3)

my_function(child1 = "Emil", child2 = "Tobias", child3 = "Linus")
```
- Arbitrary Keyword Arguments, **kwargs.If you do not know how many keyword arguments that will be passed into your function, add two asterisk: ** before the parameter name in the function definition.This way the function will receive a dictionary of arguments, and can access the items accordingly:
```
def my_function(**kid):
  print("His last name is " + kid["lname"])

my_function(fname = "Tobias", lname = "Refsnes")
```
- Default Parameter Value.The following example shows how to use a default parameter value.If we call the function without argument, it uses the default value:
```
def my_function(country = "Norway"):
  print("I am from " + country)

my_function("Sweden")
my_function("India")
my_function()
my_function("Brazil")
```
- Passing a List as an Argument.You can send any data types of argument to a function (string, number, list, dictionary etc.), and it will be treated as the same data type inside the function.E.g. if you send a List as an argument, it will still be a List when it reaches the function:
```
def my_function(food):
  for x in food:
    print(x)

fruits = ["apple", "banana", "cherry"]

my_function(fruits)
```
## Recursion
- Python also accepts function recursion, which means a defined function can call itself.
- Recursion is a common mathematical and programming concept. It means that a function calls itself. This has the benefit of meaning that you can loop through data to reach a result.
- The developer should be very careful with recursion as it can be quite easy to slip into writing a function which never terminates, or one that uses excess amounts of memory or processor power. However, when written correctly recursion can be a very efficient and mathematically-elegant approach to programming.
- In this example, tri_recursion() is a function that we have defined to call itself ("recurse"). We use the k variable as the data, which decrements (-1) every time we recurse. The recursion ends when the condition is not greater than 0 (i.e. when it is 0).

### factorial example
- by loop
```
def factorial(x):
    a=1
    list=[]
    for i in range(2,x+1):
        a=a*i
        list.append(a)
    if x==0 or x==1:
        print(x)
    else:
        print(list[x-2])
```
- by recursion
```
def factorial(x):
    """This is a recursive function
    to find the factorial of an integer"""

    if x == 1:
        return 1
    else:
        return (x * factorial(x-1))


num = 5
print("The factorial of", num, "is", factorial(num))
```
- problem with the recursion is that factorial(0), so basically, it has not even been used properly by a w3schools where even the best programmer might check if they are stuck somewhere at the basic

- the true recursion is as below,
```
def arithmeticprogression(x):
    """This is a recursive function
    to find the factorial of an integer"""

    if x == 1 or x==0:
        return x
    else:
        return (x + arithmeticprogression(x-1))
```
- output

![output](https://github.com/anindameister/pythonBasics/blob/main/snaps/1.PNG)

- the w3school's recursion have been fixed below
```
def factorial(x):
    """This is a recursive function
    to find the factorial of an integer"""

    if x == 1 or x==0:
        return x
    else:
        return (x * factorial(x-1))


print(factorial(0))
print(factorial(1))
print(factorial(2))
print(factorial(5))
```
- output
```
0
1
2
120
```
## lambda function

- the link shows lambda functions, dont see much use of it, genuinely
https://www.w3schools.com/python/python_lambda.asp

## modules

- django understanding became a little difficult for me because the basic modules concept was not probaby there for me.

```
def greeting(name):
  print("Hello, " + name)

person1 = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}

person2 = {
  "name": "Aninda",
  "age": 32,
  "country": "India"
}
```
- and
```
from mymodule import person1,person2

print (person1["age"])
print (person2["name"])
```
- the modules to the basic level has been well written in https://www.w3schools.com/python/python_modules.asp
