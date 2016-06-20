# PMG Bootstrap Theme

This is the offical bootstrap theme for PMG's internal tools.

This is a seperate style guide from the PMG Website and Branding Guidelines,
and should not be combined.

Note: You will need to install bootstrap-sass `gem install bootstrap-sass`. You may need to add bootstrap-sass to your server gem file `gem 'bootstrap-sass', '~> 3.3.6'`

## How to install

To install, add the following to your ```bower.json``` file

```json
"dependencies": {
  "pmgbootstraptheme": "git@github.com:AgencyPMG/PMGBootstrapTheme.git"
}
```

To install a tagged version, use

```json
"dependencies": {
  "pmgbootstraptheme": "git@github.com:AgencyPMG/PMGBootstrapTheme.git#v1.3.0"
}
```

Include in your compass project
```
require 'bootstrap-sass'
add_import_path "bower_components/pmgbootstraptheme/"
```

```scss
@import "assets/css/variables";
$icon-font-path: "../bootstrap-sass/assets/fonts/bootstrap/assets"; //This needs to point to the glyphicons fonts
@import "bootstrap";
@import "pmgbootstrap/button";
@import "pmgbootstrap/theme";
```

If you would like the compiled version that has bootstrap already included, you
can use the dist folder
```html
<link href="bower_components/pmgbootstraptheme/dist/css/app.css" rel="stylesheet" />
```


## How to compile

To compile, first run ```bower install```, and then follow the steps below

### Development
```
compass clean
compass watch
```

### Production
```
compass clean
compass compile -e production --force
```

### Navigation

Your navigation should following the bootstrap HTML example: http://getbootstrap.com/components/#navbar

Logo/title should follow mirror this example:

```
<a class="navbar-brand" href="#">
    <span class="logo">
          <img src="{link_to_image}">
      </span>
      {tool_title}
  </a>
 ```

### Body

 This theme adds a min-height to the content, for this you need to add a class named `main` to the body content wrapping divided

### Footer

The footer should follow this HTML:

```
<footer>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <span class="copyright">© PMG Worldwide, LLC. All rights reserved.</span>
            </div>
        </div>
    </div>
</footer>
```
