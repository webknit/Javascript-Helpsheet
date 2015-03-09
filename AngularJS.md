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