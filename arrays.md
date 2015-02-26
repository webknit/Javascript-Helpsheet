# Arrays

## Getting and setting

	var nameArray = [‘shane’, ‘john’, ‘paul’];
	var firstname = nameArray[0];

Setting/getting a function in array

	var myArray = [‘shane’, 28, function(num){ return a * 2}];
	var myFunc = myArray[2];
	console.log(myFunc(2)) // 4

Setting

	nameArray[1] = ‘Jason’;

Adding the end of array

	nameArray[nameArray.length] = ‘New string’;

## Methods

var myArray = [1,2,3,4];

push to end of array
	
	myArray.push(5);

pulls the last element from an array

	var value = myArray.pop();

unshift adds element to start of the array
	
	myArray.unshift(0);

shift removes the first element

	var value = myArray.shift();

Sort the array

	var sorted = myArray.sort();
	With a compareFunction
	var sorted = myArray.sort(function(a, b){return a-b});

Reverse the array

	var revSorted = myArray.reverse();

combine arrays

	var x = [1,2,3];
	var y = [4,5,6];
	var z = x.concat(y);
	var a = z.concat([7,8,9]);

## Slice

Pull out part of an array

	var arr = [0,1,2,3,4,5];
	var sliceIt = arr.slice(1,4); // 1,2,3

## Join

join arrays together

	var words = [‘here’, ‘are’, ’some’, ‘words’];
	var sentence = words.join(‘ ’); // here are some words
	var sentence = words.join(‘-’); // here-are-some-words