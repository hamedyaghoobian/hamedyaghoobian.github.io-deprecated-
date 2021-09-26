---
title: Conditionals in Python
linktitle: Conditionals
type: book
date: "2021-08-20"
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
---

* Your program may need to test for certain conditions and take certain actions based on those conditions.
    * If the user inputs the wrong data
    * If the end of the file has been reached
    * If a sufficient number of actions have been performed


* Conditional statements provide this functionality
    * No additional modules needed


## Alternative Execution or Branches
* `if else` statements allow for certain operations to happen in predefined cases

    ```python
    if expression:
        Statements executed if True
    else:
        Statements executed if False
    ```
* Indentations instruct Python on how to group instructions


## Chained conditionals
* Sometimes there are more than two possibilities and we need more than two branches. One way to express a computation like that is a **chained conditional**.

* `if`, `elif`, and `else` allow for multiple conditions to be tested one after another
    * The first expression to resolve to True ends the testing

        ```python
        if expression1:
            Statements if expression1 true
        elif expression2:
            Statements if expression1 false and expression2 true
        else:
            Statements if expression1 and expression2 are false
        ```

## Expressions
* Resolves to `True` or `False`, `1` or `0`, a boolean type

* Equality
    * `==`
    * `!=`

* Relational
    * `<`
    * `>`
    * `<=`
    * `>=`


## Nested if-else
* Conditional statements can be nested inside other conditionals 
    * Need to keep track of indentations
        ```python
        if expression1:
            if expression2:
                Statements if expression1 True and expression2 True
        else:
            Statements if expression1 False
        ```



## Sequential if-else
```python
if expression1:
    Statements
if expression2:
    Statements 
if expression3:
    Statements
# All three expressions will be evaluated
```

```python
if expression1:
    Statements
elif expression2:
    Statements 
elif expression3:
    Statements

# All three expressions may be evaluated 
# The first one to resolve to True will end the evaluation
```

## Logical Operators
* We do not necessarily need one `if statement` for each expression
* Compound expression can be created using logical operators
    * `and`
    * `or`
    * `not`
     
        ```python
        if expression1 and expression2:
            statements
        ```
* Common concepts in Boolean Algebra
    * Set Theory, Propositional Logic, Circuits


## Short Circuiting
* Compound expressions need not be fully evaluated

* First expression connected with `and` to return `False` causes the entire compound expression to be `False`

* First expression connected with `or` to return `True` causes the entire compound expression to be `True`

* Keep in mind how the expressions are grouped! :point_up:


## Order of Precedence :pencil2:	
1. `()`
2. `not`

3. `*` `/` `%` `+` `-`

4. `<`   `<=`   `>`   `>=`

5. `==`   `!=`

6. `and`

7. `or`


## Strings Testing
* Comparing equality
    * `==` `!=`
    * Returns a bool
    * Checks one character at a time

* Check if a particular phrase or character is `in` a string
    * `in` e.g., `"test" in myString`

* Check if a particular phrase or character is NOT in a string
    * `not in` e.g., `"test" not in myString`

* Return the number of characters in a string
    * `len(myString)`


## Modifying Strings
* Return the string in all upper case
    *  `.upper()` e.g., `myString.upper()`

* Return the string in all lower case
    * `.lower()` e.g., `myString.lower()`

* Return the string with all leading and trailing whitespace removed
    * `.strip()` e.g., `myString.strip()`

* Return the string with specified parts replaced
    * `.replace("target","replacement")` e.g., `myString.replace("target","replacement")`

## Random
* Python provides the ability to generate random numbers
    * `import random` at the beginning of the program
* `random.random()`
    * Generates a random floating point value between `[0.0,1.0)`
* `random.randint(val1,val2)`
    * Generates a random integer value between `[val1,val2]`
    * `val1` and `val2` must be integer values
* `random.uniform(val1,val2)`
    * Generates a random floating point value between `[val1,val2]`
    * `val1` and `val2` must be floating point values

## Random Range
* `random.randrange(val1)`
    * Generates a random integer value between `[0,val1)`
    * `val1` must be an __integer__ value

* `random.randrange(val1,val2)`
    * Generates a random integer value between `[val1,val2)`
    * `val1` and `val2` must be __integer__ values

* `random.randrange(val1,val2,val3)`
    * Generates a random integer value between `[val1,val2)` in `val3` step intervals
    * `val1`, `val2`, and `val3` must be integer values


## Pseudorandom
* Random numbers are generated according to complex mathematics
    * They need a starting value to perform the processes on to generate the first number
* Seed value is this input value!
    * Python uses the current system time by default
        * number of seconds since **Jan 1, 1970** or the epoch
    * `random.seed(val)` specifies the seed value!
        * `val` must be an integer
* Random number generation is often cyclic
    * Better generators have larger periods between cycles
    * Better generators may be very complex and intensive to run
