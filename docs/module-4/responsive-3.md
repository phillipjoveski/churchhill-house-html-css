# Responsive 3: Media Queries



## Introduction

-   Media queries



## Meet Media Queries
Media Queries allow us to build on a flexible framework, and customise styles for different screen types and sizes.

```
@media screen and (max-device-width: 480px) {
    .column {
       float: none;
    } 
}
```
The query contains two components:

A. a media type (`screen`), and

B. the actual query enclosed within parentheses, containing a particular media feature (`max-device-width`) to inspect, followed by the target value (`480px`).

<hr>



## Core ingredients
So what does it take to create a responsive design? 

Speaking purely in terms of front-end layout, it takes three core ingredients:

*   Flexible grids & measurements
*   Flexible images & media
*   Media queries



## Use flexible everything
*   Start with a flexible grid
*   Use relative units (`rem`, `em`, etc) Make your images flexible
*   Make your code simple & robust




### Mobile first?
Consider mobile first. 
That doesn’t mean you need to code that way.

*   You may choose to begin with wide views in order to get a handle on a more complex layout
*   It can be easier to ensure columns and spacing are working on the wider views before working down to a single column
*   Either way, ensure you considered responsive optimisation when you planned your content; screen sizes, connection speeds, device capabilities, fat fingers vs mouse pointers, hover states etc will all affect your coding.

<hr>



## Relative units & Flexible Typesetting
*   `Em`
*   `Rem`
*   `Vw`, `vh` & `vmin`




### Em

`1em` = `16px` in most browsers

You can set the document Root to `16px` using CSS resets or by styling the body

To convert your design’s font-size to `em`, divide the desired target `font-size` (e.g. `24px`) by the container `font-size` (e.g. `16px`).

```
target ÷ context = result
24 ÷ 16 = 1.5
font-size: 1.5em;
```

Or try a convertor, like [PXtoEM](http://pxtoem.com/)


### Em’s are inherited

Whenever you set an em-based `font-size` on any container, you now need to calculate any nested font sizes based on that new `font-size`!

Let’s imagine a new target `font-size` of `11px`:

```
11 ÷ 24 = 0.45833333333333em
font-size: 0.45833333333333em
```

Don’t round that number if you’re trying to stay true to a design! `0.46em` might be neater, but proportionately it wont match.



### Rem
A relative unit, like `em`

But it is always relative to the "root" element rather than using the inherited cascade like em does
This vastly simplifies working with relative units!

One great technique:
**`Px`** at the Root, **`Rem`** for Components, **`Em`** for Text Elements



### Vw, vh & vmin
CSS3 has some new values for sizing things relative to the current viewport size.

`1vw` = `1%` of viewport width  
`1vh` = `1%` of viewport height  
`1vmin` = `1vw` or `1vh`, whichever is smaller  
`1vmax` = `1vw` or `1vh`, whichever is larger  
If the viewport is 40cm wide, `1vw` = 0.4cm  

You can read more about viewport units over at [CSS Tricks](https://css-tricks.com/fun-viewport-units/)


## Flexible Grids
How to get started with flexible grids?  
We can re-use the same formula that let us calculate ems!

Make sure you also look at the CSS Grid Layout on the next [page](../responsive-4/). 

From pixels to percentages

_target ÷ context = result_

![Flexible grids](images/responsive-2-grids.png)

`700 ÷ 1000 = 0.7 = 70%`  
`290 ÷ 1000 = 0.3 = 29%`  
`200 ÷ 700 = 0.285 = 28.5%`

## Flexible images

An image with a specific size can be the bane of your existence when you’re trying to build a responsive website.

While there are many different advanced solutions, there is usually one very basic fix:

```
    img { 
        max-width: 100%; 
        height: auto;
    }
```
This forces any image to adjust to the container width.



### Media queries

As above (so you don't forget):

```
@media screen and (max-device-width: 480px) {
    .column {
       float: none;
    } 
}
```
The query contains two components:

- A. a media type (`screen`), and
- B. the actual query enclosed within parentheses, containing a particular media feature (`max-device-width`) to inspect, followed by the target value (`480px`).



#### Extra reading
*   Read more about [Media Queries](https://css-tricks.com/snippets/css/media-queries-for-standard-devices/)! Media Queries are the kings of Responsive Web Design.
*   Specific ways to write [fancy logic-based media queries](https://css-tricks.com/logic-in-media-queries/) based on different browser types, sizes, etc.




### Media Queries & Breakpoints
*   We used to add media queries for the most popular mobile pixel dimensions. The explosion of new tablets, smartphones & touch devices means that we don’t have a preset list of dimensions anymore!
*   It’s become standard to let media queried breakpoints be defined by content/layout rather than any specific device
*   Whenever things don’t fit or hierarchy breaks, add a media query
*   I use min or max-width most often: this is a good way to keep your queries simple

You can read about why [basing your media queries on specific device sizes is doomed to failure](https://responsivedesign.is/articles/why-you-dont-need-device-specific-breakpoints). 

!!! tip
    To reiterate the point above (I know you'll skim over it), it is better to not set the breakpoints based on the size of the device, because there are far too many devices AND you can't predict the future. 



### Media Queries and the navigation 

As you'd aware, it is very common to hide the navigation behind a hamburger style button when viewing the site on smaller devices. In order to do this, you need to write some more advanced CSS. 

There is a fantastic tutorial explaining how to create a pure CSS hamburger-style menu here: [Responsive, Pure CSS Off-Canvas Hamburger Menu](https://medium.com/@heyoka/responsive-pure-css-off-canvas-hamburger-menu-aebc8d11d793).

There are plenty of other code examples online, e.g. see [this post](https://redstapler.co/10-awesome-css-hamburger-menu/). If you do choose to follow along with one of these tutorials, make sure you reference it appropriately in your reflection. I'll be checking to see that you are able to integrate and adapt the code so it fits in with your work - rather than you just copying and pasting it without actually thinking about what is going on. 



#### Extra reading
* [Defining breakpoints](https://responsivedesign.is/strategy/page-layout/defining-breakpoints/)
* [CSS Tricks: Specificity ](https://css-tricks.com/specifics-on-css-specificity/)



<hr>



### Readings
*   Trent Walton’s blog (anything!): [Fit to scale](http://trentwalton.com/2011/05/10/fit-to-scale/); [Fluid type](http://trentwalton.com/2012/06/19/fluid-type/); [Flexible foundations](http://trentwalton.com/2013/01/07/flexible-foundations/)
*   [Examples of great responsive designs](http://mediaqueri.es/)
*   [A minimal, free, wire framing tool](https://wireframe.cc/)
*   [CSS Tricks on relative units of measurement & how to use them](https://css-tricks.com/rems-ems/)






