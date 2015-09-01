# PMG Bootstrap Theme

This is the offical bootstrap theme for PMG's internal tools.

This is a seperate style guide from the PMG Website and Branding Guidelines,
and should not be combined.

## How to install

To install, add the following to your ```bower.json``` file

```json
"dependencies": {
  "pmgbootstraptheme": "https://github.com/AgencyPMG/PMGBootstrapTheme.git"
}
```

To install a tagged version, use

```json
"dependencies": {
  "pmgbootstraptheme": "https://github.com/AgencyPMG/PMGBootstrapTheme.git#1.0.0"
}
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
