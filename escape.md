#encodeURI()
*escape() is deprecated. Use encodeURI() instead. Used to encode URI instances in a string*

Write a description here. Provide an overview of what the reference entry is, how it's used, it's significance, or how it's commonly used.

The encodeURI() function encodes a string where special characters are encoded into their respective Uniform Resource Identifier (URI). URI can be from one to four escape sequences which represent the [UTF-8](http://www.fileformat.info/info/charset/UTF-8/list.htm) encoding of the character. encodeURI() is used when you want to create a working URL when the URL includes special characters other than the following: 
`alphanumeric characters  - _ . ! ~ * ' ( ) #  $  &  +  /  :  ; ,  =  ?  @`


Usage:
```javascript 
encodeURI("This has spaces^among other characters>"); // will output: This%20has%20spaces%5Eamong%20other%3Ccharacters%3E
```
To use 

## Syntax

The syntax for encodeURI() is as follows

```
     encodeURI(URI);
```

### Parameters

encodeURI() accepts only one parameter in the form of a string, it assumes this string is a complete URI which contains character that need to be encoded.

#### URI

According to Wikipedia  
> a Uniform Resource Identifier (URI) is a string of characters used to identify a resource. Such identification enables interaction with representations of the resource over a network, typically the World Wide Web, using specific protocols.  

Usually a URI is a string that you want to add to a URL but it contains special characters that need encoding in order to be used by the browser.

## Example 1

Here we are using encodeURI() to encode a a string which includes spaces and a `^`. encodeURI() will replace the spaces with `%20` and replace the caret symbol (^) with `%5E`.

```javascript 
var str = encodeURI("a string with spacesand a ^");
 console.log(str); // output = a%20string%20with%20spacesand%20a%20%5E
```

## Example 2 - Complex

Here we are using encodeURI() to encode a directory name which includes spaces. encodeURI() will replace these spaces with `%20` which is the UTF-8 code for a space.

```javascript 
var myDir = encodeURI("some directory with spaces in the name"); //output "some%20directory%20with%20spaces%20in%20the%20name"
var myURL = "http://www.example.com/" + myDir + "/index.html";
console.log(myURL); // outputs: http://www.example.com/some%20directory%20with%20spaces%20in%20the%20name/index.html
```

## Special Notes

encodeURI() replaces the deprecated escape(). 


