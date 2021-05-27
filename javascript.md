# Javascript

### <span style="color:#FFA400">**History:-**</span>
- it started in 1995.
- earlier design mocha live script.
- designed by brendan.  
- donated to ECMA to create a  standard implementation.
- new js based on ECMAscript.
- javascript = java + livescript. 

### <span style="color:#FFA400">**Definition:-**</span>
- javascript  is client-side scripting language.
- it executes in user's browsers.
- interactive web pages.
- Doesn't need any expensive development tools.

### <span style="color:#FFA400">**Tech debt:-**</span>
1.  +:- act as concat and add depending on variable type always do concat when the one of the variable is string type.
2. === :- identify/type check. 
3. null :- missed/ if check for null type returns a type of object.

### <span style="color:#FFA400">**Variable:-**</span>
- in javascript variable like container.
- javascript variable defined using  var  keywords.
- var (ES5) functional scope.
- let, const(ES6)

|  var | let | const |
|----|-----|--------|
| can be redeclared | can't be redeclared |can't be redeclared( non primitive values can updated) |
| can be reinitialized | can be reinitialized | can't  be reinitialized |
| functional scope( local variable overrides the global variable with same name) | Lexical scope( lexical variable overrides the parent lexical or global declaration ) | Lexical scope|
| hoisted | dosen't get  hoisted | doesn't get hoisted |
| ES5 |ES6 |ES6|

### <span style="color:#FFA400">**Categories:-**</span>
1. primitive:-
- string
- number
- boolean 
- undefined
- null
- symbol(ES6)
2.  non-primitive:-
- object:-collection of primitive  or non-primitive data. it holds anything.
- array:- nothing but object but reference  wiith index.

| primitive  | non-primitive |
|----------|----------|
|primitive holds value. | non-primitive always hold reference |
| pass by value | pass by reference |


### <span style="color:#FFA400"> **Conditional evaluation:-**</span>
 
 **Falsy value:-**
- 0
- null
- undefined
- ""
- nan
- false

**Truthy value:-**
- all non-primitive are truthy value.(object & array  is truthy value because they are container & they space allocated.)
- any primitive which is  not falsy is called truthy value.

**Hoisting:-**
- when a declare variable it get declaration at top. 

### <span style="color:#FFA400"> **Lexical and functional scope:-**</span>

**Functional scope:-**
- variable get hoisted.
- start with global scope.
- we can assign variable again in function log.

**Lexical scope:-**
- any block inside in function.
- if  first variable is ES6 it will check in lexical scope then parent lexical scope,functional scope.
- whenever  we have {} we called as lexical code.

### <span style="color:#FFA400"> **Function:-**</span>
- function behaviour  exactly same as variable.
- it act like container.
- hoisting
-  override function
- scope local & global

**Functional hoisting:-**
- functional hoisting only occurs for function declaration,not an function expression.

**Two ways to assign function:-**
>```javascript   
>function doTask(){   //declaration
> console.log("print");   
>
> } 
>```

>```javascript 
 >var doTask2= function(){  // assignment
 >    console.log("print");  
>    
>}
>```
- it can return function
- function is kind of object,object is non-primitive.
- function can assigned  to variable.
- declaration get hoisted.
- assignment can't be hoisted
- because we assigned to variable,variable get hoisted not a function.

### **Properties of function:-**
1. first class citizen:-(it can do anything)
-  function can be assigned to variable.
- function can be return from another function.
- function return  a function.
- declaration and assignment
>``` javascript
>function hello(value){ //declaration =>hosited
>console.log("print" + value); 
>function inner(){
>console.log(value * 2 );
>}return inner;   
>}
> var val=20;
> var result = hello(val);  //assignment
>console.log( result, typeof result);
>```
2. pure function:-
- when same input is pass every time output is same.
- make code more robust and flexiable.
3. higher order function:-
- any function take function as parameter.

**Inner function:-**
- when we defined function in function we can't define outside is called as inner function.

**Anonymous function:-**
- function does not have name is  called as anonymous function.

### **IIFE:-**
- stands for immediately invoked function expression(is also called as self executing function)
>```javascript
> var hello = function(){  //normal fucntion
>console.log("printing hello");    
>}
>hello();
>```

>``` javascript
>(function(){  //IIFE
> console.log("printing hello");   
>})();
>```
**Closure:-**
- nothing but access to private function.

