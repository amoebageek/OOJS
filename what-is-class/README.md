              

Concept Of Class In JS
----------------------

I was so confused with this part,when i get introduced to this.I'll try to discuss things that came to my mind while understanding this part.

Before we proceed ahead please note few points:
*There is no strictly defined syntax to handle the class,syntax may vary as per the languages,what all we have to keep in mind is the basics of objected oriented (oo) language.*

1.Inheritance
2.Encapsulation
3.Abstraction
4.Polymorphism

and also others like ***objects,constructors,functions,instantiations*** etc.
##  What is Class in JS ? 

Lets  make a class file named `MyClass.js`
       		The syntax for defining our class should be.

       		class MyClass Extends someOtherClass{
					
				//play ground

       		}


Now i would like to tell you this is not the way that we should define a class in javascript.
       	Defining a class in javascript is not the same as in other OOP languages.
       	**In JS there is nothing like Class***,*function(not each and every defined function in JS) is treated as a class* or function is defined as a class but yes the keyword class is kept reserve for some future use.   	
       	       	

    Now see how to define a class in javascript;
       	

js>

       	 var myClass=function(params){

       	 			this.parameter=params,	
       	 			this.name="My Name"

       	 }

Yes this way we define a class in javascript.  
    There is so many questions in my mind after reading just the above 6 lines of code.

 -- How this is class ,its just a function.
 --        What is `this` key word
 --        And yes is  this a new style of defining a function ?

Okay Let me try to answer it one by one.

 **---**In JS there is nothing like a class,we follow the basics of the OO and treat a function as a class.
        Yes you are right its a function but we are treating it a class.Can you notice one thing ,if it is a function, it is not returning a value,its just initiating. 
        Since there is no Class in javascript therefore we follow the `prototype` way to handle the inheritance.
        (*prototype is the next topic that i will discuss*).
                    **---** About `this` ,there are types of scopes in javascript,ie. global scope and local scope.
    		Here `this` is a local scope with holds the property locally and made the property available only within the class or function.
   **---** This type of function declaration is known as a `no-name` function (since this function does not have any name) or `function literal`. It protects the function initiation processes from getting polluted.(I will clear the things more in the upcoming topics).

*Now come back to our topic.*
---------------------------

	

    var myClass=function(params){
    
    		this.parameter =params,
    		this.name      ="My Name" 
    /*
    		here this will behave as a global variable,which is available globally wherever this class is inherited. 
    */	
    	}   

 

	var myClass_second=function(){
		this.name="My Name",
		var country=function(){    
			return 'My country';
		}
	} 
	
    /*    
    this country method is a private method is available only inside this class,it cannot be inherited,if we want to do so then we have to call this method inside this class then inherit that property.
     */
**Instantiation of the class**

   
   			var myObj=new myClass("pass-parameters");
   			console.log(myObj);


Now what is inheritance ?
-------------------------

   *In simple words  inheritance is method of getting the properties of one class into other*.

 

How to do inheritance in JS?
---------------------

This is one of the most interesting and important topic in JS.
It took too much time of mine to build and understand a concept of prototyping. 
   Inheritance is done with prototype or prototyping chaining,it is a *`process of inheritance`* in js.

   let see:

   			myClass.prototype.description=function(){

   				return this.name+'  Is inherited';
   			};

   			console.log(myObj);
   			console.log(myObj.description());

   Run the above three sets of snippets in your console,you can see that, we are using the `name` property of `myClass` inside the `description` `method`.
   


 

What are function and what are methods,when shall i call my function a method ?
------------------------------------------------------------------------

   When a function is defined as a property of an object its is classify as a method.
    eg. when you console above object 
			
	console.log(myObj);
	/*
	   in this case you can see the Object as 
	   {
	       parameter="pass-parameters", 
	       name="My Name",
	        description=function()....
	    }
    try to expand the object you can see the constructor and a prototype property in your console.
    
    console.log(myObj.description());


   
   
   *This is all the basics of JS class and inheritance concepts.*
   
   If in case i missed anything or you have some queries feel free to ask any question as a issue ,don't think how logical or much silly it is. :)			






