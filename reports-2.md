# Fixes

## Changes to Reports page HTML

After:
```html
    var options = {
      width: '100%',
      height: '100%',
```  
Insert:
```html      
      chartArea: {
              left: "20%",
              top: "10%",
              height: "70%",
              width: "75%"
          },
```
You might have to play with the chartArea %s to make it fit nicely in the modal

---
Edit the "title" row inside the "var options"
---

Right after:
```html 
   var chart = new google.visualization.ColumnChart(document.getElementById('chart-container'));
   chart.draw(data, options);
```
Insert: 
```html 
    $('body').one('shown.bs.modal', '#myModal', function(){
      chart.draw(data, options);
    });
```

This re-draws the chart right after the modal is opened, to make it fit nicely in it

---

To change the modal size, edit in:
```html 
    <div class="modal fade bs-example-modal-md" id="myModal" tabindex="-1" role="dialog" aria-labelledby="myModalLabel">
      <div class="modal-dialog modal-md" role="document">
```
the classes "bs-example-modal-md" and the "modal-md"
into: "bs-modal-lg" and "modal-lg"
(lg is for large, while md is for medium size)

---

In the modal body, add a wrap around the "chart-container" div and remove the "center" tags, like this:
```html 
                <div id="visualization_wrap">
                <div id="chart-container"></div>
                </div>
```

---

Remove the modal footer:
```html 
          <div class="modal-footer">
          </div>
```

---

## Changes to CSS

Add the following inside the inline css:

```css
    #visualization_wrap {
    position: relative;
    padding-bottom: 80%;
    height: 0;
    overflow:hidden;
}
  #chart-container  {
      position: absolute;
      top: 0;
      left: 0;
      width:100%;
      height:100%;
  }

```
