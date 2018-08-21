# Lodash_Practise

### Index
* [docs](#docs)
* [input analysis](#input-analysis)
* [part-task](#part-task)
* [recap](#recap)
* [helpful links](#helpful-links)

Documentation : https://lodash.com/docs/4.17.10
In this exercice, we practice 4 steps analysis of a piece of code. This piece of code is a part of the lodash library : padstart.

## Padstart
  * padstart : https://lodash.com/docs/4.17.10#padStart 
  * Remark on dependencies. Depencies are not freedom. The darkside of opensource is that you depends on some other people's dependencies. This is a question we should ask ourself : can I build it myself.
  * module lodash, module dot export. : https://github.com/elewa-academy/module-dot-exports.git
  
## Documentation

general introduction and overview
___

### [Docs](https://lodash.com/docs/4.17.10#padStart)

> _.padStart([string=''], [length=0], [chars=' '])

_Behavior_
Pads string on the left side if it's shorter than length. Padding characters are truncated if they exceed length.

_Arguments_
```
[string=''] (string): The string to pad.
[length=0] (number): The padding length.
[chars=' '] (string): The string used as padding.
```

_Returns_
```
(string): Returns the padded string.
```

_Example_
```js
_.padStart('abc', 6);
// => '   abc'
 
_.padStart('abc', 6, '_-');
// => '_-_abc'
 
_.padStart('abc', 3);
// => 'abc'
```


___

### Input Analysis

Consider as much input classification as possible.

| string: to_pad | number: length | string: padding
|---|---|---|
| escaped charecters | not + integer | escaped charecters |
| wrong type | * neg int | empty string |
| empty string | * pos decimal | wrong type |
| | * neg decimal | longer than number |
| | * Infinity | |
| | * NaN | |
| | is a pos. int | |
| | too long | |
| | string number | |
| | shorter than to_pad | |
| | longer than to_pad | |
| | equal to to_pad | |

___

### Recap

Summarize what you've learned and struggled with studying this function.
