#escape()
*Used to encode a string*


The escapeI() function encodes a string where special characters are encoded. escape() is used to create a working URL when the URL includes special characters other than alphanumeric characters and the following punctuation: `@ * _ . -  /`


Usage:
```javascript 
     encodeURI("This has spaces^among other characters>"); // will output: This%20has%20spaces%5Eamong%20other%3Ccharacters%3E
```

## Syntax

The syntax for escape() is as follows

```
     escape(string);
```
escape() returns a string where some characters are replaced

### Parameters

escape() accepts only one parameter in the form of a string that needs to be encoded.

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

encodeURI() replaces the deprecated escape(). Use decodeURI() or decodeURIComponent() to decode previously encode strings. To encode all characters except alphanumeric and _ . ! ~ * ' ( ), use encodeURIComponent(). 


