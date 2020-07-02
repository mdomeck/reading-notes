# SMACSS and Responsive Web Design
## Responsive Web Design
- Growth in mobile internet usage, how to build websites suitable for all users... Responsive Web Design RWD
- builing a website suitable to work on every device and every screen size.
- Responsive means to react quickly and positively to any change, while adaptive means to be easily modified for a new purpose or situation, such as change.

### Flexible Layouts
- building a layout of a website with a flexible grid, capable of resizing any width.
- CSS3 has relative length units
1. relative viewport lengths, vw, vh, vmin and vmax
1. flexible grid, target ÷ context = result

### Media Queries
- @media all and (max-width: 1024px) {...}
- @import url(styles.css) all and (max-width: 1024px) {...}

- linking separate style sheet within HTML, `<link href="styles.css" rel="stylesheet" media="all and (max-width: 1024px)">`
- min and mac prefixed can be used
- orientation media feature- landscape or potrait
- mobile first- using style targeted at smaller viewports as the defauly styles, fesigning with the constraints of a mobile user in mind
- `<meta name="viewport" content="width=device-width">`
- The minimum-scale and maximum-scale values determine how small and how large a viewport may be scaled.
### Flexible Media
- to make scalable use max-width 100%
- doesn't work well with iframes but work around...
- embedded element needs to be absolute position within a parent element

## All About Floats
- text flows around images
- Flexbox and Grid are much stronger
- clearing floats
  - The Empty Div Method
  - The Overflow Method
  - The Easy Clearing Method
 


