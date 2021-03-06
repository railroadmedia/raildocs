<style>
    .col {  min-height:50px;border:1px solid #d1d1d1;text-align:center;  }
    h2 {  background:#000;color:#fff;  }
</style>

###### Float Grid

# Rows

The grid uses a row container to house the main contents of a page. There are two containers to choose from.

The default row container is a responsive fixed width container. Capping at ~1000px on desktop widths.
```html
    <div class="row">
    ...
    </div>
```

The fluid row container expands itself to cover the full viewport, regardless of breakpoint
```html
    <div class="row fluid">
    ...
    </div>
```
# Columns

The grid uses a 12 column float layout. (Meaning each column floats to the left and wraps back to the left upon overflowing.)
* It is recommended that columns are a direct child of rows
* Columns can be nested indefinitely, rows cannot
* Grid classes apply to devices with screen widths greater than or equal to the breakpoint sizes, and override grid classes targeted at smaller devices. Therefore, e.g. applying any .md-* class to an element will not only affect its styling on medium devices but also on large devices if a .lg-* class is not present.

Here we have a column that is 2 columns wide on large devices, 4 columns wide on medium devices, and 6 columns wide on small devices
```html
    <div class="col lg-2 md-4 sm-6">
    ...
    </div>
```

Here is a table showing how certain aspects of the grid behave on certain breakpoints

|                 | Small Devices ( ≤ 640px)  | Medium Devices ( ≤ 1024px)   | Large Devices ( > 1024px) |
|-----------------|---------------------------|------------------------------|---------------------------|
| Row Width       | Fluid (100%)              | Fluid (100%)                 | Fixed (1000px)            |
| Class Prefix    | .sm-*                     | .md-*                        | .lg-*                     |
| Gutter Width    | 30px / 3                  | 30px / 2                     | 30px / 2                  |

# Gutters

Columns and rows both have a gutter size of 1.875rem (30px) half of the gutter width is added to each side of the container on desktop and tablets, while one third of the gutter width is added to each side on mobile.

Gutters can be removed from rows and columns by adding the .collapse class to the container

```html
    <div class="row collapse">
    ...
    </div>
    <div class="col lg-2 md-4 sm-6 collapse">
    ...
    </div>
```

<div class="row">
<div class="col sm-4 md-4 lg-3" style="font-size:0;margin-right:15px;">
<img src="https://placehold.it/400x400?text=With+Gutters">
</div>
<div class="col sm-4 md-4 lg-3 collapse" style="font-size:0;">
<img src="https://placehold.it/400x351?text=Without+Gutters">
</div>
</div>

```html
    <div class="row">
        <div class="col sm-6 md-4 lg-3">
            <img src="https://placehold.it/400x400?text=With+Gutters">
        </div>
        <div class="col sm-6 md-4 lg-3 collapse">
            <img src="https://placehold.it/400x400?text=Without+Gutters">
        </div>
    </div>
```

# Example Grid

Here's an example of a grid using classes for all breakpoints. .sm-6 means on smaller devices the columns will be 12/6 or 2 wide. md-4 means on medium devices the columns will be 12/4 or 3 wide. .lg-2 means the columns will be 12/2 or 6 wide.

<div class="row" markdown="1">
<div class="col sm-6 md-4 lg-2">
<span class="show-for-sm-only">sm-6</span>
<span class="show-for-md-only">md-4</span>
<span class="show-for-lg-only">lg-2</span>
</div>
<div class="col sm-6 md-4 lg-2">
<span class="show-for-sm-only">sm-6</span>
<span class="show-for-md-only">md-4</span>
<span class="show-for-lg-only">lg-2</span>
</div>
<div class="col sm-6 md-4 lg-2">
<span class="show-for-sm-only">sm-6</span>
<span class="show-for-md-only">md-4</span>
<span class="show-for-lg-only">lg-2</span>
</div>
<div class="col sm-6 md-4 lg-2">
<span class="show-for-sm-only">sm-6</span>
<span class="show-for-md-only">md-4</span>
<span class="show-for-lg-only">lg-2</span>
</div>
<div class="col sm-6 md-4 lg-2">
<span class="show-for-sm-only">sm-6</span>
<span class="show-for-md-only">md-4</span>
<span class="show-for-lg-only">lg-2</span>
</div>
<div class="col sm-6 md-4 lg-2">
<span class="show-for-sm-only">sm-6</span>
<span class="show-for-md-only">md-4</span>
<span class="show-for-lg-only">lg-2</span>
</div>
<div class="col sm-6 md-4 lg-2">
<span class="show-for-sm-only">sm-6</span>
<span class="show-for-md-only">md-4</span>
<span class="show-for-lg-only">lg-2</span>
</div>
<div class="col sm-6 md-4 lg-2">
<span class="show-for-sm-only">sm-6</span>
<span class="show-for-md-only">md-4</span>
<span class="show-for-lg-only">lg-2</span>
</div>
<div class="col sm-6 md-4 lg-2">
<span class="show-for-sm-only">sm-6</span>
<span class="show-for-md-only">md-4</span>
<span class="show-for-lg-only">lg-2</span>
</div>
<div class="col sm-6 md-4 lg-2">
<span class="show-for-sm-only">sm-6</span>
<span class="show-for-md-only">md-4</span>
<span class="show-for-lg-only">lg-2</span>
</div>
<div class="col sm-6 md-4 lg-2">
<span class="show-for-sm-only">sm-6</span>
<span class="show-for-md-only">md-4</span>
<span class="show-for-lg-only">lg-2</span>
</div>
<div class="col sm-6 md-4 lg-2">
<span class="show-for-sm-only">sm-6</span>
<span class="show-for-md-only">md-4</span>
<span class="show-for-lg-only">lg-2</span>
</div>
</div>

```html
<div class="row">
    <div class="col sm-6 md-4 lg-2">
     ...
    </div>
    <div class="col sm-6 md-4 lg-2">
    ...
    </div>
    <div class="col sm-6 md-4 lg-2">
    ...
    </div>
    <div class="col sm-6 md-4 lg-2">
    ...
    </div>
    <div class="col sm-6 md-4 lg-2">
    ...
    </div>
    <div class="col sm-6 md-4 lg-2">
    ...
    </div>
    <div class="col sm-6 md-4 lg-2">
    ...
    </div>
    <div class="col sm-6 md-4 lg-2">
    ...
    </div>
    <div class="col sm-6 md-4 lg-2">
    ...
    </div>
    <div class="col sm-6 md-4 lg-2">
    ...
    </div>
    <div class="col sm-6 md-4 lg-2">
    ...
    </div>
    <div class="col sm-6 md-4 lg-2">
    ...
    </div>
</div>
```

# Visibility Classes

Using .hide-for-* or .show-for-* classes, you can control the visibility of elements on various breakpoints.

<div class="row">
<div class="col show-for-lg-only">
<strong>Large Only</strong>
</div>
<div class="col show-for-md-only">
<strong>Medium Only</strong>
</div>
<div class="col show-for-sm-only">
<strong>Small Only</strong>
</div>
</div>

```html
<div class="row">
    <div class="col show-for-lg-only">
       Large Only
    </div>
    <div class="col show-for-md-only">
       Medium Only
    </div>
    <div class="col show-for-sm-only">
       Small Only
    </div>
</div>
```

The table below shows visibility of classes at the various breakpoints

|                   | Small Devices ( ≤ 640px)  | Medium Devices ( ≤ 1024px)   | Large Devices ( > 1024px) |
|-------------------|:-------------------------:|:----------------------------:|:-------------------------:|
| .show-for-md      |            ✖             |              ✔               |            ✔              |
| .show-for-lg      |            ✖             |              ✖               |            ✔              |
| .show-for-sm-only |            ✔             |              ✖               |            ✖              |
| .show-for-md-only |            ✖             |              ✔               |            ✖              |
| .show-for-lg-only |            ✖             |              ✖               |            ✔              |
|                   |                          |                               |                           |
| .hide             |            ✖             |              ✖               |            ✖              |
| .hide-for-sm-only |            ✖             |              ✔               |            ✔              |
| .hide-for-md      |            ✔             |              ✖               |            ✖              |
| .hide-for-md-only |            ✖             |              ✖               |            ✔              |
| .hide-for-lg-only |            ✔             |              ✔               |            ✖              |


# Sass Variables

| Variable                           | Usage                                                                    |
|------------------------------------|--------------------------------------------------------------------------|
| **$fixedRowWidth**                 | Controls the size of a fixed row                                         |
| **$gutterWidth**                   | Controls the size of gutters                                             |
| **$tabletWidth**                   | Controls the md breakpoint                                               |
| **$desktopWidth**                  | Controls the lg breakpoint                                               |
| **$largeDesktopWidth**             | Controls a larger breakpoint if needed                                   |


# Mixins

| Mixin                              | Usage                                                                    |
|------------------------------------|--------------------------------------------------------------------------|
| **@include tablet {}**             | Allows control of css at the tablet breakpoint                           |
| **@include desktop {}**            | Allows control of css at the desktop breakpoint                          |
| **@include largeDesktop {}**       | Allows control of css at the large desktop breakpoint                    |
| **@include highDpi {}**            | Allows control of css on high dpi devices (ex. loading a higher res background image for retina devices)|


