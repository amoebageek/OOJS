What is hoisting?
-----------------


So don't get confused between `hoisting` and `hosting`.

Hoisting doesn't mean deploying your JavaScript code on to the server or some `cdn`.


It is not a very wide topic to build a concept,so lets try to understand it.

***`Hoisting in JavaScript is a process in which variable is used first and declare later.`***

Yes thats all about hoisting.  :)


  lets try:

      function hoisting_false(){

      		var x=2;
      		var y=3;

      		var sum=x+y;

      		console.log(sum);     //answer will be 5


      }

      hoisting_false();
      
Now if you ask whats new in this function then,ill say nothing,yes this is your native function,the way you normally use to write.


 Now consider this function 

       function hoisting_true(){

       		var x=2;
       		    y=3;

       		var sum=x+y;
       		console.log(sum); 		 //answer will be 5
       		
       		var y;
       }   


       hoisting_true();

run and check the output of the second code in your browser's console.It will give you the same result ie. 5.

You can see we are initiating and using 'Y' (with value 3), before we declare it.This is what hoisting is.


Since its a very small topic to discuss,so lets do some experiments.

**eg.1**
		
		funcition example_1(){               
			
      		var x=2;
      		var y=3;

      		var sum=x+y;

      		console.log(sum);     //answer will be 5
		}
		example_1();

**eg.2**


        function example_2(){

        	var x=2;

        	var sum=x+y;

        	console.log(sum);            

        	var y=3;
        }
        function example_2();


Now execute eg. 2 and check for the result.

    **NAN** : is that what you get ?

Now check the eg 2 carefully i am not only declaring the value y but also initializing it,after using it in the calculation.
Hoisting is a process of using a variable first and declaring it later.

variable should be initialized with the value before using it.




    function example_2(){
    
            	var x=2;
            		y=3;
            	var sum=x+y;
    
            	console.log(sum);             //answer will be 5
    
            	var y=3;
            }
            function example_2();
