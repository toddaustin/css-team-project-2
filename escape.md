#escape()
*Used to encode a string*


The escapeI() function encodes a string where special characters are encoded. escape() is used to create a working URL when the URL includes special characters other than alphanumeric characters and the following punctuation:  
`@ * _ . -  /`

When escape() is used on a string, certain characters are replaced using their [hexidecimal](https://en.wikipedia.org/wiki/Hexadecimal) (or hex as it is often called) equivalent, and prefixed with a `%`. For example the hexidecimal equivalent in html for a space is `%20` and for the greater than symbol (>) the hexidecimal equivalent is `%3E`. 

**Common hexidecimal equivalents:**  

Symbol | Hex
------------ | -------------
space | %20
> | %3E
< | %3C
= | %3D
% | %25
) | %28
( | %29
/# | %23


Usage:
```javascript 
     escape("This has spaces^among other characters>"); // will output: This%20has%20spaces%5Eamong%20other%20characters%3E
```

## Syntax

The syntax for escape() is as follows

```javascript
     escape(string);
```
escape() returns a string where some characters are replaced with the hexidecimal equivalent character code.

### Parameters

#### String
escape() accepts only one parameter in the form of a string.  
```javascript
     escape(string);
```

## Example 1

Here we are using escape() to encode a a string which includes spaces and a `^`. escape() will replace the spaces with `%20` and replace the caret symbol (^) with `%5E`.

```javascript 
     var str = escape("a string with spacesand a ^");
     console.log(str); // output = a%20string%20with%20spacesand%20a%20%5E
```

## Example 2 - Complex

Here we are using escape() to encode a directory name which includes spaces. escape() will replace these spaces with `%20` which is the UTF-8 code for a space.

```javascript 
     var myDir = escape("some directory with spaces in the name"); //output "some%20directory%20with%20spaces%20in%20the%20name"
     var myURL = "http://www.example.com/" + myDir + "/index.html";
     console.log(myURL); // outputs: http://www.example.com/some%20directory%20with%20spaces%20in%20the%20name/index.html
```

## Special Notes

To decode a string that has been encoded by escape() you would use unescape(), however, escape() has been derprecated as of JavaScript 1.3, you should use encodeURI(). Use decodeURI() or decodeURIComponent() to decode previously encode strings. To encode all characters except alphanumeric and _ . ! ~ * ' ( ), use encodeURIComponent(). 


