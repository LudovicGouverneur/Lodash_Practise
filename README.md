# Lodash_Practise

[l - Trace-Blocked](Lodash_Practise/1 - Trace-blocked.md)

### 0 - Index
* [docs](#docs)
* [input analysis](#input-analysis)
* js files : 
  * 0 - padStart : contains code to study with its documentation
  * 1 - padStart - trace - blocked 
* [part-task](#part-task)
* [recap](#recap)
* [helpful links](#helpful-links)

Documentation : https://lodash.com/docs/4.17.10
In this exercice, we practice 4 steps analysis of a piece of code. This piece of code is a part of the lodash library : padstart.

## 1 - Padstart - Pre-analysis
  * padstart : https://lodash.com/docs/4.17.10#padStart 
  * Remark on dependencies. Depencies are not freedom. The darkside of opensource is that you depends on some other people's dependencies. This is a question we should ask ourself : can I build it myself.
  * module lodash, module dot export. : https://github.com/elewa-academy/module-dot-exports.git
  
## 1.1 - [Docs](https://lodash.com/docs/4.17.10#padStart)

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

## 1. 2 Input Analysis

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

## 2.1 - padStart - trace - blocked 

First step in exploring the code. Split the code in three objects : 

  * _arguments_ : the arguments are not Hoisted. Easier to consider it "declared" at the top of the analysis, as they are passed to the function via the function call.
  * _dependencies_ : check the documentation for that. You can go as deep as you want (dependencies of dependencies ...) depensing of you goal. 
  * _"function"_ : Everything in the third object should refer to methods/variables defined in the first two objects.

This code is not supposed to run. The goal is : 
  * understand dependancies;
  * To break down the function -> Trace block


    
## Recap

Summarize what you've learned and struggled with studying this functionn.
