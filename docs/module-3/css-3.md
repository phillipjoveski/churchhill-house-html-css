# CSS 3: Wrappers



## Introduction

- What are they
- How to use them



## Setting the width
When you start building a website, you'll quickly realise that the content always fills the whole, which is rarely what you want. To overcome this, you generally want to add an element where you can define the width and hold everything on the page inside that.  

As [Coyier](https://css-tricks.com/best-way-implement-wrapper-css/) explains:

> Sometimes the first bit of HTML we write in a new document is an element that wraps everything else on the page. The term wrapper is common for that. We give it a class, and that class is responsible for encapsulating all visual elements on the page.



## The technique

The best approach is to add a new `<div>` to the page, below the first `<body>` tag, and closed before the last `</body>` tag. Give it a class, and then set the width.

!!! tip
    You'll notice that I've used a `<div>`. That's because this element has no semantic meaning - it is just a generic container.



<hr>
### HTML


```
<!DOCTYPE html>
<html lang="en">

<head>
    <title>My first web page</title>
    <meta charset="utf-8">
</head>

<body>
    <div class="wrapper">
        <h1>Hello World.</h1>
        <p>This is a basic web page.</p>
    </div>
</body>

</html>


```



### CSS

```
.wrapper {
    width:980px;
    margin-right: auto;
    margin-left:  auto;
    margin-top: 0;
    margin-bottom: 0;
}

```

or shorthand:

```
.wrapper {
    width:980px;
    margin: 0 auto;
}

```

`margin: 0 auto` means that the margin on the top is 0, left and right is auto (the same), so it will automatically position the page in the middle of the browser window. 

