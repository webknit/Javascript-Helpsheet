# Functions

## Arguments

The data that’s passed into a function

	function hello (name) {
		console.log(‘hello ’ + name)
	}

	hello(’shane’);

## Return values

Return allows us to pass a value from our function and stop the function itself.

	function hello (name) {
		if(typeof name === ‘undefined’) return 0;
		else console.log(‘hello ’ + name);
	}

	hello(); // 0

## Scope

We can declare variables inside of our functions, and they have a unique property, they exist only within that function. This is scope.

	var color = ‘red’;
	var colorGlobal = ‘blue’;

	function scope () {
		var color = ‘black’;
		colorGlobal = ‘green’;
		console.log(color);
	}

	console.log(color) // red
	function scope() // black
	console.log(colorGlobal) // green

## Anonymous functions

Functions without names are called anonymous functions, they can  be called once or simply stored in a variable.

	(function() {
		var a = “something”;
		console.log(a);
	})();

The following runs immediately it doesn’t need to be called as we executed the function with parentheses at the end something


	var thisFunc = function() {
		console.log(‘function called’);
	}

	thisFunc(); // function called