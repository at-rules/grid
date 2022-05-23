# Grid
**WIP**
A Full customisable grid based off of Foundation (Flex Grid)

## Variables Available

Below are the default variables, as this package uses @at-rules/breakpoints those variables will also be available
```scss
$grid-col-size: 12 !default;
$grid-gutter: 1rem !default;
$grid-max-width: 1140px !default;
```

## Usage
These classes are generated on import using @use. @at-rules/breakpoints is included  for  
responsive classes. 

## Classes

```scss
.grid-container // The grid container 
.grid-container .fluid // 100% width container

.grid-x // The grid row

.grid-margin-x // add a gutter to either side of the row > cell 
.grid-margin-y // adds a gutter above and below the row > cell

.cell // Defines a cell within the grid
```


## Example 
```html
<div class="grid-container">
  <div class="grid-x grid-margin-y grid-margin-x">
    <div class="cell auto"> will fill the remaining space</div>
    <div class="cell mobile-2">2/12 by default or 2/($grid-col-size)</div>
  </div>
  <div class="grid-x">
    <div class="cell mobile-6"> will take half</div>
    <div class="cell mobile-6"> will take half</div>
  </div>
</div>
```

Includes all the breakpoints as prefixes mobile, phablet, tablet and desktop
from 1 to 12/$grid-col-size
```html
<div class="mobile-1 phablet-8 laptop-9 desktop-12"></div>
```

Also include all of the above as offsets
```html
<div class="phablet-offset-2 phablet-9">
  for Phablet up (Large Phones) this column will be offset by 2 and fill 9 leaving 1 column on the right§
</div>
```
