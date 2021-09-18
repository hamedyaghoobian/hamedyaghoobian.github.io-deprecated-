---
title: Python Basics I
linktitle: Basics I
type: book
date: "2021-08-20"
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
---

## Program Structure
* Programs are a series of statements (instructions) that the computer executes in sequence, typically **top to bottom**.

* Statements
    * Store a value to a variable
    * Access a value from a variable
    * Perform a calculation (addition, subtraction, multiplication, etc.)
    * Perform a comparison (less than, greater than, equal to, etc.)
    * Swap control of the program between different groupings of instructions (more on functions later)


## Variables
* Stores data in a program
    * Integers
    * Floating points numbers
    * Strings
    * Booleans
    * Data structures
    * Objects
* Variable names
    * Helps humans identify variables
    * Represent a slot in memory

## Variable Usage
* Declaration and Assignment
    * `pop_count = 500`

* Expression
    * `totalPop = pop_count*2`

* Variables must be assigned data in declared

# Variable Rules
* Variable names are called identifiers
* Choosing variable names
    * Use meaningful names that represent data to be stored
* First character must be 
    * a letter
    * the underscore character
* Remaining characters must be
    * letters
    * numbers
    * underscore character
* Variable names are **case sensitive**!


## Python Reserved Words (keywords)

* Must be used as defined in the language
* Cannot be used as identifiers
* No object can have the same name as a **reserved word**.
* entirely lowercase, except for `False`, `None`, and `True`
* `help("keywords")` in Python interpreter

  ```
  False	    def	    if	        raise
  None	    del	    import	return
  True        elif    in	        try
  and	    else    is          while
  as          except  lambda	with
  assert      finally nonlocal	yield
  break	    for	    not	
  class	    from    or	
  continue    global  pass
  ```


### Identifiers

Are the following valid identifiers?
* `distance`
* `1x`
* `x_1`
* `rate%`
* `x_sum`
* `pass`
* `initial_time`
* `DisTaNce`
* `X&Y`
* `first-rate`
* `server`


## Arithmetic

Numeric Expressions | Operations 
:---:        |    :----:
$+$                 | addition     
$-$       | subtraction        
$*$   | multiplication
$/$   | division
$\%$   | modulus (remainder division)
$**$  | exponentiation



### Precedence Rules
Follows basic PEMDAS/BODMAS rules
1. $()$
2. $**$
2. unary $-$
3. $*$ $/$ $\%$
4. $+$ $-$
5. left-to-right

Let's try this with `a=1` `x=3` `y=5`: 
`z = a + ((x*-y / 5)**2)`


## String Operations
Some operators apply to strings
* `+` implies **concatenation**
* `*` implies **multiple concatenation**
Python knows when it is dealing with a string or a number and behaves appropriately. 

  ```console
  >>> print('abc' + '123')
  Abc123
  ```
  ```console
  >>> print('Hi' * 5)
  HiHiHiHiHi
  ```
Let's try `print('Hi'+5)` in Python interpreter and see what happens? What should we do to fix it? 



## Data Types
* Data can come in many forms
    * Numbers, text, complex representations

* Python recognizes seven major types of data
    * __Numeric__: integers, floating point, complex
    * __Text__: strings
    * __Boolean__: Boolean (true/false)
    * Sequence: list, tuple, range
    * Mapping: dictionary
    * Set: set, frozen set
    * Binary: byte, byte array


## Numeric Variables
* Python determines a numeric variable's type on the fly
    * Integer (whole number)
    * Floating point (real number)
    * Complex (real number plus imaginary component)

  ```console
  >>> a = 5
  >>> type(a)
  <class 'int'>
  ```
We can determine what a variable’s type is by using `type(var)`. Let's try `b = 6.5` and then `c = a + b`. 


## Text Variables
* Text data is stored as a string, i.e. a sequence of characters
    * Letters, digits, punctuation, spaces, emojis, other symbols, etc.

* Two types of strings
    * String literal: a sequence of character between a pair of single or double quotes (“ or ‘)
    * `"This is a string literal"`
    * `'As is this'`
* String variable: a variable that has been assigned a string value
    * `quote = "The right man in the wrong place can make all the difference in the world."`


Sometimes we want to include `“` and `‘` as symbols inside our strings
* The `\` symbol acts as an escape character in our string: It allows certain symbols to be interpreted differently.

Escaped Character | Result
:---:        |    :----:
`\'`         | Single quote     
`\"`       | Double quote        
`\\`   | Blackslash
`\n`   | New line
`\t`   | Tab


## Boolean Variables
* Sometimes it is helpful to store whether a situation is true or false
    * Does the player have an item?
    * Can the player enter the next area?
    * Should the cut scene play?

* Booleans represent two values `True` and `False`
* False = 0
* True = any other value, but usually 1

:exclamation: We will work with this more when we get to conditionals.