### **Arrow function:-**
- arrow function introduced in ES6.
- it allow us to write shorter function Syntax.

>```javascript
>var b ()=>{
> console.log("arrow");   
>}
>```
### <span style="color:#FFA400">**Constructor & prototype:-**</span>
- object can be converted into a prototype constructor by using new keyword.
- function in javascript converted into prototype ,prototype is an object.
- in javascript we can't find source of object.
- object is child of prototype object.
- object constructor add DOT to used a method 
>```javascript
>person.prototype.getName=function(){
>  return this.name;  
>}
>```

**Built-in constructor:-**
- string
- math
- date
- object
- RegEx
- array
- number 
- boolean
- function

### <span style="color:#FFA400">**Array,Object & string prototype methods:-**</span>
**Array Built-in method:-**
>```javascript
>var names = [" rohan","ron","don","gone"];  //Array
>console.log(names);
>```
1. push(); :- 
- add value at ending of array
>```javascript
>names.push("nate");
>```
2. pop(); :-
- remove last item.
>```javascript
>names.pop();
>```
3. unshift();  :-
- add value at begining of array.
>```javascript
>names.unshift("na");
>```
4.shift(); :-
- remove item in begining of  array.
>```javascript
>names.shift();
>```
5. concat :- 
- is used merge two or more array.
>```javascript
> var new_array = names.concat(name2);
>```
6. map() :-
- create new array with result of calling  a function for every array item.

>```javascript
> var mapfn = function(item,index){
> let value = item +"great";
> return value;    
>}
> var ano_arr = names.map(mapfn);
>console.log( ano_arr);
>```

7. filter() :-
- create an array filled with all array element that pass  a test.
>```javascript
> var filterfn = function(item){
>return !!item;    
>}
>var filterarr = names.filter(filterfn);
>console.log(names, filterarr);
>```

8. indexof() :-
-  searches the array for the specified item, and returns its position.
 >```javascript
> var index = names.indexof("ron");
>console.log(index);
>if(index === -1){
    >console.log("item is not present in array");
    >}else{
>console.log(" item found",+index+position);
    >}
>}
>```
9. includes() :-
- it exact same as index but  output is true or false.
>```javascript
> let present = names.includes("ron");
>console.log(present);
>```
10. join() :-
- joins all the items of an array into a string.
>```javascript
> let value = names.join();
>console.log(value);
>```

**string methods:-**
1. toUpperCase() :-
- converted into upper case.
>```javascript
>console.log(text.toUpperCase());
>```
2. toLowerCase() :-
- converted into lower case.
>```javascript
>console.log(text.toLowerCase());
>```
3. replace() :-
-  replaces only the first match.
>```javascript
>console.log(text.replace("ts","TS"));
>```

4. trim() :-
- remove whitespace from both side of string
 >```javascript
>console.log(text.trim("   helo   " ));
>```
5.  split() :-
- used to split a string into an array of substrings, and returns the new array.
>```javascript
>console.log(text.split("," ));
>```
6. tostring() :-
- converting number into string value.
>```javascript
>console.log(no.tostring(2));
>```
 
 ### <span style="color:#FFA400">**Built-in methods:-**</span>
 1. setTimeout() :-
 - node is runtime environment which run on backend or server.
 - timer api(delay a code specific time.)
 >```javascript
>const timefn = function (){
> console.log("printing after 2 sec") ;
> } console.log("Running 1");
>setTimeout(timefn,2000);
>console.log("Running 2");
>```
- we can use function  directly on 
>```javascript
>setTimeout(function());
>```
2. setInterval() :-
- exactly same work  as setTimeout but setInterval run continuously.
- setInterval keep on looking.
3. clearInterval():-
- it stops Interval.
>```javascript
>console.log("Running 1");
>let counter = 0 ;
>const timer = setInterval(function(){
    >console.log("printing after 5 sec");
    >if (counter > 5 ){
        >clearInterval (timer);
    >}counter ++;
>},3000);
>console.log("Running 2");
>```
4. parseInt() :-
    - it converts into integer number.
>```javascript
> num ="10.1";
> parseInt(num);
>console.log(int num);
>``` 

### <span style="color:#FFA400">**JSON:-**</span>
- it build in java 
- they are two method
1. 
>```javascript
> JSON.Stringify({});
>``` 
- it convert object into JSON string.
2.
>```javascript
> JSON.parse("{}");
>``` 
- it convert string into JSON object.










