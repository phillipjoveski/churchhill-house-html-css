# Responsive 4: Grid Systems 



## Introduction

-  Grid Systems 



## CSS Grid Layout

You can use CSS grids to create complex responsive layouts whilst still ensuring the underlying page structure remains structured. Support was first added to Chrome, Firefox and Safari in March 2017. 

> Grid Layout lets us properly separate the order of elements in the source from their visual presentation. As a designer this means you are free to change the location of page elements as is best for your layout at different breakpoints and not need to compromise a sensible structured document for your responsive design.

*   CSS Tricks has a great [guide to CSS Grid Layout](https://css-tricks.com/snippets/css/complete-guide-grid/)
*   [Realizing common layouts using CSS Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout/Realizing_common_layouts_using_CSS_Grid_Layout) from Mozilla MDN



## Flex-box

> The Flexbox Layout (Flexible Box) module (a W3C Candidate Recommendation as of October 2017) aims at providing a more efficient way to lay out, align and distribute space among items in a container, even when their size is unknown and/or dynamic (thus the word "flex").

Read the CSS Tricks [Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) for a very detailed introduction.



### Grid or Flexbox

You'll find lots of information online about this topic, but worth reading this great summary:

>Flexbox is for one-dimensional layouts - anything that needs to be
laid out in a straight line (or in a broken line, which would be a
single straight line if they were joined back together).  
Grid is for two-dimensional layouts.  It can be used as a low-powered
flexbox substitute (we're trying to make sure that a single-column/row
grid acts very similar to a flexbox), but that's not using its full
power.  

>    Flexbox is appropriate for many layouts, and a lot of "page component"
elements, as most of them are fundamentally linear.  Grid is
appropriate for overall page layout, and for complicated page
components which aren't linear in their design.  
The two can be composed arbitrarily, so once they're both widely
supported, I believe most pages will be composed of an outer grid for
the overall layout, a mix of nested flexboxes and grid for the
components of the page, and finally block/inline/table layout at the
"leaves" of the page, where the text and content live.

[CSS-grid-layout - Relationship with Flexbox](http://lists.w3.org/Archives/Public/www-style/2013May/0114.html)

