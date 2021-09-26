---
# Loops
linktitle: Week 4
summary:  
weight: 4
icon: book-reader
icon_pack: fas

# Page metadata.
title: Week 4
date: "2021-09-15"
type: book  # Do not modify.
---

## Variable Reassignment & Updates :zap:
```console
>>> a=5
>>> b=a     #a and b are now equal
>>> a=3     #a and b are no longer equal
```
### Updating variables
* Before we can update a variable, we need to __initialize__ it:
```console
>>> x = x + 1
NameError: name 'x' is not defined
>>> x = 0
>>> x = x + 1
>>> x
1
```

* Updating a variable by adding 1 is called an increment; subtracting 1 is called a decrement.

## Loops
* Provide us with a control structure to repeatedly perform actions

* Python provides two styles of loops
  * `while` loops
  * `for` loops



## While Loop

```python
while expression:
    statement1
    statement2
    statement3
```

* Expression can be testing for a particular value, or a range!
  * May not know how many times the loop will execute

* A single pass through the statements of a loop is called an iteration

* Must be careful not to loop infinitely!



## Break 

* `break` statement exits the loop when called
* Typically used in conjunction with an `if` statement

    ```python
    while expression:
        statement1
        break
        #everything after this does not get executed
        statement2
        statement3
    ```



## Continue
* `continue` statement jumps back to the expression test
    * Typically used in conjunction with an `if` statement

    ```python
    while expression:
        statement1
        continue
        #everything after this does not get executed
        statement2
        statement3
    ```




## While-Else
* An `else` statement may be added to the end of the `while` loop as a final block of statements to be executed
* May be useful if some clean-up must be performed after the `while` loop is complete (closing files, clearing data structures, resetting variables)

    ```python
    while expression:
        statement1
        statement2
        statement3
    else:
        statement 4
        statement 5
    ```

## Sentinel Values
* Sometimes the program needs to loop until the user specifies a stopping point
    * "Enter your id number and press # when complete"
* Sentinel values are values outside the range of normal input values
    * Y/N
    * -1
    * \#
* We can test if the sentinel value has been entered in the while loop
    * May need to initialize the variable appropriately first
        ```python
        while userChoice != -1:
        ```

## `For` Loop
* For loops iterate through a range of specified values 
    ```python
    for x in [1,2,3,4]:
        statement1
        statement2
        statement3
    ```
* `x` is known as the index variable and stores the current value
* `[1,2,3,4]` is a data structure known as a __List__
    * We could store text as well `["a","b","c"]`
    * We will discuss __Lists__ more later


## Range
* Instead of explicitly listing all values, we can define a range instead using the `range()` function
* ```python
    for x in range(val1):
    ```
    * Iterates through all __integer__ values between `[0,val1)`
    <!-- * val1 must be an __integer__ value -->
* ```python 
    for x in range(val1,val2):
    ```
    * Iterates through all __integer__ values between `[val1,val2)`
    <!-- * `val1` and `val2` must be __integer__ values -->
* ```python
    for x in range(val1,val2,val3):
    ```
    * Iterates through all __integer__ values between `[val1,val2)` in `val3` step intervals
    <!-- * `val1`, `val2`, and `val3` must be __integer__ values -->


## Break and Continue
* `break` and `continue` work with for loops as well!
* `break` still exits the loop immediately
    ```python
    for x in [1,2,3,4]:
        statement1
        break
        statement2
    ```	
* `continue` moves to the next value and restarts the loop body
    ```python
    for x in [1,2,3,4]:
        statement1
        continue
        statement2
    ```


## Shorthand Operators
* It is often the case that we need to add some value to an already existing variable
    * Shorthand operators help make this less code intensive
* `x += 1`
    * `x = x + 1`
* `x -= 1`
    * `x = x - 1`
* `x *= 1`
    * `x = x * 1`
* `x /= 1`
    * `x = x / 1`
* `x %= 1`
    * `x = x % 1`
