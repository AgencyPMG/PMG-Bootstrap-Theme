# PMG Bootstrap Theme

This is the offical bootstrap theme for PMG's internal tools.

This is a seperate style guide from the PMG Website and Branding Guidelines,
and should not be combined.

## Installation

```
npm install --save @agencypmg/bootstrap-theme
```

## Usage

### Webpack

You'll need a few loaders:

```
npm install --save-dev sass-loader css-loader \
    resolve-url-loader css-loader
```

Then include `bootstrap-sass` and `@agencypmg/bootstrap-theme` in your
`sass-loader` configuration.


```js
var path = require('path');
var ExtractTextPlugin = require("extract-text-webpack-plugin");

var sassOptions = {
    sourceMap: true,
    outputStyle: 'compressed',
    // setup bootstrap and @agencypmg/bootstrap!
    includePaths: [
        path.join(__dirname, 'node_modules', 'bootstrap-sass', 'assets', 'stylesheets'),
        path.join(__dirname, 'node_modules', '@agencypmg', 'bootstraptheme', 'assets')
    ]
};
var ex = new ExtractTextPlugin({
    filename: 'css/[name].css',
});
var rules = [
    // ...
    {
        test: /\.scss$/,
        loader: ex.extract({
            use: [{
                loader: 'css-loader',
                options: {
                    import: false,
                    url: true
                }
            }, {
                loader: 'resolve-url-loader'
            }, {
                loader: 'sass-loader',
                options: sassOptions,
            }],
            fallback: 'style-loader'
        })
    }
];
```

### Using the Precompiled Version

If you would like the compiled version that has bootstrap already included, you
can use the dist folder.

```html
<link href="node_modules/@agencypmg/bootstrap-theme/dist/app.css" rel="stylesheet" />
```

## HTML Examples

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

 This theme adds a min-height to the content, for this you need to add a class named `main` to the body content wrapping divided. I.e.

```
<header>
    //nav
</header>
<div class="main">
   <div class="container"> //can also be container-fluid
   //content
   </div>
</div>
<footer>
    //copyright notice
</footer>
```

### Footer

The footer should follow this HTML:

```
<footer role="main">
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <p class="copyright">&copy; PMG Worldwide, LLC. All rights reserved.</p>
            </div>
        </div>
    </div>
</footer>
```

## Development

```
npm install
# work work work
```

### Compiling

```
./bin/compile
```
