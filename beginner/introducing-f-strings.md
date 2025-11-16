# An Introduction to f-Strings: Modern Interpolation and Formatting in Python

> [!TIP]
> *Before beginning this tutorial, you should already be familiar with Python:*
> - *[**strings**](https://realpython.com/python-data-types/#regular-string-literals)*
> - *[**integers**](https://realpython.com/python-data-types/#integer-numbers)*
> - *[**variables**](https://realpython.com/python-variables/)*
> - *and how to use the [**`print()`**](https://realpython.com/python-print/) function.*

## Table of Contents
- [Introduction](#introduction)
- [Prior to f-Strings](#prior-to-f-strings)
  - [The Modulo Operator (%)](#the-modulo-operator-)
  - [The `str.format()` Method](#the-strformat-method)
- [String Interpolation With f-Strings](#string-interpolation-with-f-strings)
  - [What are f-Strings?](#what-are-f-strings)
  - [Embedding Expressions With f-Strings](#embedding-expressions-with-f-strings)
  - [Formatting With f-Strings](#formatting-with-f-strings)
- [Conclusion](#conclusion)

## Introduction
By the end of this tutorial, you'll understand how to use f-strings in Python to format text and interpolate variables.

Formatting strings and [string interpolation](https://en.wikipedia.org/wiki/String_interpolation) lets you combine text with variables and expressions.
This is useful whenever you want your programs to communicate useful information to the user.
While there are many different ways to format strings in Python, the f-string, also known as formatted strings, was first introduced in Python 3.6 with [PEP-498](https://peps.python.org/pep-0498/), which makes this clearer and easier than older methods.

## Prior to f-Strings

### The Modulo Operator `%`
Similar to the `printf()` function used in the [C language](https://en.wikipedia.org/wiki/C_(programming_language)), Python strings have a built-in operator that allows them to be formatted using the Modulo Operator `%` followed by a character representing the data type.

```Python
name = "Jane"
age = 28

print("Hello, %s. You are %d years old." % (name, age))
# 'Hello, Jane. You are 28 years old.'
```

Here, `%s` and `%d` act as placeholders for strings and integers.
While this method works, the syntax can be confusing, and requires you to know what the data type returned will be.

### The `str.format()` Method

Another approach is the built-in `.format()` method in Python strings.

```Python
name = "Jane"
age = 28

print("Hello, {0}. You are {1} years old.".format(name, age))
# 'Hello, Jane. You are 28 years old.'
```

This method replaces the values in `{}` with variable values in order.
Although `.format()` improved readability slightly, it's important to note that you must match the paceholders and variables by the correct position and name.

Using the same example as above but swapping `{0}` and `{1}`, or `name` and `age` arround would return the incorrect value.

## String Interpolation With f-Strings

### What are f-Strings
An f-string is a modified Python string, where it is prefixed with an `f` before the quotation marks. 
This allows you to directly insert variables or expressions inside curly braces `{}`.

Lets look at f-strings in action, using the same example as before:

```Python
name = "Jane"
age = 28

print(f"Hello, {name}. You are {age} years old.")
# 'Hello, Jane. You are 28 years old.'
```

As you can see, by prefixing the string with an `f`, you can embed variables right where they are needed.
This small improvement, dramatically improves the codes readability while requiring less work than other methods.

### Embedding Expressions With f-Strings
You're not just limited to using variables in f-strings, any expression works inside curly braces.

```Python
apples = 3
oranges = 5

print(f"You have a total of {apples + oranges} pieces of fruit.")
# 'You have a total of 8 pieces of fruit.'
```

Here you can see that f-strings can also be used to embed evaluated expressions in Python strings.
This is super handy for calculating and formatting expressions on the fly.

### Formatting With f-Strings
f-Strings also allow you to control how variables and expressions are displayed using format codes.
This is useful for numbers with many decimals, or aligning output text.

A practical use-case for this is expressing currency in its correct format.

```Python
price_per_apple = 0.2

print(f"The price of apples are ${price_per_apple:.2f} each.")
# 'The price of apples are $0.20 each.'
```

Here, `:.2f` tells Python to show two digits after the decimal.
You can add a colon and a format specifier in your curly braces to style numbers, dates, and more.

## Conclusion
f-Strings provide an efficient and readable way to format strings in Python.
Compared to older approaches like the modulo operator `%` or `.format()` method, f-strings make it much easier for you to embed variables and expressions inline and to control how your data appears.

Throughout this tutorial, you learned not only how to use f-strings, by prefixing your string with an `f` and placing expressions inside curly braces, but also why they're the reccomended choice for modern Python code.
With f-strings, your programs become easier to write and maintain, letting you focus more on what your code should do, rather than on tricky formatting details.

You're now equipped to format strings effectively in Python, and to recognize when and why to use f-strings in your own projects.
