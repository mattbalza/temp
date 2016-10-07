# Fixes

## Change to My Account page HTML

This is the new body:
```html
<body class="matters-show pace-done pace-done">

  <nav class="navbar navbar-default">
    <div class="container">
      <div class="col-md-10 col-md-offset-1">
        <!-- Brand and toggle get grouped for better mobile display -->
        <div class="navbar-header">
          <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
            <span class="sr-only">Toggle navigation</span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
          <a class="mobile-logo navbar-brand" href="http://justly-staging.herokuapp.com/">
            <img alt="Justly Logo" src="./Justly_files/logo-blue-8196378ca494b371d68b5a6c4fe15d35183f5ce2b94f8ea6cc104cd4a82a60c2.png">
          </a>
        </div>

        <!-- Collect the nav links, forms, and other content for toggling -->
        <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
          <ul class="nav navbar-nav navbar-left">
            <li class="dropdown">
              <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Legal Timeline Analytics <span class="caret"></span></a>
              <ul class="dropdown-menu">
                <li><a href="#">My Matters</a></li>
                <li role="separator" class="divider"></li>
                <li><a href="#">Matter Details</a></li>
              </ul>
            </li>
            <li><a href="#">Dockets</a></li>
          </ul>
          <ul class="nav navbar-nav navbar-right">
            <li class="dropdown">
              <a href="javascript:void(0)" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">matteo.advisor@justly.com <span class="caret"></span></a>
              <ul class="dropdown-menu">
                <li><a href="#">Profile</a></li>
                <li role="separator" class="divider"></li>
                <li><a href="#" rel="nofollow" data-method="delete">Sign out</a></li>
              </ul>
            </li>
          </ul>
        </div><!-- /.navbar-collapse -->
      </div>
    </div><!-- /.container -->
  </nav>
  <div class="container-fluid"> 
    <div class="row">
      <div class="col-md-6 col-md-offset-3 signin">
        <div class="boxed-myacc col-md-12">
          <div class="row">
          <div class="col-md-8 page-title matter-table">
              <div class="row" id="matter-details">
                <div class="col-md-9 col-md-offset-1 no-left-pad">
                  <h1>My profile</h1>
                </div>
              </div>
            </div>
            <div class="col-md-4 case-assess">
            </div>
          </div>
        </div>
        <div class="boxed-2 col-md-12">
        </div>
        <div class="boxed-3-sign col-md-12">
          <div class="outer-view outer-view-controller-profiles">
            <div class="flash full-column"></div>
            <div class="container full-column controller-profiles">
              <h4>
                <span>Demo Account</span>
              </h4>
              <h4>
                <span>new-demo@justly.com</span>
                <span>&nbsp;</span>
                <span><button class="btn btn-md btn-primary raised" href="/users/edit">change email</button></span>
              </h4>
              <div>
                <span>Joined  </span>
                <span>2016-09-26 18:41:25 UTC</span>
              </div>
              <div>
                <span>Last signed in  </span>
                <span>2016-10-07 04:43:05 UTC</span>
              </div>
              <ul class="myacc-sec">
                <li><button class="btn btn-md btn-primary raised" data-method="get" href="/users/edit">Change password</button></li>
                <li>&nbsp;</li>
                <li>
                  <form class="button_to" method="post" action="/users/sign_out">
                    <input type="hidden" name="_method" value="delete" />
                    <input class="btn-signout" type="submit" value="Sign out" />
                    <input type="hidden" name="authenticity_token" value="FiWnZINPx7XzXfU00jdVMdojLgf0E3tmc+U+yV6YrwRbyFL+gG6tasoN8ujuUQz8mLVx1yaLcw/xX2NUC6YEQw==" />
                  </form>
                </li>
                <li>&nbsp;</li>
                <li>
                  <form class="button_to" method="post" action="/profile">
                    <input type="hidden" name="_method" value="delete" />
                    <input class="close-acc" data-confirm="Are you sure you want to close your account?" type="submit" value="Close my account" />
                    <input type="hidden" name="authenticity_token" value="zjk23i5xp3Rake/9vlE0V63K4iBXHTfE3RZz4Tol18eD1MNELVDNq2PB6CGCN22a71y98IWFP61frC58bxt8gA==" />
                  </form>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="container footer">
    <div class="row">
      <div class="col-sm-10 col-md-offset-2">
        <br/><br/>
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
  <div class="modal">
    <input class="modal-state" id="modal-terminus" type="checkbox">
    <div class="modal-fade-screen">
      <div class="modal-inner">
        <div class="modal-close" for="modal-terminus">
        </div>
        <h1>This is it for now</h1>
        <p class="modal-intro">We're busy classifying over 8 million U.S. lawsuits and will be adding new features constantly. In the meantime please peruse our <a target="_blank" href="http://justly-staging.herokuapp.com/blog">blog</a>.</p>
        <p class="modal-intro"><a class="show-intercom" href="mailto:info@justly.com">Click here to chat.</a> We'd love to know what you'd like to see or do on our site.</p>
      </div>
    </div>
  </div>
</body>
```

## Changes to CSS

Add the following inside custom.css:

```css

.boxed-myacc {
  box-shadow: rgba(0, 0, 0, 0.0470588) 0px -3px 31px 0px, rgba(0, 0, 0, 0.0196078) 0px 6px 20px 0px;
  background: rgb(255, 255, 255);
  padding-right:30px;
  padding-left:55px;
  border-radius: 7px 7px 0 0;
  font-size: 16px;
}

.myacc-sec {
  padding-top:20px;
}

input[type="submit"].btn-signout {
  background-color:#9a9a9a;
}

input[type="submit"].close-acc {
  background-color:rgb(247,247,247);
  color: #9a9a9a;
  padding-left:0;
  font-size:10px;
}
```
