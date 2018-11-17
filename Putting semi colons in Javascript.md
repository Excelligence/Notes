### Putting semi colons in Javascript

source:link:https://www.youtube.com/watch?v=gsfbh17Ax9I

+ semi colons are optional in js
+ Team themselves decide on the best practices there are no central authority.
+ Uniformity for team -they may decide on having semi colons
+ When switching between SQL and JS it is less jarring when you use semi colons



Invalid reason for using semicolon

​	It will protect from errors related to automatic semi colon insertion. This is wrong.

Example of one of the errors caused by automatic semi colon insertion

```javascript
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

Adding semi colons will save you on lines starting with [ and (

If you put semi colons in front of lines starting with '[' and '(' you will be OK.

---

SOURCE:link:https://www.youtube.com/watch?v=gsfbh17Ax9I

Some solutions for issues with semi colons

+ Use semicolons before ( and [ on the beginning of line

+ Assign array to a variable to avoid this error

  ```javascript
  //This will give an error
  [1,2,3].forEach
  //Assign array to a variable and use forEach
  const arr=[1,2,3]
  arr.forEach
  
  ```

+ For an IIFE use a  semi colon before.

  ```javascript
  ;(function(){
      
  }());
  //or give function proper name and call it.
  ```




---



[Source]: https://news.codecademy.com/your-guide-to-semicolons-in-javascript/

Situations when semi colon are required

The semicolon in JavaScript is used to separate statements, but it can be omitted if the statement is followed by a line break (or there’s only *one* statement in a `{`block`}`)

when two statements are on same line

Avoid semi colons in these situations

+ After a closing curly bracket except for an assignment statement.

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



+ After the round bracket of an if, for, while or switch statement

  ```js
  if (0 === 1); { alert("hi") }
  
  // equivalent to:
  
  if (0 === 1) /*do nothing*/ ;
  alert ("hi");
  ```

  ---




