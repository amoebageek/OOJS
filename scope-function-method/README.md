What are Functions and Methods ?
------------------------------

According to the concept of functions and methods defined by JavaScript,i believe there are only methods in JavaScript ie. all functions are methods and thus there are only a methods,because JavaScript is a language of browser where each and everything (*DOM*) is in an Object,and all the functions inside an object is a method,but during development phase we keep the functions and methods separate to keep the things clear.

Lets draw a line and try to understand concept of function in JavaScript.
    **Syntax:**
    

        function function_name (parameter1,parameter2){
            
             //play ground of funciton
             return scope;
        }

.
       **eg.**

             
        function myFunc(a,b){

                var sum=a+b;
                return sum;

        } 


Lets focus on the scopes.


        var global_scope;
        function myFunction_1(){
            
            var local_scope;
            global_s_scope;
        }

        function myFunction_2(){
        /*  
            global_scope            //Available
            global_s_scope         //Available
            local_scope           // NA 
        */ 
        }


lets deal with the scopes,here we are considering ***three scopes*** named as 

**`global_scope`** : If the variable is declared outside a function `(global_scope)`that means it is available for all the parallel or nested functions.Thus its known as a global scope.

also if a variable is come into use inside a body of a function `(global_s_scope)`without declaring it anywhere this variable will behave as a global variable and is available for other functions as well.

    Note:It wont work in strict mode.

**`local scope:`** If a variable is declared inside a function it is a local scope ie it can not be shared with the any function outside the function in which it is defined.

**this**
----

  Now lets discuss one more type of scope ie `this`.      
  Take these two sentences :

     1. John Doe is a dummy name,his name is used for templating.

 and
 

    2. John Doe is a dummy name,Jon Doe's name is used for templating.

 

  Think why don't we use 2 sentence,we always use 1.


 Yes its correct,we use `this` to represent local variable within and for,local function.


 

Nested Function
---------------

   *We will be considering this part while understanding the closure*
   ****

    function ParentFunction(){
     this.parent_name = "Parent",
         this.child_method = function(){
                console.log('1.'+ this.parent_name);
                }
         var chlid_function=function(){
        console.log('2.'+this.parent_name);          //available
                console.log('3.'+this.child_method);        //available
                console.log('4.'+this.child_method());
                this.child_scope="Child Scope";
            var child_name="Name Of Child";
                }
             console.log('5.'+chlid_function());
           
           // console.log(child_name)          //NA
           // console.log(chiid_scope)        //NA
       }
    
        ParentFunction();


Compare the above function with the theory of the `functions`,`methods`,`local scope`,`private scope`,*run this in you console* for live execution,also *uncomment the commented* section and try to figure out why you are getting error or undefined.


    JSON Object

      {
            "property" :"name",
            "method"   :define_or_call(){
                function body
        /*
             You can directly define or call a function as in property of an Object,and using a function as a property of an object is called a method.
      */
            } 

      }
