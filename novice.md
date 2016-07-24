Learning.js.

Latest version at time of writing is [ECMA-402.](http://www.ecma-international.org/ecma-402/3.0/ECMA-402.pdf);

Bit bored: So just writing.

[Google Javascript guidelines](https://google.github.io/styleguide/javascriptguide.xml)

[ECMAScript 2017 Language Specification](https://tc39.github.io/ecma262/#sec-ecmascript-data-types-and-values)

[ECMAScript compatibility table](https://kangax.github.io/compat-table/es6)

[DHS Gov](http://www.dhs.pa.gov/cs/groups/webcontent/documents/document/p_031774.pdf)

[ECMAScript engines](https://en.wikipedia.org/wiki/List_of_ECMAScript_engines)

ECMAScript is the language to which Javascript is a **dialect**, similar to LiSP re: Common Lisp, and Scheme, et al.

A conforming implementation of **ECMAScript** must **provide** and **support** all the various:
<code>
(var 
    Types
    Values, objects
    Properties
    Functions,
    Program syntax, semantics);
</code>

[[4.3.1](https://tc39.github.io/ecma262/#sec-type)]

Types of conforming implementations must be data values as per defined in section 6 of the standard.

[[6]](https://tc39.github.io/ecma262/#sec-ecmascript-data-types-and-values) states that algorithms with specification manipulate 
values. Each of which has an associated type. The possible range of value types are exactly those defined within Section 6 of the 
ECMAScript standards. 

A conforming implementation of ECMAScript **must not implement any extension that is listed as a Forbidden Extension** in 
subclause 16.1.

Types are further sub-classified into **ECMAScript language types** as well as **specification types**.

`Type(x)` is used as shorthand for `the type of x` where “type” refers to the language or specification type defined.

The `empty object pattern` also shown as `{ }` is used to check whether a value is `coercible` to an object. When `>` or `<` 
operators are applied to strings, they compare those strings only according to UTF-8 encodings by default. The `collation` order 
of the current locale on the hosted environment is not specified.

The ECMAScript language types are:

	Undefined, Null, Boolean, String, Symbol, Number, and Object.

	localCompare() is a function that provides a way to compare strings that takes collation order into account.

As we have seen, only undefined and null aren’t able to be collated:

```
({ }) = [true, false];	// Arrays  are coercible to objects
({ }) = 'abc';			// OK, strings are coercible to objects
    
({ }) = undefined;    	// TypeError
({ }) = null;			// TypeError

var s; // Array of strings to be sorted.
s.sort(function(a, b) { 
  return a.localeCompare(b);
});
```

The general consensus is that JavaScript is an **Object-Based rather Object- Oriented programming in that `JavaScript = 
ECMAScript + DOM API;`**
