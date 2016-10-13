# Fixes

## Changes to Case Assessment screen HTML

Add the following in the footer of the page:

```html
      <script>
    $(document).ready(function() {
      $('#collapseExample').on('shown.bs.collapse', function () {
  //var $target = $('html,body');
  $('html,body').animate({ scrollTop: $("#collapseExample").offset().top + 900 }, 2000);
});
    });
  </script>
```
---
