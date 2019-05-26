# javascript-datatype-conversion


### Converting strings to numbers

* The parseInt() method converts a string into an integer (a whole number). It accepts two arguments. The first argument is the string to convert. The second argument is called the radix. This is the base number used in mathematical systems. For our use, it should always be 10.
		console.log("using parseInt()");
    
* The parseFloat() method converts a string into a point number (a number with decimal points). You can even pass in strings with random text in them.
		console.log("using parseFloat()");
    
* The Number() method converts a string to a number. Sometimes it’s an integer. Other times it’s a point number. And if you pass in a string with random text in it, you’ll get NaN, an acronym for “Not a Number.”
		console.log("using Number()");  

```
var a = "Hello";
var b = "1234";
var c = "1234.3456";
var d = "1234vgvh";

console.log("using parseInt(): ", parseInt(a, 10), parseInt(b, 10), parseInt(c, 10), parseInt(d, 10));
console.log("using parseFloat(): ", parseFloat(a), parseFloat(b), parseFloat(c), parseFloat(d));
console.log("using Number(): ", Number(a), Number(b), Number(c), Number(d));
    
```

#### Output 
```
using parseInt():  NaN 1234 1234 1234
using parseFloat():  NaN 1234 1234.3456 1234
using Number():  NaN 1234 1234.3456 NaN
```
