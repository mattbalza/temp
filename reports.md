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


After
```html
    <div class="container footer">
      <div class="row">
        <div class="col-sm-10 col-md-offset-2">
          <ul class="nav nav-pills">
            <li><a href="#">Terms of Service</a></li>
            <li><a href="#">Privacy</a></li>
            <li><a href="#">About Justly</a></li>
            <li><a class="show-intercom" href="mailto:info@justly.com">Contact Us</a></li>
            <li class="copy">© 2016 Justly Inc. All rights reserved.</li>
          </ul>
        </div>
      </div>
    </div>
 ```

place the following:
```html
<!-- Heatmap Modal -->
    <div class="modal fade bs-example-modal-lg" id="myModal" tabindex="-1" role="dialog" aria-labelledby="myModalLabel">
      <div class="modal-dialog modal-lg" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
            <h4 class="modal-title" id="myModalLabel">JPMC CASE VOLUME BY STATE (2006-2016 YTD)</h4>
          </div>
          <div class="modal-body">
                <center><div id="geochart-colors"></div></center>
          </div>
          <div class="modal-footer">
          </div>
        </div>
      </div>
    </div>
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

