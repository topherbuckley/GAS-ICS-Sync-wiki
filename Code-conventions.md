In an effort to keep uniform code throughout the whole program, here are some defined code conventions. 

*Note that I am not a JS-primary developer and as such some of these conventions are carried over from what I'm familiar with in C#. If something is typically done differently in JS applications, please let me know and I'll adjust this page.*

**1. All variables must be declared *before* they are used**

**2. Every line that *could* end with a semicolon *should* end with a semicolon**

**3. Variable and function names should use "camel casing" where the first letter is lower-case** (eg `thisIsAVariableName`)

**4. Proper indentation should be respected. GAS uses multiples of two spaces to differentiate indentation levels**

**5. The bracket convention in GAS-ICS-Sync is the following (I don't know if there's a name for this):**
```
if (true){

}
```
**6. `if-elseif-else` statements must follow this form:**
```
if (true){

}
else if (false){

}
else{

}
```
The following is *NOT* allowed:
```
if (true){

} else {

}
```

**7. Curly brackets may be omitted if the "action" is only a single line. For example:**
```
if (true){
  doSomething();
}
```
can be optionally simplified as
```
if (true)
  doSomething();
```
**8. An exception to #7 - if the if statement condition itself takes up multiple lines, curly brackets *MUST* be used. For example:**

This is illegal:
```
if (variable1 == variable2 &&
    variable3 == variable4)
    doSomething();
```
So, for sake of readability, this is what should be done instead:
 ```
if (variable1 == variable2 &&
    variable3 == variable4){
    doSomething();
}
```