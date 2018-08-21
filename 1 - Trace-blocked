## 2.1 - padStart - trace - blocked 

First step in exploring the code. Split the code in three objects : 

  * _arguments_ : the arguments are not Hoisted. Easier to consider it "declared" at the top of the analysis, as they are passed to the function via the function call.
  * _dependencies_ : check the documentation for that. You can go as deep as you want (dependencies of dependencies ...) depensing of you goal. 
  * _"function"_ : Everything in the third object should refer to methods/variables defined in the first two objects.

This code is not supposed to run. The goal is : 
  * understand dependancies;
  * To break down the function -> Trace block

Example for the three objects :

First Objects : arguments
```
let args = {
		string: undefined,
		length: undefined,
		chars: undefined
 	};
  ```
Second Object : dependencies  
```
let dep = {
	toInteger: {
			args: {
				anything: "the value to convert"
			},
			returns: {
				number: "the converted integer"
			},
			behavior: "Converts `value` to an integer."
		},
(...)
}
```
Third object : "function"
```
 let ret_val;
	padStart: {
		args.string = dep.toString(args.string);
		args.length = dep.toInteger(args.length);
(...)
		break padStart;
	};
} 
```
