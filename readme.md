# PMG Bootstrap Theme

This is the offical bootstrap theme for PMG's internal tools.

This is a seperate style guide from the PMG Website and Branding Guidelines,
and should not be combined.

Note: You will need to install bootstrap-sass `gem install bootstrap-sass` and you may need to add bootstrap-sass to your gem file `gem 'bootstrap-sass', '~> 3.3.6'`

## How to install

To install, add the following to your ```bower.json``` file

```json
"dependencies": {
  "pmgbootstraptheme": "git://github.com/AgencyPMG/PMGBootstrapTheme.git"
}
```

To install a tagged version, use

```json
"dependencies": {
  "pmgbootstraptheme": "git://github.com/AgencyPMG/PMGBootstrapTheme.git#v1.0.0"
}
```

Include in your compass project
```
require 'bootstrap-sass'
add_import_path "bower_components/pmgbootstraptheme/"
```

```scss
@import "assets/css/variables";
$icon-font-path: "../bootstrap-sass/assets/fonts/bootstrap/"; //This needs to point to the glyphicons fonts
@import "bootstrap";
@import "assets/css/button";
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
