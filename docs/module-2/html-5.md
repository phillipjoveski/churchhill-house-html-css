# Coding introduction



### Introduction

- Describe some key coding terms 
- Outline the default HTML structure 
- Describe how it works



### Key terms 

- Elements
- Tags
- Attributes



### Key terms: elements

- Define the structure and content of objects within a page
- We want to write semantic HTML 
- Using the most appropriate element for the content 
- E.g. headings, paragraphs, nav, footer, aside



### Key terms: tags

- An element name surrounded by the less-than and greater-than angled brackets
- Most commonly occur in pairs
- They open and close
- Opens like: `<div>`
- Closes like: `</div>`
- What falls between is the content of a tag:

```
<div>............</div>
```



### Key terms: attributes

Attributes are used inside a tag and provide further information about that element

Can only be in the opening tag:  

```
<div class="...">....</div>
```

Must follow the same format:  
attribute name</p>
equals sign</p>
quoted attribute value</p>



### Key terms: attributes

For example:

```
<a href=”http://google.com”>Google</a>
```

or

```
<div id="col">....</div>
```

or 

```
<header><h1 class="main">Site title</h1></header>
```



### Lowercase

- Keep your code in lowercase!



### Those terms again

**Elements**  
The named description of the content

**Tags**  
Element name wrapped in `<` and `>`

**Attributes**  
Provide additional information about an element



### HTML structure

- All HTML documents have the same structure
- It is very specific
- If you put code in the wrong spot then you will have major issues when you validate the code later



### HTML structure
Here is the basic html5 document structure:

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <title></title>
        <meta charset="utf-8">
    </head>
    <body>

    </body>
</html>
```

Let's break it down!



### HTML structure

```
<!DOCTYPE html>
```

The first line of every document must declare what version of HTML you are writing

This is known as the doctype declaration 

In HTML5 it is super short and easy to remember, previously it was much longer



### HTML structure

```
<html>


</html>
```
Following the doctype, the HTML element is declared

It signifies the start of the document

Don’t forget to close it though, it also signifies the end of the document



### HTML structure

```
<head>
    <title></title>
</head>

```
The content within the `<head>` does not actually appear on the page 

This is where you set the title that appears in the browser

Also where you will add the link to your CSS documents later

Don’t forget to close the tag! 



### HTML structure

```
<body>
    <p>Content would go here</p>
</body>
```
All the visible content on the page must go between the `<body>` tags

That means all text, images and layout tags 



### Super simple page

A very simple page would look like this:


```
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>My first web page</title>
        <meta charset="utf-8">
    </head>
    <body>
        <h1>Hello World.</h1>
        <p>This is a basic web page.</p>
    </body>
</html>
```

[See page here](assets/code/basic-html.html).

