What is Closure ?
-----------------


Remember we had marked a note somewhere while learning functions and methods, that we are going to use that parts while learning closure,[what was that part](https://github.com/amoebageek/OOJS/tree/master/scope-function-method#nested-function) ? 
I believe that was a topic of nested function.


lets rewrite the functions here: 

**eg1**

    function ParentFunction(name){

        this.name = name;
    }

    var myObj = new ParentFunction('Jhon');

    console.log(myObj);

**eg2**  

        function ParentFunction(myName){

            var name=myName;

        }


    var myObj = new ParentFunction('Jhon');
    
    console.log(myObj);

*Execute these two examples one by one and find the difference.*

In **eg1** we are declaring *`name as a public`* variable ie. it is available for all the functions in which it gets inherited,thats why on instantiating the constructor function  ParentFunction holds the property name:"Jhon".
    *`output :  ParentFunction { name="Jhon"}`*


Where as in **eg2** ,we had declared *`name as a private`e* variable of a ParentFunction which is not available for any other functions/methods outside the ParentFunction,on instantiating hte ParentFunction we wont find any property.

  *`output :  ParentFunction {}`*


Now what if we want to access the private variables and make it available for others,How we can do so ?
------------------------------------------------------------------------


Here comes the existence of closure,closure is a process of making a private variable accessible for others.

*`If I'll ask for your suggestion how we can do so ?`*

Very first answer would be.

     Write a public method inside a ParentFunction, then call and return this private variable in and from this method. 

Yes you are correct,this is what closure is and how it works.
I am just writing your thoughts into codes.


    function ParentFunction (name){
        
        var  __nam=name;

        this.access_name=function(){
            return __nam;
        }
        }


    var myObj = new ParentFunction('Jhon');
    
    console.log(myObj.access_name());                   //accessing a method of a called function 



This is what a closure is,you can access a private variables by defining a closure.    

    



