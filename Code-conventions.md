In an effort to keep uniform code throughout the whole program, here are some defined code conventions. 

*Note that I am not a JS-primary developer and as such some of these conventions are carried over from what I'm familiar with in C#. If something is typically done differently in JS applications, please let me know and I'll adjust this page.*

**1. All variables must be declared *before* they are used**

BAD:
```javascript
if (i == 1)
  i += 1;

var i = 0;
```

GOOD:
```javascript
var i = 0;
if (i == 1)
  i += 1;
```

**2. If a variable is to be used after a statement, declare it before the statement.**

BAD:
```javascript
if (true)
  var temp = 5;

temp += 6;
```

GOOD:
```javascript
var temp; //Alternatively, could initialize as "var temp = 0;"
if (true)
  temp = 5;

temp += 6;
```

**3. Use proper spacing in statements**

BAD:
```javascript
for(var i=0;i<5;i++){
```

GOOD:
```javascript
for (var i = 0; i < 5; i++) { //last space before curly bracket is optional
```

**4. Every line that *could* end with a semicolon *should* end with a semicolon. (Similarly, DON'T put in excess semicolons - like after `if`, `for`, or `while` statements)**

**5. Variable and function names should use "camel casing" where the first letter is lower-case** (eg `thisIsAVariableName`)

**6. Proper indentation should be respected. GAS uses multiples of two spaces to differentiate indentation levels**

**7. The bracket convention in GAS-ICS-Sync is the following ("Egyptian brackets"):**
```javascript
if (true){

}
```
**8. `if/elseif/else` statements must follow this form:**
```javascript
if (true){

}
else if (false){

}
else{

}
```
The following is *NOT* allowed:
```javascript
if (true){

} else {

}
```

**9. Curly brackets may be omitted if the "action" is only a single line. For example:**
```javascript
if (true){
  doSomething();
}
```
can be optionally simplified as
```javascript
if (true)
  doSomething();
```
**10. An exception to #7 - if the if statement condition itself takes up multiple lines, curly brackets *MUST* be used. For example:**

This is illegal:
```javascript
if (variable1 == variable2 &&
    variable3 == variable4)
    doSomething();
```

So, for sake of readability, this is what should be done instead:
```javascript
if (variable1 == variable2 &&
    variable3 == variable4){
    doSomething();
}
```