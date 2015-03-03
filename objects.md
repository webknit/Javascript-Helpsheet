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

## Prototypes

To create an object prototype we use an object constructor function, using the new keyword to create objects from the same prototype.

	function Animal(name, colour, age) {
		this.name = name
		this.colour = colour;
		this.age = age;
	}

	var sheep = new Animal('Barry', 'white', 28);

The protype property enables inheritance in JS

	function SaySomething(theSomething) {
		this.saying = theSomething || "hello";
	}

	SaySomething.prototype.say = function () {
		console.log(this.saying);
	}

	var obj = new SaySomething('I am alive today'); // I am alive today
	var obj = new SaySomething(); // hello

	obj.say();

There are two main ways the prototype is used in JS

**Prototype Property: Prototype-based Inheritance**

	function Car() {
		this.name = 'car';
		this.wheels = 4;
		this.belongs = 'On the road';
		this.isFast = true;
	}

	Car.prototype.giveDetails = function() {
		console.log('I am a ' + this.name + '. I have ' + this.wheels + 'wheels.')
	}

	Car.prototype.amIFast = function() {
		if(this.isFast) console.log('Faster than usain Bolt');
	}

	var newMotor = new Car();
	newMotor.giveDetails(); // I am a car I have 4 wheels
	newMotor.amIFast(); // Faster than usain Bolt

	function FordCar(model, litre) {
	  this.model = model;
	  this.litre = litre;
	}

	// This inherits all of the car properties
	FordCar.prototype = new Car();

	FordCar.prototype.sayCarModel = function() {
	  console.log('This is a Ford ' + this.model + ' ' + this.litre);
	}

	var escort = new FordCar('escort', 1.3);

	escort.amIFast(); // Faster than usain Bolt
	escort.sayCarModel(); // This is a Ford escort 1.3

**Prototype Attribute: Accessing Properties on Objects**

	function Family() {
	  this.surname = 'Prendergast';
	  this.location = 'Scarborough'; 
	}

	var me = new Family();
	me.location = 'Macclesfield'

	var mySister = new Family();
	mySister.surname = 'Beckham';

	console.log(me.surname); // Prendergast
	console.log(me.location); // Macclesfield

	console.log(mySister.surname); // Beckham
	console.log(mySister.location); // Scarborough



