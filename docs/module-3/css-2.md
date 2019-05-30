# CSS 2: Box model and positioning



## Introduction

- What is the box model?
- CSS properties that can be styled

## The Box Model
Basically, everything on the page is a box. You can the define various options about the box: it's position, size, colour etc using CSS. 



## Key Properties

When considering the box model, the key properties are: 

- `display`
- `width`
- `height`
- `margin`
- `padding`
- `border`
- `float` (Only left or right)


### Further reading
*   [Mozilla introduction to the box model](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)
*   [float reference](https://css-tricks.com/almanac/properties/f/float/)


## CSS positioning

To get more precise control, you can also use the `position` property to determine the exact location of the element. 

`position` accepts the values of: `fixed`, `relative`, `absolute` or `sticky`

You then need to add `top`, `right`, `bottom` or `left` to control the exact position. E.g.

```
h1 {
    position: fixed;
    top: 35px; 
    left: 200px;
}
```

### Examples
*   [CSS Tricks reference](https://css-tricks.com/almanac/properties/p/position/)




