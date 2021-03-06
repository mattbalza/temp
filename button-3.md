
# Export Predecents - button

## Changes to the Case Assessment Page

Under the "My Cases" tab, substitute:
```html
          <center>
           <button class="btn btn-success btn-lg show-prec" type="button" data-toggle="collapse" data-target="#collapseMyCases" aria-expanded="false" aria-controls="collapseMyCases">
                SHOW PRECEDENTS
            </button>
        </center>
     
```

with the following: 

```html
<center>
    <h5>
      <div class="export-contain">
        <a class="btn btn-lg btn-primary btn-export" format="xls"  data-toggle="modal" data-target="#export" href="#">Export All Precedents</a>
      </div>
    </h5>
    <!-- Export Modal -->
    <div class="modal fade" id="export" tabindex="-1" role="dialog" aria-labelledby="myModalLabel">
      <div class="modal-dialog" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
            <h4 class="modal-title" id="myModalLabel">Export all precedents matching the following:</h4>
          </div>
          <div class="modal-body">
            <form action="">
              <input type="checkbox" value="post-ipo"> POST-IPO<br/>
              <input type="checkbox" value="class-action"> CLASS ACTION<br/>
              <input type="checkbox" value="no-fraud-alleged"> NO FRAUD ALLEGED<br/>
              <input type="checkbox" value="1933-act"> 1933 ACT<br/>
              <input type="checkbox" value="underwriter-def"> UNDERWITER DEF.
            </form>
          </div>
          <div class="modal-footer">
            <button type="button" class="btn btn-primary">Export</button>
          </div>
        </div>
      </div>
    </div>
      <button class="btn btn-success btn-lg show-prec" type="button" data-toggle="collapse" data-target="#collapseMyCases" aria-expanded="false" aria-controls="collapseMyCases">
      SHOW TOP PRECEDENTS
  </button>
</center>

```
---

## Changes to custom.css

Add the following 

```css

.btn-export,
.btn-export:hover {
  border:none;
  border-radius: 5px;
}
```
