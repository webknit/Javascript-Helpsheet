# Strings

## Escape characters
	var sentence = ’you\’re not going to believe this’;

## Concatenation
Adding two strings together
	var full = part1 + part2;

## Methods
Finding the length of a string
	var sentence = “Shane is here”;
	var sentenceLength = sentence.length;
	console.log(length) // 13;

The indexOf() method returns the position of the first occurrence of a specified value in a string. zero indexed remember and it’s case sensitive.
	var sentence = “Shane is here”
	var sentenceIndex = sentence.indexOf('is');
	var sentenceIndex2 = sentence.indexOf(‘Here’);

	console.log(sentenceIndex); // 6
	console.log(sentenceIndex2); // -1

Check if something exists in a string
	console.log(sentence.indexOf(‘Here’) !== -1); // False

The charAt() method returns the character at the specified index in a string.
	var sentence = “Shane is here”
	console.log(sentence.charAt(1)); // S

The substr() method extracts parts of a string, beginning at the character at the specified position, and returns the specified number of characters.
	var sentence = “Shane is here”
	console.log(sentence.substr(1, 4)); // “hane”

The toLowerCase() method converts a string to lowercase letters.
	var sentence = “Shane is here”
	console.log(sentence.toLowerCase()); // “shane is here”

The toUpperCase() method converts a string to uppercase letters.
	var sentence = “Shane is here”
	console.log(sentence.toLowerCase()); // “SHANE IS HERE”

## Comparing strings
	== equal to
	=== equal value and equal type
	!= not equal
	!== not equal to or not exact value
	< Less than
	<= Less than or equal to
	> Greater than
	>= Greater than or equal to

Example
	var one = “one”;
	var two = “two”

	if(one === two) return true
	else return false