# Fixes


## Changes to JS

Include the following Js file below the jQuery Js:
https://gist.github.com/randylien/5683851#file-smartresize-js

## Changes to Reports page HTML

Add the following inside the head tags:
```html
<script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>
    <script type="text/javascript">
      google.charts.load('upcoming', {'packages':['geochart']});
      google.charts.setOnLoadCallback(drawRegionsMap);
      function drawRegionsMap() {
        var data = new google.visualization.DataTable();
         data.addColumn('string', 'Country');
         data.addColumn('number', 'Value'); 
         data.addRows([[{v:'US-AK',f:'Alaska'},100]]);
         data.addRows([[{v:'US-AL',f:'Alabama'},83]]);
         data.addRows([[{v:'US-AR',f:'Arkansas'},3]]);
         data.addRows([[{v:'US-AZ',f:'Arizona'},82]]);
         data.addRows([[{v:'US-CA',f:'California'},2334]]);
         data.addRows([[{v:'US-CO',f:'Colorado'},207]]);
         data.addRows([[{v:'US-CT',f:'Connecticut'},6]]);
         data.addRows([[{v:'US-DC',f:'District Of Columbia'},18]]);
         data.addRows([[{v:'US-DE',f:'Delaware'},14]]);
         data.addRows([[{v:'US-FL',f:'Florida'},361]]);
         data.addRows([[{v:'US-GA',f:'Georgia'},78]]);
         data.addRows([[{v:'US-HI',f:'Hawaii'},24]]);
         data.addRows([[{v:'US-IA',f:'Iowa'},110]]);
         data.addRows([[{v:'US-ID',f:'Idaho'},64]]);
         data.addRows([[{v:'US-IL',f:'Illinois'},66]]);
         data.addRows([[{v:'US-IN',f:'Indiana'},14]]);
         data.addRows([[{v:'US-KS',f:'Kansas'},2]]);
         data.addRows([[{v:'US-KY',f:'Kentucky'},0]]);
         data.addRows([[{v:'US-LA',f:'Louisiana'},36]]);
         data.addRows([[{v:'US-MA',f:'Massachusetts'},29]]);
         data.addRows([[{v:'US-MD',f:'Maryland'},23]]);
         data.addRows([[{v:'US-ME',f:'Maine'},0]]);
         data.addRows([[{v:'US-MI',f:'Michigan'},20]]);
         data.addRows([[{v:'US-MN',f:'Minnesota'},405]]);
         data.addRows([[{v:'US-MO',f:'Missouri'},29]]);
         data.addRows([[{v:'US-MS',f:'Mississippi'},4]]);
         data.addRows([[{v:'US-MT',f:'Montana'},0]]);
         data.addRows([[{v:'US-NC',f:'North Carolina'},15]]);
         data.addRows([[{v:'US-ND',f:'North Dakota'},4]]);
         data.addRows([[{v:'US-NE',f:'Nebraska'},8]]);
         data.addRows([[{v:'US-NH',f:'New Hampshire'},0]]);
         data.addRows([[{v:'US-NJ',f:'New Jersey'},29]]);
         data.addRows([[{v:'US-NM',f:'New Mexico'},6]]);
         data.addRows([[{v:'US-NV',f:'Nevada'},18]]);
         data.addRows([[{v:'US-NY',f:'New York'},459]]);
         data.addRows([[{v:'US-OH',f:'Ohio'},230]]);
         data.addRows([[{v:'US-OK',f:'Oklahoma'},1143]]);
         data.addRows([[{v:'US-OR',f:'Oregon'},100]]);
         data.addRows([[{v:'US-PA',f:'Pennsylvania'},79]]);
         data.addRows([[{v:'US-PR',f:'Puerto Rico'},0]]);
         data.addRows([[{v:'US-RI',f:'Rhode Island'},13]]);
         data.addRows([[{v:'US-SC',f:'South Carolina'},443]]);
         data.addRows([[{v:'US-SD',f:'South Dakota'},7]]);
         data.addRows([[{v:'US-TN',f:'Tennessee'},8]]);
         data.addRows([[{v:'US-TX',f:'Texas'},164]]);
         data.addRows([[{v:'US-UT',f:'Utah'},23]]);
         data.addRows([[{v:'US-VA',f:'Virginia'},30]]);
         data.addRows([[{v:'US-VI',f:'Virgin Islands'},1]]);
         data.addRows([[{v:'US-VT',f:'Vermont'},0]]);
         data.addRows([[{v:'US-WA',f:'Washington'},394]]);
         data.addRows([[{v:'US-WI',f:'Wisconsin'},104]]);
         data.addRows([[{v:'US-WV',f:'West Virginia'},1]]);
         data.addRows([[{v:'US-WY',f:'Wyoming'},0]]);
        var options = {
          colorAxis:  {minValue: 0, maxValue: 2334,  colors: ['#e9efe9','#188814',]},
          backgroundColor: {fill:'#FFFFFF',stroke:'#FFFFFF' ,strokeWidth:0 },  
          datalessRegionColor: '#f5f5f5',
          defaultColor: '#f5f5f5',
          width: '100%', 
          height: '100%', 
          region: 'US', 
          resolution: 'provinces',
          enableRegionInteractivity: 'true',
          sizeAxis: {minValue: 1, maxValue:1,minSize:10,  maxSize: 10},
          keepAspectRatio: true
        };
        var chart = new google.visualization.GeoChart(document.getElementById('geochart-colors'));
        chart.draw(data, options);

        $(window).smartresize(function () {
    chart.draw(data, options);
});
      };

    </script>
```

Replace the following to the heatmap's thumbnail <a> :
```html
data-toggle="lightbox"
```
into
```html
data-toggle="modal" data-target="#myModal"
```


Also, after:
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
    <div class="modal fade bs-example-modal-md" id="myModal" tabindex="-1" role="dialog" aria-labelledby="myModalLabel">
      <div class="modal-dialog modal-md" role="document">
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

