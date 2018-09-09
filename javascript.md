### comment 
- //... for single line comment
- /* ... * / for multiline comment

### Primitive value Versus Objects
- *primitive values*: boolenans, numbers, null and undefined
- Object: All others
- Non-value: undefined, null

```
>var obj1 = {}; // an empty object
>var obj2 = {}; // another empty	
>object > obj1 === obj2
false
>obj1 === obj1
true
```
```
>var prim1 = 123;
>var prim2 = 123;
>prim1 === prim2	;
true	
```
### Primitive Value
####  *Comparde by value*
the content is comapared:

####  *Always immutable*  	
Properties can't be changed, added or removed

### Object
#### Compared by reference
Identities are compared; every value has its own identity

```
>{} === {}  // two different empty objects
false
```
#### Mutable by default
You can normally freely change, add, and remove properties

#### undefined and null
- undefined and null have no proerties
- undefined means “no value.”
- null means “no object.”

### Categorizing Values Using typeof and instanceof
- There are two operators for categorizing values: typeof is mainly used for primitive values, while instanceof is used for objects.
- typeof null returning 'object' is a bug that can’t be fixed, because it would break existing code. It does not mean that null is an object.

### Booleans
The primitive boolean type comprises the values true and false. The following oper‐ ators produce booleans:
- Binary logical operators: && (And), || (Or)
- Prefix logical operator: ! (Not)
- Comparison operators:
 Equality operators, Ordering operators

#### Truthy and Falsy
- false: undefined, null, false, -0, NaN and ''
- true: All other values

#### Binary Logical Operators
Binary logical operators in JavaScript are ***short-circuiting.
***
#### Equality Operators
- Normal, or “lenient,” (in)equality: == and !=
- Strict (in)equality: === and !==

***always using strict equality is recommended***

### Numbers
All numbers in JavaScript are floating-point:
```
>1=== 1.0;
true
```
- NaN
-Infinity

### Strings
- The backslash (\) escapes characters and produces a few control characters.

- Strings are concatenated via the plus (+) operator.
```
>var messageCount = 3;
>'You have ' + messageCount + ' messages'
'You have 3 messages'
```

#### Strings Methods
- string.slice()
- string.trim()
- stirng.indexOf()

### Conditionals
- if-else statement
- switch statement

### Loops
- for loop
- while loop
- ***break leaves the loop***
- ***continue starts a new loop iteration***

### Functions
A function expression produces a value and can thus be used to directly pass functions as arguments to other functions.
- Function declarations are **hoisted**.That allows you to refer to functions that are declared later.
- Additional parameters will be ignored
- The Special Variable ***arguments***
- Missing parameters will get the value undefined

### Optional Parameters
assigning default values to parameters:
```
function pair(x, y) { 
	x = x || 0; // (1) y=y||0; 
	return[x,y];
}
> pair()
[ 0, 0 ]
> pair(3)
[ 3, 0 ]
> pair(3, 5)
[ 3, 5 ]
```
### Strict Mode
To switch it on, type the following line first in a JavaScript file or a < script > tag:
`'use strict';`

**also enable strict mode per function**



### Objects and Constructors

#### Single Object
- Directly create plain objects, via object literals:

```
'use strict';
var jane={
        name: 'Jane',
		describe: function () {
			return 'Person named '+this.name;
		} 
};
```
- You can read (“get”) and write (“set”) properties:
```
> jane.name  // get
'Jane'
> jane.name = 'John';  // set
> jane.newProperty = 'abc';  // property created automatically
```

- Function-valued properties such as describe are called methods:
```
> jane.describe()  // call method
'Person named John'
> jane.name = 'Jane'; 
> jane.describe() 
'Person named Jane'
```
- The in operator checks whether a property exists:
```
> 'newProperty' in jane
true
> 'foo' in jane
false
```
- The delete operator removes a property:
```
> delete jane.newProperty
true
```
#### Arbitrary Property Keys
use square brackets to get and set the property:
```
> var obj = { 'not an identifier': 123 }; 
> obj['not an identifier']
123
```
#### Functions Inside a Method
If you extract a method, it loses its connection with the object.

```
'use strict'; 
var jane={
	name: 'Jane',
	describe: function () {
		return 'Person named '+this.name;
	}
}
```
- We want to extract the method describe from jane, put it into a variable func, and call it. 


