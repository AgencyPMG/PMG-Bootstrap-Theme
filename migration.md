# Migration Guide

## Migrating from 3.x to 4.x

To migrate from 3.x to 4.x, there are some changes that need to happen to your
layout file.

### General Layout.

Because of the way the titles work, the general layout has changed slightly.

```html
<html class="sidenav">
    <body>
        <div class="body">
            <nav class="navbar navbar-default">
                ...
            </nav>
            <div class="main-content" role="main">
                <div class="container-fluid title-bar">
                    <ol class="breadcrumb">
                        <li>
                            <a href="/">Home</a>
                        </li>
                    </ol>
                </div>
                <div class="container"> <!-- or container fluid -->
                 content goes here
                </div>
                <footer role="main">
                    ...
                </footer>
            </div>
        </div>
    </body>
</div>
```

### Breadcrumbs

The breadcrumbs now play a more important role in the layout now. They act as the
title of the page. Typically you will want to keep these a bit short.

```html
<ol class="breadcrumb">
    <li>
        <a href="/">Home</a>
    </li>
    <li class="active">
        Current page
    </li>
</ol>
```
