# Fixes

## Changes to Reports page HTML


Replace the following to the heatmap's thumbnail <a> :
```html
data-toggle="lightbox"
```
into
```html
data-toggle="modal" data-target="#myModal"
```


## Changes to custom.css

Inside media queries, add the following:

### @media only screen and (min-width : 992px) {
```css
  .modal-lg {width: 950px; height: 900px;}
```

### @media only screen and (min-width : 1200px) {
```css
.modal-lg {width: 1100px; height: 900px;}
```

### @media only screen and (min-width : 1300px) {
```css
.modal-lg {width: 1200px; height: 900px;}
```

### @media only screen and (min-width : 1400px) {
```css
 .modal-lg {width: 1250px; height: 900px;}
```

