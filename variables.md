# Variables

## Null and undefined
Undefined means a variable that has been declared but not assigned.

	var TestVar;
	alert(TestVar); //shows undefined

Null is an assignment variable, it is assigned to a variable as a representation of no value.

	var TestVar = null;
	alert(TestVar); //shows null

	undefined == null // shows true
	null == undefined // shows true

*** Scope
Scope is the set of variables, objects, and functions you have access to.

	var fname = “shane”;

	function myFunc() {
		var lname = “prendergast”;
	}

	console.log(fname) // shane
	console.log(lname) // undefined

*** Shadowing
Shadowing is where a variable declared within a certain scope has the same name as one declared in outer scope.

	var fname = “shane”;

	function myName() {
		var name = fname + “prendergast”;
	}

*** Hoisting
In short, hoisting is when JavaScript moves variable and function declarations to the top of their scope before any code is executed.
Rather than me trying to explain it I am just going to link to the best - and extensive - description I've come across
http://howchoo.com/g/ythlzdq1mzb/understanding-javascript-hoisting