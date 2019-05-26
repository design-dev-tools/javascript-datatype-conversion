
# JavaScript Data Types
> In JavaScript there are 5 different data types that can contain values:
* string
* number
* boolean
* object
* function

> There are 6 types of objects:
* Object
* Date
* Array
* String
* Number
* Boolean

> And 2 data types that cannot contain values:
* null
* undefined

# JavaScript Type Conversion Table

| OriginalValue    |  ConvertedtoNumber | ConvertedtoString | ConvertedtoBoolean |
|------------------|--------------------|-------------------|--------------------|
| false            | 0                  | "false"           | false              |
| true             | 1                  | "true"            | true               |
| 0                | 0                  | "0"               | false              |
| 1                | 1                  | "1"               | true               |
| "0"              | 0                  | "0"               | true               |
| "1"              | 1                  | "1"               | true               |
| NaN              | NaN                | "NaN"             | false              |
| ""               | 0                  | ""                | false              |
| "twenty"         | NaN                | "twenty"          | true               |
| [ ]              | 0                  | ""                | true               |
| [20]             | 20                 | "20"              | true               |
| [10,20]          | NaN                | "10,20"           | true               |
| ["twenty"]       | NaN                | "twenty"          | true               |
| ["ten","twenty"] | NaN                | "ten,twenty"      | true               |
| { }              | NaN                | "[object Object]" | true               |
| null             | 0                  | "null"            | false              |
| undefined        | NaN                | "undefined"       | false              |


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

### Converting JSON string into Object
* A JSON object is a key-value data format that is typically rendered in curly braces. JSON object consist of curly braces ( { } ) at the either ends and have key-value pairs inside the braces. The JSON.parse() method parses a JSON string, constructing the JavaScript value or object described by the string.

```
var txt = '{"key1" : "value1", "key2" : "value2"}';
var obj = JSON.parse(txt);
console.log(obj);
``` 

#### Output:
```
{key1: "value1", key2: "value2"}
```

### Converting string into array of strings

* str.split() function is used to split the given string into array of strings by separating it into substrings using a specified separator provided in the argument.  

```
str.split(separator, limit)
```

###### paramters: This function accepts three parameters as mentioned above and described below:

- str: This parameter holds the string to be split.
- separator: It is optional parameter. It defines the character or the regular expression to use for breaking the string. If not used, the same string is returned (single item array).
- limit: It is optional parameter. It is an integer which specifies the number of splits. All the items after limit are discarded.

```
var fruits = 'apple, orange, pear, banana, raspberry, peach';
var ar = fruits.split(', '); // split string on comma and space
console.log( ar );

var str = "How are you doing today?";
var res = str.split(" "); // split string on space
console.log( res );


var text1 = "text1";
var text2 = "text2";
var arr = [text1, text2];
console.log(arr);


var k = ["1", "2", "3", "4", "5", "6"];
var x = [];
var m = k.map(function(n){
	x = [...x, n];
})
console.log(x);
```

#### Output:
```
["apple", "orange", "pear", "banana", "raspberry", "peach"]
["How", "are", "you", "doing", "today?"]
["text1", "text2"]
["1", "2", "3", "4", "5", "6"]
```

### Converting numbers to strings

* The .toString() method that belongs to the Number.prototype object, takes an integer or floating point number and converts it into a String type. There are multiple ways of calling this method. If a number (base) is passed as a parameter to the .toString() method, the number will be parsed and converted to that base number.

* The String() method creates a primitive String type for the number that is passed to it. The main difference here is that the String object does not do any base conversions like Number.toString() does.

```
var a = 20;

var srt1 = a.toString(); 
console.log("data type: ",typeof(srt1));
console.log("value : ",  srt1);
   
var srt2 = a.toString(2);
console.log("data type: ",typeof(srt2));
console.log("value : ",  srt2);


var srt3 = String(a);    
console.log("data type: ",typeof(srt1));
console.log("value : ",  srt3);

```

#### Output: 
```
data type:  string
value :  20
data type:  string
value :  10100
data type:  string
value :  20
```


### Converting numbers to object

```
var value = 1235;
var obj = {"num" : value};
console.log(obj);

```

#### Output:

```
{num: 1235}
```


