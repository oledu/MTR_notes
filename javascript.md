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

Primitive Value
####  *Comparde by value*
the content is comapared:
`3===3`
**`true`**

####  *Always immutable*  	
Properties can't be changed, added or removed		
`var str = 'abc';`	
`str.length = 1; // try to change property length`	
`str.length // ⇒ no effect` 	
`3`

