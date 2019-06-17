##### Introduction to comparison operators
Assume you are adding 2 numbers. The numbers are the operands and the `+` symbol is the operator.

Comparison operators in python are used to compare the values of its operands and return a **boolean** result. Not just numbers, you can also compare **strings**. Confused? The secret lies in **ASCII** values.

ASCII is a character encoding standard and stands for **American Standard Code for Information Interchange**. It is basically used for converting binary computer text to human readable text and is used in all electronics devices. You can find a list of all ASCII codes [here](https://theasciicode.com.ar/). 

Here are the various types of comparison operators in python.

![comparison-operators](/img/comparison-operators/comparison-table-2.png)

Let's check out the usage of all these operators through some examples.

##### Greater than operator (>)

This operator is used to check if the value on the left is greater than the value on the right.

```python3
print(3 > 2)

print(-5 > 4)

print(-290023 > 1)
``` 
In all the above examples, it is going to check if the comparison holds. The above snippet will return the following result.
```bash
True
False
False
```

Makes sense, right?

Like mentioned earlier, we can also compare strings. 
```python3
print('Savan' > 'savan')
``` 
The above snippet will return us **False**. Its because the ASCII value of `s` is 115 and ASCII value of `S` is 83. When you compare strings, the ASCII values of the first characters are first compared. If the ASCII values are different, a boolean result is returned based on the comparison. If the ASCII values are same, the next characters are compared and so on.

So what happens when you run the following code?
```python3
print('savan' > 'savaN')
``` 
The starting 4 characters of both the strings are same. Only the last character is different. In this case, python will compare the ASCII values of all the characters until the last. Since the ASCII value of `n`(110) is greater than the ASCII value of `N`(78), Python will return us **True**. The image below shows the pictorial representation of the process.

![comparison-operators-example](/img/comparison-operators/savan-comparison.png)

##### Less than operator (<)
This operator is used to check if the value on the left is less than the value on the right.

```python3
print(3 < 2) # Returns False

print(-5 < 4) # Returns True

print(-290023 < 1) # Returns True
``` 
It works similarly with strings.
```python3
print('Savan' < 'savan')
``` 
The above snippet will return us **True**. Its because the ASCII value of `S` is 83 and ASCII value of `s` is 115. So the rest of the letters are not compared anymore and Python returns us True.

##### Equality operator (==)

Equality operator is used to check the equality of the values of its operands. 
Not to be confused with the equal to (`=`) operator.

The `=` operator is used to assign a value to a variable. When you say `x = 5`, you are assigning the value **5** to variable **x**. The `==` operator just checks if the values of both left and right operands are equal or not and returns a boolean. 

Consider the following statements.

```python3
x = 5
print(x == 5) # Returns True
print(x == 4) # Returns False

# Equality with strings

print('Savan' == 'Savan') # Returns True
print('Savan' == 'savan') # Returns False
```
For numerical comparison, it is pretty straight forward. For strings, it is the ASCII value again that determines the result of the comparison.

##### Not equal to (!=)

This is the opposite of the equality operator. It checks if the values of its operands are unequal. Lets consider the above example.
```python3
x = 5
print(x != 5) # Returns False
print(x != 4) # Returns True

# Equality with strings

print('Savan' != 'Savan') # Returns False
print('Savan' != 'savan') # Returns True
```
So if the values of both its operands are equal, the `!=` operator will return **False**.

##### Greater than equal to (>=)
This operator combines the greater than operator `(>)` with the equality operator `(==)`. It checks if the left side operand is **greater than or equal to** the right side operand.

```python3
x = 5
print(x >= 5) # Returns True
print(x >= 6) # Returns False

# Comparison of strings

print('Savan' >= 'Savan') # Returns True
print('Savan' >= 'savan') # Returns False
```

Since the ASCII value of `S` (83) is less than the ASCII value of `s` (115), the comparison will return us False.

##### Less than equal to (<=)

This operator is the opposite of **>=** operator. This operator combines the less than operator `(<)` with the equality operator (==). It checks if the left side operand is less than or equal to the right side operand.

```python3
x = 5
print(x <= 5) # Returns True
print(x <= 4) # Returns False

# Comparison of strings

print('Savan' <= 'Savan') # Returns True
print('Savan' <= 'savan') # Returns True
```
Since the ASCII value of `S` (83) is less than the ASCII value of `s` (115), the comparison will return us True.

If you have any questions, concerns or criticisms - do put them down in the comments section.
