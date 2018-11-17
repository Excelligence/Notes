### Putting semi colons in Javascript

The semicolon in JavaScript is used to separate statements, but it can be omitted if the statement is followed by a line break (or there’s only *one* statement in a `{`block`}`)

They are optional

Javascript will automatically insert semi colons for you using ASI(automatic semi colon insertion)

Reasons for using semi colons

+ They are required when two statements are on same line to separate them.
+ If your team is using it, then you can use it for uniformity.



Invalid reason for using semi colon

+ Thinking that it will protect you from ASI errors

```js
Example of one of the errors caused by automatic semi colon insertion

function returnA () {
return 4
}
//4
function returnB () {
    return
     4
    }
//undefined

//Second function is interpreted like this
function returnC () {
    return;
     4;
    }
console.log(returnA(),
returnB(),
returnC(),)
```

Adding semi colons will not help you in the above error. The ASI will insert a semi colon after the return statement.

### Errors causes by not using semi colons

When Looping through an array

```js
//This will give an error
[1,2,3].forEach
```

It can be solved by inserting a semi colon at the beginning 

```js
//Assign array to a variable and use forEach
const arr=[1,2,3]
arr.forEach

```

When using an IIFE

```JS
(function(){
   //function body 
}());
//This will produce error.

// Can be resolved using a semi colon

;(function(){
   //function body 
}());

```

### Situations to avoid semi colons

After a closing curly bracket except for an assignment statement.

```js
// NO semicolons after }:
if  (...) {...} else {...}
for (...) {...}
while (...) {...}

// BUT:
do {...} while (...);

// function statement: 
function (arg) { /*do this*/ } // NO semicolon after }
```

After the round bracket of an if, for, while or switch statement

```js
if (0 === 1); { alert("hi") }

// equivalent to:

if (0 === 1) /*do nothing*/ ;
alert ("hi");
```

#### The less confusing path

+ Assign your arrays to variable and loop through them.
+ Use a semi colon before IIFE.
+ Don't use semi colons other than that.





source:link:https://www.youtube.com/watch?v=gsfbh17Ax9I

SOURCE:link:https://www.youtube.com/watch?v=gsfbh17Ax9I

[Source]: https://news.codecademy.com/your-guide-to-semicolons-in-javascript/