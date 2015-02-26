# Numbers

## Parsing numbers from strings
The parseInt() function parses a string and returns an integer.

	var string = “197”;
	var parseInt(string);
	Optional parseInt(string, 10);
	// This ensures it will always be done in base 10.

## Operators

	+ plus 
	- Minus
	/ divide
	% modulas
	++ increment
	— decrement

## The Math object

Random number

	var num = Math.random();
	var numOneAndTen = Math.random() * 10;

Round numbers(2.49 will be rounded down, 2.5 will be rounded up.)

	var numWhole = Math.round(2.6); // 3

Round numbers down

	var numDwon = Math.floor(3.7); // 3

Round numbers up

	var numUp = Math.ceil(3.7); // 4