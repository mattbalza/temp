# Fixes

## Changes to Custom.css

Add:
```css
.nav-tabs>li.active>a, .nav-tabs>li.active>a:focus, .nav-tabs>li.active>a:hover {
    color: #fff;
    background-color: #337ab7;
    }
    
.nav-tabs>li>a {text-transform:uppercase;}
```

## Changes to Case Assessment screen HTML

Right after:
```html
<h2 class="dashboard-title">Precedents</h2>
```

Replace the table div (included the div itself):
```html
<div class="table-responsive">
..
</div>
```

with the following:

```html
<ul class="nav nav-tabs" role="tablist">
  <li role="presentation" class="active"><a href="#home" aria-controls="all-cases" role="tab" data-toggle="tab">All Cases</a></li>
  <li role="presentation"><a href="#profile" aria-controls="my-cases" role="tab" data-toggle="tab">My Cases</a></li>
</ul>
<div class="tab-content">
  <div role="tabpanel" class="tab-pane fade in active" id="all-cases">
    <div class="table-responsive">
      <table data-sorting="true" data-filtering="true" data-filter-placeholder="Seach" class="table auto table-hover litigation-details table-bordered text-center">
        <thead>
          <tr>
            <th data-type="html">Case</th>
            <th data-type="html" data-filterable="false" data-breakpoints="xs sm" class="head-center">IPO</th>
            <th data-type="html" data-filterable="false" data-breakpoints="xs sm" class="head-center">Class Action</th>
            <th data-type="html" data-filterable="false" data-breakpoints="xs sm" class="head-center">1933 Act</th>
            <th data-type="html" data-filterable="false" data-breakpoints="xs sm" class="head-center">No fraud alleged</th>
            <th data-type="html" data-filterable="false" data-breakpoints="xs sm" class="head-center">Underwiter defs.</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="prec col-fixed-200"><a href="#">In re ShoreTel, Inc. Securities Litigation</a>
            <p class="case-number">3:08-cv-00271 US-Northern District of California</p></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>                  
          </tr>
          <tr>
            <td class="prec col-fixed-200"><a href="#">Petzschke v. Century Aluminum Company, et al.</a>
            <p class="case-number">3:09-cv-01001US-Northern District of California</p></td>
            <td></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
          </tr>
          <tr>
            <td class="prec col-fixed-200"><a href="#">Augenbaum v. Lone Pine Resources Inc., et al.</a>
            <p class="case-number">1:12-cv-04839 US-Southern District of New York</p></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
          </tr>
          <tr>
            <td class="prec col-fixed-200"><a href="#">Singh v. J.P. Morgan Securities LLC, et al.</a>
            <p class="case-number">1:14-cv-05450 US-Southern District of New York</p></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
          </tr>
          <tr>
            <td class="prec col-fixed-200"><a href="#">Plymouth County ReNrement System v. Model N., Inc., et al.</a>
            <p class="case-number">CIV530291 CA-San Mateo County Superior Court</p></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
  <div role="tabpanel" class="tab-pane fade" id="my-cases">
        <div class="table-responsive">
      <table data-sorting="true" data-filtering="true" data-filter-placeholder="Seach" class="table auto table-hover litigation-details table-bordered text-center">
        <thead>
          <tr>
            <th data-type="html">Case</th>
            <th data-type="html" data-filterable="false" data-breakpoints="xs sm" class="head-center">IPO</th>
            <th data-type="html" data-filterable="false" data-breakpoints="xs sm" class="head-center">Class Action</th>
            <th data-type="html" data-filterable="false" data-breakpoints="xs sm" class="head-center">1933 Act</th>
            <th data-type="html" data-filterable="false" data-breakpoints="xs sm" class="head-center">No fraud alleged</th>
            <th data-type="html" data-filterable="false" data-breakpoints="xs sm" class="head-center">Underwiter defs.</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="prec col-fixed-200"><a href="#">In re ShoreTel, Inc. Securities Litigation</a>
            <p class="case-number">3:08-cv-00271 US-Northern District of California</p></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>                  
          </tr>
          <tr>
            <td class="prec col-fixed-200"><a href="#">Petzschke v. Century Aluminum Company, et al.</a>
            <p class="case-number">3:09-cv-01001US-Northern District of California</p></td>
            <td></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
          </tr>
          <tr>
            <td class="prec col-fixed-200"><a href="#">Augenbaum v. Lone Pine Resources Inc., et al.</a>
            <p class="case-number">1:12-cv-04839 US-Southern District of New York</p></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
          </tr>
          <tr>
            <td class="prec col-fixed-200"><a href="#">Singh v. J.P. Morgan Securities LLC, et al.</a>
            <p class="case-number">1:14-cv-05450 US-Southern District of New York</p></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
          </tr>
          <tr>
            <td class="prec col-fixed-200"><a href="#">Plymouth County ReNrement System v. Model N., Inc., et al.</a>
            <p class="case-number">CIV530291 CA-San Mateo County Superior Court</p></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
            <td><i class="glyphicon glyphicon-ok"></i></td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</div>

```
Content for these tables is obviously a placeholder. The first tab, called "All Cases" will show all the precedents, while the second tab "My CaseS" will show only the company's one.

---
