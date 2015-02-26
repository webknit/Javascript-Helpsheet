# Objects

## Structure

	var myInfo = {
		name: 'shane',
		skills: ['html', 'CSS', 'JS'],
		'position held': 'Web developer',
		sayHello: function() {
			console.log('Hi my name is ' + this.name);
		};
	}

	var mateInfo = {
	  name: 'john',
	  sayHello: myInfo.sayHello
	}

	console.log(myInfo.name); // shane
	console.log(myInfo['position held']); // web developer
	myInfo.sayHello(); // Hi my name is shane
	mateInfo.sayHello(); // Hi my name is john

## Call
Call enables us to add an extra argument which determines which value should be bound to this when calling the function

	var myInfo = {
		name: 'shane',
		skills: ['html', 'CSS', 'JS'],
		'position held': 'Web developer',
		sayHello: function() {
			console.log('Hi my name is ' + this.name);
		};
	}

	var mateInfo = {
	  name: 'john',
	  sayHello: myInfo.sayHello
	}

	var sayIt = myInfo.sayHello;

	sayIt.call(myInfo); // Shane
	sayIt.call(mateInfo); // john
	sayIt.call({}); // Undefined
	sayIt.call({name : 'Harry'}); // Harry
	sayIt.call(); // Window
	myInfo.sayHello.call({name: 'Sally'}); // Sally

## Apply 

Call and apply differ on how they can take arguments. You pass the arguments via arrays and it provides us with a way to dynamically call functions.

	var myInfo = {
		name: 'shane',
		skills: ['html', 'CSS', 'JS'],
		'position held': 'Web developer',
		sayHello: function(greeting, statement) {
	    greeting = greeting || "Hi ";
	    statement = statement || "you ok?";
			console.log(greeting + " I'm " + this.name + " " + statement);
		};
	}

	var mateInfo = {
	  name: 'john',
	  sayHello: myInfo.sayHello
	}

	var sayIt = myInfo.sayHello;

	sayIt.call(myInfo); // Shane
	sayIt.apply(myInfo); // Shane
	myInfo.sayHello("Howdy ", "I'm on fire!"); // Howdy I'm Shane on fire
	sayIt.call(mateInfo, "Hey ", "I'm good thanks"); // Hey I'm John good thanks
	sayIt.apply({name: 'Susan'}, ["Hii ", "I'm ok"]); // Hii I'm Susan I'm ok

	var newPerson = ['Bonsoir', 'Je vais bien'];
	myInfo.sayHello(newPerson); // Bonsoir, Je vais bien Im shane you ok
	myInfo.sayHello.apply({name: 'Luc'}, newPerson); // Bonsoir I'm Luc Je vais bien
