# Matteo Homepage Fixes

in index.html, change

```html
<li><a href="http://www.justly.com/blog/legal-timeline-analytics">About Us</a></li>
```

into 

```html
<li><a href="http://www.justly.com/blog/justlys-billing-guidelines-for-outside-counsel">About Us</a></li>
```

in style.css, change

```css
.facts-box h2 {
    font-weight: 700;
    font-family: 'GT-Walsheim-Pro-Light', sans-serif;
    color: #767D8E;
}
```

into 

```css
.facts-box h2 {
    font-weight: 700;
    font-family: 'GT-Walsheim-Pro-Light', sans-serif;
    color: #767D8E;
    font-size: 25px;
}
```


then change

```css

.section {
    padding-top: 100px;
    padding-bottom: 100px;
}

```

into

```css
.section {
  padding-top: 50px;
  padding-bottom: 50px;
}
```


then change

```css
.home-alt h1 {
  color: #ffffff;
  font-size: 60px;
  margin-bottom: 40px;
  line-height: 54px;
}
```

into 

```css
.home-alt h1 {
  color: #ffffff;
  font-size: 45px;
  margin-bottom: 40px;
  line-height: 54px;
}
```

Add the following code at the bottom of custom.css:

```css
/* ------ /FILTERED TABLE ------ */


@media only screen and (min-width : 400px) {

  .home-alt h1 {font-size:60px;}
  .facts-box h2 {font-size: 30px;}

}
@media only screen and (min-width : 429px) {

}
@media only screen and (min-width : 480px) {

}
@media only screen and (min-width : 768px) {

}
@media only screen and (min-width : 992px) {

}
@media only screen and (min-width : 1200px) {

}

```
