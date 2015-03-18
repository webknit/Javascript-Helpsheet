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

## Using the JS and that array of objects output the mountain data in the example format provided

	// EXAMPLE CODE REQUIRED

	table  { border-collapse: collapse; }
	td, th { border: 1px solid black; padding: 3px 8px; }
	th     { text-align: left; }

	<table>
	<tr>
		<th>name</th>
		<th>height</th>
		<th>country</th>
	</tr>
	<tr>
		<td>Kilimanjaro</td>
		<td>5895</td>
		<td>Tanzania</td>
	</tr>
	</table>

Now here's the JS and array to work with

	var MOUNTAINS = [
	  {name: "Kilimanjaro", height: 5895, country: "Tanzania"},
	  {name: "Everest", height: 8848, country: "Nepal"},
	  {name: "Mount Fuji", height: 3776, country: "Japan"},
	  {name: "Mont Blanc", height: 4808, country: "Italy/France"},
	  {name: "Vaalserberg", height: 323, country: "Netherlands"},
	  {name: "Denali", height: 6168, country: "United States"},
	  {name: "Popocatepetl", height: 5465, country: "Mexico"}
	];

	function buildTable(data) {
	  // CODE IN HERE
	}

	buildTable(MOUNTAINS);

Codepen is here http://codepen.io/anon/pen/bNQJro


