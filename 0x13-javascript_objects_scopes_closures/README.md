# 0x13. JavaScript - Objects, Scopes and Closures

## Learning Objectives
* Why JavaScript programming is amazing
* How to create an object in JavaScript
* What this means
* What undefined means
* Why the variable type and scope is important
* What is a closure
* What is a prototype
* How to inherit an object from another


## Requirements
   - Install Node 14
     `- $ curl -sL https://deb.nodesource.com/setup_14.x | sudo -E 

bash -'
     - $ sudo apt-get install -y nodejs
   - Install semi-standard
   - [Documentation](https://intranet.alxswe.com/rltoken/oc1-9XTUtCiIyZkdAFvoUQ)
     `- $ sudo npm install semistandard --global`


---

### [0. Rectangle #0](./0-rectangle.js)
* An empty class Rectangle that defines a 

rectangle. Using the class notation for defining 

your class.

### [1. Rectangle #1](./1-rectangle.js)
* A class `Rectangle` that defines a rectangle. 

Use the `class` notation for defining your class, 

the `constructor` must take 2 arguments `w` and 

`h`. Initializing the instance attribute `width` 

and `height` with the value of `h` and `w` 

respectively.

### [2. Rectangle #2](./2-rectangle.js)
* A class `Rectangle` that defines a rectangle. 

Use the `class` notation for defining your class, 

the `constructor` must take 2 arguments `w` and 

`h`. Initializing the instance attribute `width` 

and `height` with the value of `h` and `w` 

respectively. If `w` or `h` is equal to 0 or not 

a positive integer, create an empty object.

### [3. Rectangle #3](./3-rectangle.js)
* A class `Rectangle` that defines a rectangle. 

Use the `class` notation for defining your class, 

the `constructor` must take 2 arguments `w` and 

`h`. Initializing the instance attribute `width` 

and `height` with the value of `h` and `w` 

respectively. If `w` or `h` is equal to 0 or not 

a positive integer, create an empty object. 

Creating an instance method called `print()` that 

prints the rectangle using the character `X`.

### [4. Rectangle #4](./3-rectangle.js)
* A class `Rectangle` that defines a rectangle. 

Use the `class` notation for defining your class, 

the `constructor` must take 2 arguments `w` and 

`h`. Initializing the instance attribute `width` 

and `height` with the value of `h` and `w` 

respectively. If `w` or `h` is equal to 0 or not 

a positive integer, create an empty object. 

Creating an instance method called `print()`, 

`rotate()`, `double()` that prints the rectangle 

using the character `X`, Exchanges the width and 

the height of the rectangle, and Multiples the 

`width` and the `height` of the rectangle by 2 

respectively.

### [4. Rectangle #4](./4-rectangle.js)
* A class `Rectangle` that defines a rectangle. 

Use the `class` notation for defining your class, 

the `constructor` must take 2 arguments `w` and 

`h`. Initializing the `instance attribute` 

`width` and `height` with the value of `h` and 

`w` respectively. If `w` or `h` is equal to 0 or 

not a positive integer, create an empty object. 

Creating an instance method called `print()`, 

`rotate()`, `double()` that prints the rectangle 

using the character `X`, Exchanges the width and 

the height of the rectangle, and Multiples the 

`width` and the `height` of the rectangle by 2 

respectively.

### [5. Square #0](./5-square.js)
* A class `Square` that defines a square and 

inherits from `Rectangle` of `4-rectangle.js`. 

Use the `class` notation for defining your class 

and `extends`, the `constructor` must take 1 

argument: `size`; while the constructor of  

Rectangle must be called (by using `super()`).

### [6. Square #1](./6-square.js)
* A class `Square` that defines a square and 

inherits from `Square` of `5-square.js`. Use the 

`class` notation for defining your class and 

`extends`, Creates an instance method called 

`charPrint(c)` that prints the rectangle using 

the character `c`(If `c` is `undefined`, use the 

character `X`).

### [7. Occurrences](./7-occurrences.js)
* A function that returns the number of 

occurrences in a list. Using Prototype: 

`exports.nbOccurences = function (list, 

searchElement)`.

### [8. Esrever](./8-esrever.js)
* A function that returns the reversed version of 

a list. Using Prototype: `exports.esrever = 

function (list)`, Do not use the built-in method 

`reverse`.

### [9. Log me](./9-logme.js)
* A function that prints the number of arguments 

already printed and the new argument value. Using 

Prototype: `exports.logMe = function (item)`, 

Output format: `<number arguments already 

printed>: <current argument value>`.

### [10. Number conversion](./10-converter.js)
* A function that converts a number from base 10 

to another base passed as argument. Using 

Prototype: `exports.converter = function (base)`, 

Do not import any file, or declare any new 

variable (`var`, `let`, etc..).

### [11. Factor index](./100-map.js)
* A script that imports an array and computes a 

new array. The script must import list from the 

file `100-data.js`using a `map`. [Tips]

(https://intranet.alxswe.com/rltoken/LOEW51ZbYDjO

4KZCFevzNQ)
A new list must be created with each value equal 

to the value of the initial list, multipled by 

the index in the list. Print both the initial 

list and the new list.

### [12. Sorted occurences](./101-sorted.js)
* A script that imports a dictionary of 

occurrences by user id and computes a dictionary 

of user ids by occurrence. The  script must 

import dict from the file `101-data.js`, In the 

new dictionary: A key is a number of occurrences, 

A value is the list of user ids. Print the new 

dictionary at the end.

### [13. Concat files](./101-sorted.js)
* A script that concats 2 files. The first 

argument is the file path of the first source 

file, the second argument is the file path of the 

second source file, the third argument is the 

file path of the destination.

### [13. Concat files](./102-concat.js)
* A script that concats 2 files. The first 

argument is the file path of the first source 

file, the second argument is the file path of the 

second source file, the third argument is the 

file path of the destination.

---

## Author
* **Richard Akpabio** - [Rikpabi]

(http://github.com/Rikpabi)
