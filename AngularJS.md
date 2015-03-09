# Angular JS

AngularJS is a MVC framework which operates on the client-side. It allows you to do things such as 

- Manipulating the DOM
- Allows you to write custom HTML declarations
- Manage the states of Model(s)
- Integreate with other UI tools

## Four main elements of Angular

- Directives
- Factories
- Controllers
- Filters

### Directives
The fundamental building blocks fo Angular. they serve as the definitions for various declarations you want to use within your Angular application.

**Example**
A module that says "make this input field a date picker".
Building a contact info card out of data of a person object. 

### Factories
Used to maintain one single instance of something. They can be used for maintaining state. Additionally, they can be used to provide an abstraction layer between your directives and your API's.

### Controllers
Have a lot of similar functionality to directives, but they are predominantly used for data connections and logical restraints around them. Unlike a directive, they can't contain any extra temlating or complex ordering.

**Example**
Commonly used as the parent for a specific page or view that collects all the necessary data, whereas directives are the individual models and pieces that make up that view.

### Filters
Used to implement temporary transformations of data as it travles between the model and the view.

**Example**
An UPPERCASE filter than chanes all the text into capital letters.
Limiting or order some datat before piping it into an NG repeat. The original array/data always stays the same, it's just the display that changes.

## Two way binding

> Data-binding in Angular apps is the automatic synchronization of data between the model and view components. The way that Angular implements data-binding lets you treat the model as the single-source-of-truth in your application. The view is a projection of the model at all times. When the model changes, the view reflects the change, and vice versa.

	<select ng-model="user.name">
		<option value="Shane">Shane</option>
		<option value="Dave">Dave</option>
		<option value="Alex">Alex</option>
	</select>

## ng-model

ng-model represents the specific property that we want to bind input to. It could be a top level property such as 'name', or nested within another object such as 'user.name'.

	<input type="text" ng-model="name" />
	<input type="text" ng-model="user.name" />

	// iterate over an ayyary and output fruit names
	angular.module('myApp', [])
		.controller('myController', function ($scope, $http) {
			$scope.bowlOfFruit = [
			{name: 'Apple'},
			{name: 'Pear'},
			{name: 'Orange'}
		];
	});

	<ul>
		<li ng-repeat="name in bowlOfFruit"> {{name}} </li>
	</ul>

For read access, eg output into an input field, you can use..

	{{property}}


## ng-list

A directive that transfroms a character seperated list into an actual data array for storage, and vice-versa.

	<input type="text" ng-model="name.emails" ng-list />


