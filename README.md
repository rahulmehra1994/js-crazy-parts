# Equlaity problem
In Js `(0.1 + 0.2) == 0.3` is actually **false** because adding **0.1** and **0.2** gives value **0.30000000000000004** which is not equal to **0.3**

### Use of `==` is dangerous!

```javascript
new Array(2) == ","; //true
```
Above array object is equal to string? 
lets check the string representation  of new Array(2)
```javascript
new Array(2).toString(); // gives ","
```
JavaScript converts the values in the both sides of the `==` operator to strings and compares them. This is one more thing we should be careful for. Instead of `==` it's better to use `===`. Three times equal will check also the type of the operands:



# Even Parentheses position is Important
```javascript
function obj1() {
   return
   {
      name: 'rahul'
   }
}

function obj2() {
   return {
      name: 'rahul'
   }
}

typeof obj1() === typeof obj2(); //it will give false
```

So what do you mean, the object type is not equals to itself or what?! Actually nope, the first function foo returns undefined And yes, that's because we've put the open parentheses on new line. The return statement “does not see” that it has something to return (; are optional in JavaScript) so it returns nothing…The second function, bar, acts as expected because in the same line where is the return statement we have {. The return statement “knows” that there begins declaration of new object literal which it should return so that’s why the returned types are different.

That’s one of the reasons the codding style in JavaScript to points out that it’s good practice to put the opening parentheses on the current line.

# Many syntax for auto run functions

Most common below:
```javascript
(function autoRunFunc() {
    alert("hi");
})();
```
Second way
```javascript
(function autoRunFunc() {
    alert("hi");
}());
```
Third Way
```javascript
var temp = autoRunFunc() {
    alert("hi");
}();
```

Fourth way
```javascript
var temp = autoRunFunc() {
    alert("hi");
}();
```
Fifth way
```javascript
var temp = (autoRunFunc() {
    alert("hi");
}());
```
Last
```javascript
var temp = (autoRunFunc() {
    alert("hi");
}());
```

