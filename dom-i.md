# DOM I
We're gonna cover:
- What DOM is
- How to get DOM elements (read)
- How to manipulate DOM elements (update)
- How to create DOM elements (create)

## What is DOM?

Q: _DOM stands for Document Object Model. If you can give a simple explanation. What is the purpose of the DOM?_

### Document
In a high level observance of the client and server relationship, the document is the medium used for communicating information.
Q: _When talking about concepts, what does it mean high level vs low level?_
Ok so here's the high level of the client-serer model:
1. Browser is the client. We make a request by entering a URL address in the URL bar.
2. The request is made to a remote server where they will respond with a payload. The payload will contain a document.
3. The browser receives the document and displays information.

### Object
Something really important occurs in between the browser receiving the document and displaying the information.
It is construction of many objects known as Node. When the browser reads markup like `html`, `body`, or `div` it will convert them to
objects known as DOM Nodes. It will do this to the entire document, and convert it to a big object. This object is the DOM.

show example of grabbing logo/img from lambda site:
```
document.body.children[1].children[1].children[0].children[0].children[0]
```


### Model
As said, the DOM is an object. This object can be represented in a tree like model.


This can be represented physically in a tree structure:
```
( ) <---- root/ Document
 |
 |
( ) <----- body
  \
   \
    \
    ( )  <---- div
      \
       \
       ( )
       /  \
      /    \
     /      \
   ( )     ( ) <--- img 
```
