# CSS

### Selectors

**Elements**
```css
img {
    /* all these styles apply to every <img> */
}
```

**Classes**
`.class-name{}`

**ID**
`#my-element{}`

**Rules**

```css
.my-wrapper .my-class{
    /*will apply only to "my-class" elements that are WITHIN "my-wrapper"*/
}

.class-one, .class-two {
    /*applies to both classes*/
}
```

### Pseudo selectors
```css
.my-class:hover{}
.my-class:focus{}

.my-class:first-child {
    /*only the first child WITHIN my-class*/
}

.my-class:nth-child(3) {
    /*only the 3 child in my-class*/
}

.class-one > .child {
    /*only direct children*/
}

.class-one.class-two {
    /*must have BOTH of these classes*/
}
```

### Units
- `px`
- `%`: percentage of the element's parent
- `vw`/`vh`: percentage viewHeight or viewWidth
- `rem`: ration of the root font-size

### Some basic CSS rules
```css
.class {
    color: blue; /*for text color*/
    background: red; /*background color*/
    width: 10px;
    height: 10px;
    margin: 20px; /*outside the element*/
    padding: 20px; /*inside the element*/
    font-size: 10px;
    font-family: "Avenir", Helvetica; /*Specific one, default if not found*/
}
```

### Position
- `relative`: default for all elements, will be arranged based on their siblings
- `absolute`: removes the element from the "flow" of sibling element. Instead, it becomes positioned based on its 
closest parents that has "relative" positioning. You can use `top`, `bottom`, `left`, `right` to move it around precisely
- Note: either "relative" or "absolute" positioning lets you use the `z-index`

### Display
- `block` (default)
- `inline-block` (stack horizontally)
- `none` (hide)
- `flex` (the King 👑)

### Flexbox
```css
.parent {
    display: flex;
    flex-direction: column; /*or row*/ 
    align-items: center; /*or flex-start, flex-end, space-between, space-around*/
    justify-content: center; 
    flex-flow: column wrap; 
}

.child {
    flex: 1; /*the ratio of how much space to take up*/
}
```
- `align-items`: aligns opposite the direction axis
- `justify-content`: aligns items along direction axis
- `flex-flow`: combines `flex-direction` and `flex-wrap` into one
