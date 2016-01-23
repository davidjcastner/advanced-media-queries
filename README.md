# advanced-media-queries

CSS classes and [Sass mixins](http://sass-lang.com/) useful in responsive design.

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

```scss
// Advanced Media Queries
@import "advanced-media-queries";

// or Advanced Media Queries with css classes available
// automatically includes the normal package
@import "advanced-media-queries-classes";
```

## Browser Support

Supported by any browser that fully supports @media. You can check [w3schools.com](http://www.w3schools.com/cssref/css3_pr_mediaquery.asp) for more information.

| Browser | Chrome | Edge  | Internet Explorer | Firefox | Safari | Opera |
| ------- | :----: | :---: | :---------------: | :-----: | :----: | :---: |
| Version | 21     | 12    | 9                 | 3.5     | 4.0    | 9     |

## CSS Classes

Place a copy of either `advanced-media-queries.css` or `advanced-media-queries.min.css` in your project. Then include the following in your HTML head:

```html
<!-- if using advanced-media-queries.css -->
<link rel="stylesheet" href="/path/to/css/file/advanced-media-queries.css">
<!-- else -->
<link rel="stylesheet" href="/path/to/css/file/advanced-media-queries.min.css">
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

## SCSS Mixins

To use the SCSS mixins, including the following at the top of your SCSS code:

```scss
// if _advanced-media-queries.scss is in the same directory
@import "advanced-media-queries";
// else
@import "/path/to/file/advanced-media-queries";
```

**(Optional) Including the CSS classes:** If you would like to have Advanced Media Queries's CSS classes available along with the SCSS mixins include the following at the top of your SCSS code:

```scss
// automatically includes "advanced-media-queries",
// so no need to @import "advanced-media-queries";

// if _advanced-media-queries-classes.scss is in the same directory
@import "advanced-media-queries-classes";
// else
@import "/path/to/file/advanced-media-queries-classes";
```

#### Helpers

**advanced-media-queries-hide**

Hides the content, equivalent to  `{ display: none !important; }`

```scss
@mixin advanced-media-queries-hide;
// hides the content
// how to use:
@include advanced-media-queries-hide;
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

Selectors with one of the **only-style** mixins will cause the selector to be given the style on the specified media. The style can be passed to it through the @content arguement, there is no limit to how much can be passed.

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
// only displays the element if $min <= screen width
@include custom-breakpoint-show($min: $show-min-breakpoint);
// only displays the element if screen width < $max
@include custom-breakpoint-show($max: $show-max-breakpoint);
// only displays the element if $min <= screen width < $max
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
// hides the element if $min <= screen width
@include custom-breakpoint-hide($min: $hide-min-breakpoint);
// hides the element if screen width < $max
@include custom-breakpoint-hide($max: $hide-max-breakpoint);
// hides the element if $min <= screen width < $max
@include custom-breakpoint-hide($min: $hide-min-breakpoint, $max: $hide-max-breakpoint);
```

##### custom-breakpoint-style ([$min], [$max]) { @content }

Applies styling to elements for a custom breakpoint. At least one of $min or $max must be defined and both must be a pixel value. The will be applied if the condition is met: $min <= screen width < $max.

> @content passes a block of styles to the mixin

```scss
@mixin custom-breakpoint-style ([$min], [$max]) { @content };
// applies the styling { @content } to the element if [$min <=] screen width [< $max]

// how to use:
$style-min-breakpoint: $insert_breakpoint_as_pixel_value;
$style-max-breakpoint: $insert_breakpoint_as_pixel_value;
// applies the styling to the element if $min <= screen width
@include custom-breakpoint-style($min: $style-min-breakpoint) { @content };
// applies the styling to the element if screen width < $max
@include custom-breakpoint-style($max: $style-max-breakpoint) { @content };
// applies the styling to the element if $min <= screen width < $max
@include custom-breakpoint-style($min: $style-min-breakpoint, $max: $style-max-breakpoint) { @content };
```

#### SCSS Examples

## Frequently Asked Questions

**Question:** How is mobile, tablet, and desktop defined for Advanced Media Queries?  
**Answer:** Mobile is defined as the screen width being less than 768px. Tablet is defined as the screen width being greater than or equal to 768px and less than 1024px. Desktop is defined as the screen width being greater than or equal to 1024px.