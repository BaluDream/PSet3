![image](https://github.com/BaluDream/PSet3/assets/119417439/9c2b25e7-1ba0-4b51-96ba-998113dddbc1)# PSet3
From Harvard cs50 assignments.

# Lesson Plan for Fuel Gauge
 ![Alt Text](fuel-1-screenshot.png)

 Fuel gauges indicate, often with fractions, just how much fuel is in a tank. For instance 1/4 indicates that a tank is 25% full, 1/2 indicates that a tank is 50% full, and 3/4 indicates that a tank is 75% full.

In a file called fuel.py, implement a program that prompts the user for a fraction, formatted as X/Y, wherein each of X and Y is an integer, and then outputs, as a percentage rounded to the nearest integer, how much fuel is in the tank. If, though, 1% or less remains, output E instead to indicate that the tank is essentially empty. And if 99% or more remains, output F instead to indicate that the tank is essentially full.

If, though, X or Y is not an integer, X is greater than Y, or Y is 0, instead prompt the user again. (It is not necessary for Y to be 4.) Be sure to catch any exceptions like ValueError or ZeroDivisionError.


## Hints

* Recall that a str comes with quite a few methods, per docs.python.org/3/library/stdtypes.html#string-methods, including split.

* Note that you can handle two exceptions separately with code like:

    try:
      ...
  except ValueError:
      ...
  except ZeroDivisionError:
      ...

  Or you can handle two exceptions together with code like:

    try:
      ...
    except (ValueError, ZeroDivisionError):
      ...
## Demo

  ![Alt Text](fuel-2-screenshot.png)

  ![Alt Text](fuel-3-screenshot.png)

## How to Test

Here’s how to test your code manually:

* Run your program with python fuel.py. Type 3/4 and press Enter. Your program should output:
  75% 
* Run your program with python fuel.py. Type 1/4 and press Enter. Your program should output:
  25%
* Run your program with python fuel.py. Type 4/4 and press Enter. Your program should output:
  F
* Run your program with python fuel.py. Type 0/4 and press Enter. Your program should output:
  E
* Run your program with python fuel.py. Type 4/0 and press Enter. Your program should handle a ZeroDivisionError and prompt the user again.

* Run your program with python fuel.py. Type three/four and press Enter. Your program should handle a ValueError and prompt the user again.

* Run your program with python fuel.py. Type 1.5/3 and press Enter. Your program should handle a ValueError and prompt the user again.

* Run your program with python fuel.py. Type 5/4 and press Enter. Your program should prompt the user again.


# Lesson Plan for Felipe's Taqueria
  ![Alt Text](taqueria-1-screenshot.png)

One of the most popular places to eat in Harvard Square is Felipe’s Taqueria, which offers a menu of entrees, per the dict below, wherein the value of each key is a price in dollars:

  {
      "Baja Taco": 4.00,
      "Burrito": 7.50,
      "Bowl": 8.50,
      "Nachos": 11.00,
      "Quesadilla": 8.50,
      "Super Burrito": 8.50,
      "Super Quesadilla": 9.50,
      "Taco": 3.00,
      "Tortilla Salad": 8.00
  }
In a file called taqueria.py, implement a program that enables a user to place an order, prompting them for items, one per line, until the user inputs control-d (which is a common way of ending one’s input to a program). After each inputted item, display the total cost of all items inputted thus far, prefixed with a dollar sign ($) and formatted to two decimal places. Treat the user’s input case insensitively. Ignore any input that isn’t an item. Assume that every item on the menu will be titlecased.



## Hints

* Note that you can detect when the user has inputted control-d by catching an EOFError with code like:
    try:
      item = input()
    except EOFError:
      ...
  You might want to print a new line so that the user’s cursor (and subsequent prompt) doesn’t remain on the same line as your program’s 
  own prompt.
* Inputting control-d does not require inputting Enter as well, and so the user’s cursor (and subsequent prompt) might thus remain on the same line as your program’s own prompt. You can move the user’s cursor to a new line by printing \n yourself!
  
* Note that a dict comes with quite a few methods, per docs.python.org/3/library/stdtypes.html#mapping-types-dict, among them get, and supports operations like:
  d[key]
  and
  if key in d:
    ...
  wherein d is a dict and key is a str.
  
* Be sure to avoid or catch any KeyError.

## Demo

  ![Alt Text](taqueria-2-screenshot.png)

  ![Alt Text](taqueria-3-screenshot.png)

## How to Test
Here’s how to test your code manually:

* Run your program with python taqueria.py. Type Taco and press Enter, then type Taco again and press Enter. Your program should output:
  Total: $6.00
  and continue prompting the user until they input control-d.
* Run your program with python taqueria.py. Type Baja Taco and press Enter, then type Tortilla Salad and press enter. Your program should output:
  Total: $12.00
  and continue prompting the user until they input control-d.
* Run your program with python taqueria.py. Type Burger and press Enter. Your program should reprompt the user.

* Be sure to try other foods and vary the casing of your input. Your program should behave as expected, case-insensitively.



# Lesson Plan for Grocery List

Suppose that you’re in the habit of making a list of items you need from the grocery store.

In a file called grocery.py, implement a program that prompts the user for items, one per line, until the user inputs control-d (which is a common way of ending one’s input to a program). Then output the user’s grocery list in all uppercase, sorted alphabetically by item, prefixing each line with the number of times the user inputted that item. No need to pluralize the items. Treat the user’s input case-insensitively.


## Hints

* Note that you can detect when the user has inputted control-d by catching an EOFError with code like:
  try:
    item = input()
  except EOFError:
    ...
* Odds are you’ll want to store your grocery list as a dict.

* Note that a dict comes with quite a few methods, per docs.python.org/3/library/stdtypes.html#mapping-types-dict, among them get, and 
  supports operations like:
  d[key]
  and
  if key in d:
    ...
  wherein d is a dict and key is a str.
* Be sure to avoid or catch any KeyError.

## Demo

  ![Alt Text](grocery-1-screenshot.png)

  ![Alt Text](grocery-2-screenshot.png)

  ![Alt Text](grocery-3-screenshot.png)

  

## How to Test


# Lesson Plan for Outdated
## Hints

## Demo

  ![Alt Text](url)

  ![Alt Text](url)

## How to Test
Here’s how to test your code manually:

* Run your program with python grocery.py. Type mango and press Enter, then type strawberry and press Enter, followed by control-d. Your   program should output:
  1 MANGO
  1 STRAWBERRY
* Run your program with python grocery.py. Type milk and press Enter, then type milk again and press Enter, followed by control-d. Your    program should output:
  2 MILK
* Run your program with python grocery.py. Type tortilla and press Enter, then type sweet potato and press Enter, followed by control-d.   Your program should output:
  1 SWEET POTATO
  1 TORTILLA

