# Questions

## I need 5 == 3 & 3==2 & 1==1, how do I do it?

	var num1 = 5;
	var num2 = 3;
	var num3 = 1;

	// I want those to change to, without just defining them manually.

	var num1 = 3;
	var num2 = 2;
	var num3 = 1;

## Consider the following code snippet:

	for (var i = 0; i < 5; i++) {
	  var btn = document.createElement('button');
	  btn.appendChild(document.createTextNode('Button ' + i));
	  btn.addEventListener('click', function(){ console.log(i); });
	  document.body.appendChild(btn);
	}

What gets logged to the console when the user clicks on “Button 4” and why?

## Write a function to find the longest increasing subsequence of an array of integers and return the sequence

	var numbers = [5, 9, 10, 6, 3, 7, 8, 16, 0];
	// From that i want
	var longestIncreasingSubsequence = [3, 7, 8, 16];