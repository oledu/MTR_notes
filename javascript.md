## comment 
- //... for single line comment
- /* ... * / for multiline comment

## Primitive value Versus Objects
- *primitive values*: boolenans, numbers, null and undefined
- Object: All others
- Non-value: undefined, null

`var obj1 = {}; // an empty object`	

`var obj2 = {}; // another empty`	

`object > obj1 === obj2`	

**`false`**	

`obj1 === obj1`	

**`true`**

`var prim1 = 123;`	
`var prim2 = 123; > prim1 === prim2`	
`**true**`	

### Primitive Value
####  *Comparde by value*
the content is comapared:

####  *Always immutable*  	
Properties can't be changed, added or removed

### Objects
#### Compared by reference
Identities are compared; every value has its own identity
` >{} === {}  // two different empty objects`
**`false`**

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
Binary logical operators in JavaScript are short-circuiting.


