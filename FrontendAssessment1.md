#Frontend Assessment Part 1

#HTML

What does "semantic markup" mean?  
	Semantic elements describe their meaning or purpose clearly to the browser and to the developer. Instead of <div> you'd see <header> 
What does a doctype do?
	Doctype, or Document Type Declaration associates the document with a Document Type Definition.
Explain what standards and standards bodies are and why they are important.
	W3C is a standards body that recommends standards for the development of web technology, to promote cross browser compatability.  Standards are important to create ease of communication of data.
What are CSS3 and HTML5? How are they different from previous standards? 
	CSS3 and HTML5 are the current standards for presenting style and content, respectively.
Why is this important?  Browser versions only support given web standards.  CSS3 and HTML5 are standards for current browsers to support, that allow web developers to create projects with a normalized base in mind.

#CSS

What does a CSS reset do and why is it useful? The goal of a reset stylesheet is to reduce browser inconsistencies in things like default line heights, margins and font sizes of headings.  Its can help ensure content is visible to all users.  
What is the box model? Draw a picture and label the portions here.	
	CSS box model is essentially a box that wraps around HTML elements, and it consists of: margins, borders, padding, and the actual content.

	Margin-----------------------
	|	Border--------------	|
	|	|	Padding------|	|	|
	|	|	|			 |	|	|
	|	|	|___content__|	|	|
	|___________________________|

What is the difference between positioned element?... 
Relative - The element is positioned relative to its normal position, so "left:20" adds 20 pixels to the element's LEFT position
Fixed - The element is positioned relative to the browser window
Absolute - The element is positioned relative to its first positioned (not static) ancestor element
Statically - Default value. Elements render in order, as they appear in the document flow
What is SASS and why do people use it? SASS (Syntactically Awesome Stylesheets) interpretes CSS, and is a a programming language for designers.  
Name one feature of SASS and explain why it is helpful. Sass lets you use features that don't exist in CSS yet like variables, nesting, mixins, inheritance that allows you to keep your code dry and easier to manage.

#JS

Prototypal inheritance is when an object inherits from another object, instead of the typical class.
What is a closure and how/why would you use one?  Function defined in the closure (independent variables) 'remembers' the environment in which it was created in, such as having access to the variables value one level out and nested.  

Deep in space…
var currentEvent = “traveling in space.”;
function robot(){
var currentEvent = “traveling inside the jupiter2.”;
show(currentEvent);
}
function jupiter2() {
show(currentEvent);
robot();
}
jupiter2();
Output:
//for function jupiter2 
"traveling in space."
//for function robot
"traveling inside the jupiter2."

What is an anonymous function? Give a typical usecase for one.

alert((function(x){
	return x*x;
})(10));

Anonymous functions are a form of nested function, in that they allow access to variables in the scope of the containing function (non-local variables). Unlike named nested functions, they cannot be recursive without the assistance of a fixpoint operator (also known as an anonymous fixpoint or anonymous recursion).

Describe the difference between
function Person(){} // creates a new obj type, Person
var person = Person() // assigns a variable an obj 
var person = new Person() // new instance of Person obj

Explain hoisting.

	Function declarations and variable declarations are always moved (“hoisted”) invisibly to the top of their containing scope by the JavaScript interpreter. Function parameters and language-defined names are, obviously, already there. This means that code like this:

	function foo() {
		bar();
		var x = 1;
	}
	is actually interpreted like this:

	function foo() {
		var x;
		bar();
		x = 1;
	}


What is the difference between === and ==?

== will check for equality of values, and in js convert values to different types to see if they are "equal."

=== is explicit and will need the values to also be of the same type to be equal. 
