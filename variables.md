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

They are, however, considered to be two different types.
	alert(typeof TestVar); //shows undefined
	alert(typeof TestVar); //shows object