<!-- 
Document Analysis
--- [https://wordcounter.net/]
  - Word-Count: 634 
  - Char-Count: 3,766
  - Time-to-Read: 2 min 19 sec
-->

# An Introduction to f-Strings: Modern Interpolation and Formatting in Python
By the end of this tutorial, you'll understand how to use f-strings in Python to format text and interpolate variables.

Formatting strings and [string interpolation](https://en.wikipedia.org/wiki/String_interpolation) let you combine text with variables and expressions, which is perfect for communicating useful information in your programs.
While there are many ways to format strings, the integration of [PEP-498](https://peps.python.org/pep-0498/) in Python 3.6 introduced formatted strings, more commonly known as f-strings, making it clearer and easier than any prior method.

## Before f-Strings

- ### The Modulo Operator `%`
  Python strings have a built-in format operator, the Modulo Operator `%`, followed by a character that specifies the data type.

  ```Python
  name = "Jane"
  age = 28
  
  print("Hello, %s. You are %d years old." % (name, age))
  # 'Hello, Jane. You are 28 years old.'
  ```

  Here, `%s` and `%d` act as placeholders for a string and an integer.
  While this method works, the syntax can be confusing, and requires you to know the exact data type of the variable.

- ### The `str.format()` Method
  Another approach is the built-in `.format()` method in Python strings.

  ```Python
  name = "Jane"
  age = 28
  
  print("Hello, {0}. You are {1} years old.".format(name, age))
  # 'Hello, Jane. You are 28 years old.'
  ```

  This method replaces the values in `{}` with variables in their given order.
  Although `.format()` improves readability, it's important to note that placeholders and variables must follow in their specific order.

  Using the example above, but swapping variables or placeholders around would return incorrectly.

## String Interpolation With f-Strings

- ### What are f-Strings?
  An f-string is a modified Python string, where it is prefixed with an `f` before the quotation marks. 
  This allows you to directly insert variables or expressions inside curly braces `{}`.

  ```Python
  name = "Jane"
  age = 28
  
  print(f"Hello, {name}. You are {age} years old.")
  # 'Hello, Jane. You are 28 years old.'
  ```
  
  As you can see, by prefixing the string with an `f`, you can embed variables directly in the string.
  This small change dramatically improves the code readability while requiring less work than other methods.
  
- ### Embedding Expressions With f-Strings
  You're not just limited to using variables in f-strings; any expression works inside curly braces.
  
  ```Python
  apples = 3
  oranges = 5
  
  print(f"You have a total of {apples + oranges} pieces of fruit.")
  # 'You have a total of 8 pieces of fruit.'
  ```
  
  Here you can see that f-strings can also be used to embed evaluated expressions inside strings.
  This is handy for calculating and formatting expressions on the fly.
  
- ### Formatting With f-Strings
  f-Strings also allow you to control how variables and expressions are displayed using format codes.
  This is useful for numbers with many decimals, or aligning output text.
  
  A practical use case for this is correctly formatting currency.
  
  ```Python
  price_per_apple = 0.2
  
  print(f"The price of apples is ${price_per_apple:.2f} each.")
  # 'The price of apples is $0.20 each.'
  ```
  
  Here, `:.2f` tells Python to display 2 digits after the decimal point.
  You can add a colon and a format specifier in your curly braces to style numbers, dates, and more.
  
## Conclusion
f-Strings provide an efficient and readable way to format strings in Python.
Compared to older approaches like the modulo operator `%` or `.format()` method, f-strings make it much easier to embed variables and expressions inline and to control how your data appears.

Throughout this tutorial, you learned not only how to use f-strings, but also why they're the recommended choice for modern Python code.
With f-strings, your programs become easier to write and maintain, letting you focus more on what your code should do, rather than on tricky formatting details.

You're now equipped to format strings effectively in Python, and to recognize when and why to use f-strings in your own projects.
