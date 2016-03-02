# smart-media-queries

**[Smart Media Queries](http://smartmediaqueries.com/) v1.1.0**

CSS classes and [Sass](http://sass-lang.com/) mixins for responsive design

[How to use Sass](http://sass-lang.com/guide)  
[Sass Documentation](http://sass-lang.com/documentation/file.SASS_REFERENCE.html)  

**Table of Contents**

* [Installing](#installing)  
* [Browser Support](#browser-support)  
* [CSS Classes](#css-classes)  
    * [Show Classes](#show-classes)  
    * [Hide Classes](#hide-classes)  
    * [CSS Examples](#css-examples)  
* [SCSS Mixins](#scss-mixins)  
    * [Helpers](#helpers)  
    * [Show Mixins](#show-mixins)  
    * [Hide Mixins](#hide-mixins)  
    * [Style Mixins](#style-mixins)  
    * [Custom Breakpoint Mixins](#custom-breakpoint-mixins)  
        * [custom-breakpoint-show](#custom-breakpoint-show-min-max)  
        * [custom-breakpoint-hide](#custom-breakpoint-hide-min-max)  
        * [custom-breakpoint-style](#custom-breakpoint-style-min-max--content-)  
    * [SCSS Examples](#scss-examples)  
* [Frequently Asked Questions](#frequently-asked-questions)  

## Installing

**Download Smart Media Queries**

[Download zip](https://github.com/davidjcastner/smart-media-queries/releases/download/v1.1.0/smart-media-queries.v1.1.0.zip)  
[Download tar.gz](https://github.com/davidjcastner/smart-media-queries/releases/download/v1.1.0/smart-media-queries.v1.1.0.tar.gz)

**Bower Installation:**
```sh
bower install smart-media-queries
```

**For CSS Classes:** Place a copy of either `smart-media-queries.css` or `smart-media-queries.min.css` in your project. Then include the following in your HTML head:

```html
<!-- if using smart-media-queries.css -->
<link rel="stylesheet" href="/path/to/css/file/smart-media-queries.css">
<!-- else -->
<link rel="stylesheet" href="/path/to/css/file/smart-media-queries.min.css">
```

**For SCSS Mixins:** Place a copy of `_smart-media.queries.scss` in your project. Include the following at the top of your SCSS code:

```scss
// if _smart-media-queries.scss is in the same directory
@import "smart-media-queries";
// else
@import "/path/to/file/smart-media-queries";
```

**For SCSS Mixins and CSS classes:** Place a copy of `_smart-media.queries.scss` and `_smart-media.queries-classes.scss` in your project (they should be in the same directory). If you would like to have Smart Media Queries's CSS classes available along with the SCSS mixins, include the following at the top of your SCSS code:

```scss
// automatically includes "smart-media-queries",
// so no need to @import "smart-media-queries";

// if _smart-media-queries-classes.scss is in the same directory
@import "smart-media-queries-classes";
// else
@import "/path/to/file/smart-media-queries-classes";
```

## Browser Support

Supported by any browser that fully supports @media. You can check [w3schools.com](http://www.w3schools.com/cssref/css3_pr_mediaquery.asp) for more information. Below is the first broswer version that fully supports @media.

| Browser | Chrome | Edge  | Internet Explorer | Firefox | Safari | Opera |
| ------- | :----: | :---: | :---------------: | :-----: | :----: | :---: |
| Version | 21     | 12    | 9                 | 3.5     | 4.0    | 9     |

## CSS Classes

Place a copy of either `smart-media-queries.css` or `smart-media-queries.min.css` in your project. Then include the following in your HTML head:

```html
<!-- if using smart-media-queries.css -->
<link rel="stylesheet" href="/path/to/css/file/smart-media-queries.css">
<!-- else -->
<link rel="stylesheet" href="/path/to/css/file/smart-media-queries.min.css">
```

#### Show Classes

Including any of the classes below on an html element will cause it to only show on the media specified.

| Class Name          | Effect                      |
| ------------------- | --------------------------- |
| `show-on-mobile`    | Only displayed on mobile    |
| `show-on-tablet`    | Only displayed on tablet    |
| `show-on-desktop`   | Only displayed on desktop   |
| `show-on-portrait`  | Only displayed on portrait  |
| `show-on-landscape` | Only displayed on landscape |

#### Hide Classes

Including any of the classes below on an html element will cause it to be hidden on the media specified.

| Class Name          | Effect              |
| ------------------- | ------------------- |
| `hide-on-mobile`    | Hidden on mobile    |
| `hide-on-tablet`    | Hidden on tablet    |
| `hide-on-desktop`   | Hidden on desktop   |
| `hide-on-portrait`  | Hidden on portrait  |
| `hide-on-landscape` | Hidden on landscape |

#### CSS Examples

```html
<html>
  <head>
    <link rel="stylesheet" href="/path/to/css/file/smart-media-queries.min.css">
  </head>
  <body>
    <div class="show-on-mobile">This only shows up on mobile</div>
    <div class="show-on-tablet">This only shows up on tablet</div>
    <div class="show-on-desktop">This only shows up on desktop</div>
    <div class="show-on-portrait">This only shows up on portrait</div>
    <div class="show-on-landscape">This only shows up on landscape</div>
    <div class="hide-on-mobile">This is hidden on mobile</div>
    <div class="hide-on-tablet">This is hidden on tablet</div>
    <div class="hide-on-desktop">This is hidden on desktop</div>
    <div class="hide-on-portrait">This is hidden on portrait</div>
    <div class="hide-on-landscape">This is hidden on landscape</div>
    <div class="show-on-mobile show-on-portrait">This only shows up on mobile portrait</div>
  </body>
</html>
```

## SCSS Mixins

To use the SCSS mixins, including the following at the top of your SCSS code:

```scss
// if _smart-media-queries.scss is in the same directory
@import "smart-media-queries";
// else
@import "/path/to/file/smart-media-queries";
```

**(Optional) Including the CSS classes:** If you would like to have Smart Media Queries's CSS classes available along with the SCSS mixins include the following at the top of your SCSS code:

```scss
// automatically includes "smart-media-queries",
// so no need to @import "smart-media-queries";

// if _smart-media-queries-classes.scss is in the same directory
@import "smart-media-queries-classes";
// else
@import "/path/to/file/smart-media-queries-classes";
```

#### Helpers

##### smart-media-queries-hide

Hides the content, equivalent to  `{ display: none !important; }`

```scss
@mixin smart-media-queries-hide;
// hides the content
// how to use:
@include smart-media-queries-hide;
```

#### Show Mixins

Selectors with one of the **show-on** mixins will cause the selector to only be displayed on the specified media.

```scss
@mixin show-on-mobile;
// only displayed on mobile
// how to use:
@include show-on-mobile;


@mixin show-on-tablet;
// only displayed on tablet
// how to use:
@include show-on-tablet;


@mixin show-on-desktop;
// only displayed on desktop
// how to use:
@include show-on-desktop;


@mixin show-on-portrait;
// only displayed on portrait
// how to use:
@include show-on-portrait;


@mixin show-on-landscape;
// only displayed on landscape
// how to use:
@include show-on-landscape;
```

#### Hide Mixins

Selectors with one of the **hide-on** mixins will cause the selector to be hidden on the specified media.

```scss
@mixin hide-on-mobile;
// only displayed on mobile
// how to use:
@include hide-on-mobile;


@mixin hide-on-tablet;
// only displayed on tablet
// how to use:
@include hide-on-tablet;


@mixin hide-on-desktop;
// only displayed on desktop
// how to use:
@include hide-on-desktop;


@mixin hide-on-portrait;
// only displayed on portrait
// how to use:
@include hide-on-portrait;


@mixin hide-on-landscape;
// only displayed on landscape
// how to use:
@include hide-on-landscape;
```

#### Style Mixins

Selectors with one of the **only-style** mixins will cause the selector to be given the style on the specified media. The style can be passed to it through the @content arguement. There is no limit to how much can be passed.

> @content passes a block of styles to the mixin

```scss
@mixin mobile-only-style { @content };
// applies the styling { @content } to mobile
// how to use:
@include mobile-only-style { @content };


@mixin tablet-only-style { @content };
// applies the styling { @content } to tablet
// how to use:
@include tablet-only-style { @content };


@mixin desktop-only-style { @content };
// applies the styling { @content } to desktop
// how to use:
@include desktop-only-style { @content };


@mixin portrait-only-style { @content };
// applies the styling { @content } to portrait
// how to use:
@include portrait-only-style { @content };


@mixin landscape-only-style { @content };
// applies the styling { @content } to landscape
// how to use:
@include landscape-only-style { @content };
```

#### Custom Breakpoint Mixins

##### custom-breakpoint-show ([$min], [$max])

Allows elements to only be displayed for a custom breakpoint. At least one of $min or $max must be defined and both must be a pixel value. The elements will only be displayed if the condition is met: $min <= screen width < $max.

```scss
@mixin custom-breakpoint-show ([$min], [$max]);
// only displays the element if [$min <=] screen width [< $max]

// how to use:
$show-min-breakpoint: $insert_breakpoint_as_pixel_value;
$show-max-breakpoint: $insert_breakpoint_as_pixel_value;
// only displays the element if: $min <= screen width
@include custom-breakpoint-show($min: $show-min-breakpoint);
// only displays the element if: screen width < $max
@include custom-breakpoint-show($max: $show-max-breakpoint);
// only displays the element if: $min <= screen width < $max
@include custom-breakpoint-show($min: $show-min-breakpoint, $max: $show-max-breakpoint);
```

##### custom-breakpoint-hide ([$min], [$max])

Allows elements to be hidden for a custom breakpoint. At least one of $min or $max must be defined and both must be a pixel value. The elements will be hidden if the condition is met: $min <= screen width < $max.

```scss
@mixin custom-breakpoint-hide ([$min], [$max]);
// hides the element if [$min <=] screen width [< $max]

// how to use:
$hide-min-breakpoint: $insert_breakpoint_as_pixel_value;
$hide-max-breakpoint: $insert_breakpoint_as_pixel_value;
// hides the element if: $min <= screen width
@include custom-breakpoint-hide($min: $hide-min-breakpoint);
// hides the element if: screen width < $max
@include custom-breakpoint-hide($max: $hide-max-breakpoint);
// hides the element if: $min <= screen width < $max
@include custom-breakpoint-hide($min: $hide-min-breakpoint, $max: $hide-max-breakpoint);
```

##### custom-breakpoint-style ([$min], [$max]) { @content }

Applies styling to elements for a custom breakpoint. At least one of $min or $max must be defined and both must be a pixel value. The style can be passed to it through the @content arguement. The styling will be applied if the condition is met: $min <= screen width < $max.

> @content passes a block of styles to the mixin

```scss
@mixin custom-breakpoint-style ([$min], [$max]) { @content };
// applies the styling { @content } to the element if [$min <=] screen width [< $max]

// how to use:
$style-min-breakpoint: $insert_breakpoint_as_pixel_value;
$style-max-breakpoint: $insert_breakpoint_as_pixel_value;
// applies the styling to the element if: $min <= screen width
@include custom-breakpoint-style($min: $style-min-breakpoint) { @content };
// applies the styling to the element if: screen width < $max
@include custom-breakpoint-style($max: $style-max-breakpoint) { @content };
// applies the styling to the element if: $min <= screen width < $max
@include custom-breakpoint-style($min: $style-min-breakpoint, $max: $style-max-breakpoint) { @content };
```

#### SCSS Examples

```scss
@import "smart-media-queries";

.mobile-landscape-element {
    // only displays the element on mobile landscape
    @include show-on-mobile;
    @include show-on-landscape;
}

.hide-on-desktop-portrait {
    // hides the element on desktop portrait
    @include hide-on-desktop;
    @include hide-on-portrait;
}

.change-font-color {
    // changes the font color:
    // mobile & portrait: red
    // mobile & landscape: yellow
    // tablet & portrait: green
    // tablet & landscape: cyan
    // desktop & portrait: blue
    // desktop & landscape: violet
    @include mobile-only-style {
        @include portrait-only-style { color: #ff0000; };
        @include landscape-only-style { color: #ffff00; };
    };
    @include tablet-only-style {
        @include portrait-only-style { color: #00ff00; };
        @include landscape-only-style { color: #00ffff; };
    };
    @include desktop-only-style {
        @include portrait-only-style { color: #0000ff; };
        @include landscape-only-style { color: #ff00ff; };
    };
}

$show-min-breakpoint: 600px;
$show-max-breakpoint: 900px;
$hide-min-breakpoint: 900px;
$hide-max-breakpoint: 1100px;
.custom-show-min {
    // only displays the element if: 600px <= screen width
    @include custom-breakpoint-show($min: $show-min-breakpoint);
}
.custom-show-max {
    // only displays the element if: screen width < 900px
    @include custom-breakpoint-show($max: $show-max-breakpoint);
}
.custom-show-min-max {
    // only displays the element if: 600px <= screen width < 900px
    @include custom-breakpoint-show($min: $show-min-breakpoint, $max: $show-max-breakpoint);
}
.custom-hide-min {
    // hides the element if: 900px <= screen width
    @include custom-breakpoint-hide($min: $hide-min-breakpoint);
}
.custom-hide-max {
    // hides the element if: screen width < 1100px
    @include custom-breakpoint-hide($max: $hide-max-breakpoint);
}
.custom-hide-min-max {
    // hides the element if: 900px <= screen width < 1100px
    @include custom-breakpoint-hide($min: $hide-min-breakpoint, $max: $hide-max-breakpoint);
}

$style-breakpoint-one: 800px;
$style-breakpoint-two: 1000px;
.custom-style {
    // changes the font color to red if: screen width < 800px
    @include custom-breakpoint-style($max: $style-breakpoint-one) {
        color: #ff0000;
    };
    // changes the font color to green if: 800px <= screen width < 1000px
    @include custom-breakpoint-style($min: $style-breakpoint-one, $max: $style-breakpoint-two) {
        color: #00ff00;
    };
    // changes the font color to blue if: 1000px <= screen width
    @include custom-breakpoint-style($min: $style-breakpoint-two) {
        color: #0000ff;
    };
}
```

## Frequently Asked Questions

**Question:** How is mobile, tablet, and desktop defined for Smart Media Queries?  
**Answer:** Mobile is defined as the screen width being less than 768px. Tablet is defined as the screen width being greater than or equal to 768px and less than 1024px. Desktop is defined as the screen width being greater than or equal to 1024px.
