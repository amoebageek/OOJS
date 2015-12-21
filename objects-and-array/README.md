What is difference between objects and array in JavaScript ?
------------------------------------------------------------

 **[ ]**       : Denotes Array
 **{ }**       : Denotes Object


 *`Array is a collection of objects`*
 
 *`Objects/Packages are the collection of properties.`*

 Every time whenever we Google something about the JavaScript or loading page,we find a sentence  "***when DOM get loaded***".
 

What is DOM :
-------------

 *DOM* is as ***DATA OBJECT MODEL*** ,ie all data which is visible on the browser, actually behind the scene it is an object .Browser only understand object.
 
 **Try this:**

 `console.log(window)`   or in ***DOM section*** of your console.

 Since *Browser stores everything in form of **OBJECT*** and *JavaScript only understand the Objects*, that is why we use JavaScript at client side to manipulate the DOM.

Array Declearation:
-------------------

            var a=[];

Object Declaration:
--------------------

			var o={};


Array is a collection of objects :
			
			var a=  [
						{
						  "name" :"object1"
						},
						{
						  "name" :"object2"
						}
			        ];

Object is a collection of properties:

			var o=  {
					  "name" :"object1"
					}





**Note**: `Whole JavaScript data handling is a game of objects.So please be very clear about the array,objects and strings.`

We can define the function as a property of an object.
------------------------------------------------------

*Functions as a property of objects,correct ?*

Yes you are absolutely right,`when a function is defined as a property of an object it is called a method`.

    var myObject={
    				"name"                 :"myname",
    				"location"             :"India",
    				"country_calling_code" :91,
    				"available"            :true,
    				"quality"			   :function(){
    											return 'my quality'
    										}	
    			}	
			

How to treat an object ?
------------------------

Properties of any object is accessible by `. (DOT)` notation.

let me make it more clear and i am sure much more things will strike your mind.


Considering the above object.

***Lets access the properties or an object*** .

	console.log(myObject.name);                    //myname

	console.log(myObject.country_calling_code);   //91

	console.log(myObject.quality());                    //myname

**Lets add the properties**

	myObject.new_property="new property added";
    console.log(myObject);




Now Recall all the past topics that we have already covered or whatever we do in JavaScript ,weather its prototyping or DOM manipulation. We use `. (DOT)` to handle objects and its properties, its clearly mean that whatever we do in JavaScript is actually ***WE PLAY WITH THE OBJECTS,THATS ALL !***



JSON
----

*JavaScript Object Notation*


The name specifies that,it is a notation in such a format,which is treated as an object by JavaScript.

JSON is much common in use today which has reduced the usages of XML for the data exchange or transformation .

	JSON is a light weighted .
	
	Trust me i never weighted the JSON.


So light weighted means it takes less time to get transform on the http calls, for the HTTP `server to server` it is a text,and text is so handy and less time taking for server to server `or server to client` transformation.

	

And when it comes in hand of the JavaScript ,it recognized it as a JSON.

	

Also JSON prefers to use because its a standard format to get recognized by the server side language too.Easy to decode to array for server side language.

	{
		"name"     :"name 1",
		"location" :"India"
	},
	{
		"name"     :"name 2",
		"location" :"Australia"
	}




Points to focus while handling JSON
-----------------------------------

 **If you are treating with one Object,Do not bind it in array**

wrong way
   

    var arr =
       			[
    				{
    					"name"     :"myName",
    					"location" :"India"					
    				}
    			]

Access property
	

    console.log(arr[0].name);
    	console.log(arr[0].location);

Correct Way
			
	var arr =
			{
				"name"     :"myName",
				"location" :"India"					
			}			

Access property
	
	

    console.log(arr.name);
    	console.log(arr.location);


 **Do not treat the boolean or integer as a string.**
	
	wrong way

			[
				{
					"name"         :"myName",
					"calling_code" :"91",
					"availability"  :"true"				
				}
			]

    Correct Way
			
			{
				"name"     :"myName",
				"calling_code" :91,
				"availability"  :true				
			}

 **Follow strict Nomenclature**
	Stay fix on the case of the characters that you are using, recommended always to use the lower case

Wrong Way
	
			
			{
				"Name"                :"myName",
				"callingCode"         :91,
				"availability_status"  :true				
			}

	

Correct Way
			
			{
				"name"                :"myName",
				"calling_code"        :91,
				"availability_status"  :true				
			}

	
		
So whenever you stuck in JavaScript or in jQuery ,do console your object or selected element `[console.log($('.class')) ]`  step by step and then access whatever you need form console using `.(DOT)` .

JSON to String Conversion:

    var J_Son=  {
    				"name"                :"myName",
    				"calling_code"        :91,
    				"availability_status"  :true				
    			}



.

    J_to_S=JSON.stringify(J_Son);
    S_to_J=JSON.parse(J_to_S);
  
    console.log(J_to_S);
	console.log(S_to_J);


----------


*Thanks Put your queries in issue section,ill try to make it more clear for you.*

