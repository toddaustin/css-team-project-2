#unescape()
*Used to decode a string that has hex value to its equivalent symbols.*


Whenever there are special characters other than alphanumeric characters and the following punctuation:  
`@ * _ . -  /`, developers use different functions to prevent cross site scripting and convert the values to a [hexidecimal](https://en.wikipedia.org/wiki/Hexadecimal) value.
 For example the hexidecimal equivalent in html for a space is `%20`.
 At some point, it becomes imperative to convert this value into the format it was received. For such purposes we use ```unescape()```.

```javascript 
     unescape("This%20has%20spaces%5Eamong%20other%20characters%3E"); // will output: 
     This has spaces^among other characters>
```
**Common hexidecimal equivalents:**  

Symbol | Hex
------------ | -------------
space | %20
> | %3E
< | %3C
+ | %2B
= | %3D
% | %25
) | %28
( | %29
# | %23




## Syntax

The syntax for unescape() is as follows

```javascript
     unescape(string);
```
## Returns
unescape() returns a string where hexadecimal values are replaced with the its correct symbols.
This is normally used for display purpose.

### Parameters

#### String
unescape() accepts only one parameter in the form of a string.  
```javascript
     unescape(string);
```

## Special Notes

To decode a string that has been encoded by escape() you would use unescape(). Remember, unescape() has been deprecated as of JavaScript 1.5, you should use decodeURI().
