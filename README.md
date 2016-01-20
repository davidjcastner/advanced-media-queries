# advanced-media-queries
CSS classes and Sass mixins useful in responsive design.

**Table of Contents**

* [CSS Classes](#css-classes)  
    * [Show Classes](#show-classes)  
    * [Hide Classes](#hide-classes)  
* [SCSS Mixins](#scss-mixins)  
    * [Display Mixins](#display-mixins)  
        * [show-on-mobile](#show-on-mobile)  
        * [show-on-tablet](#show-on-tablet)  
        * [show-on-desktop](#show-on-desktop)  
        * [show-on-portrait](#show-on-portrait)  
        * [show-on-landscape](#show-on-landscape)  
        * [hide-on-mobile](#hide-on-mobile)  
        * [hide-on-tablet](#hide-on-tablet)  
        * [hide-on-desktop](#hide-on-desktop)  
        * [hide-on-portrait](#hide-on-portrait)  
        * [hide-on-landscape](#hide-on-landscape)  
    * [Style Mixins](#style-mixins)  
        * [mobile-only-style](#mobile-only-style)  
        * [tablet-only-style](#tablet-only-style)  
        * [desktop-only-style](#desktop-only-style)  
        * [portrait-only-style](#portrait-only-style)  
        * [landscape-only-style](#landscape-only-style)  
    * [Custom Breakpoint Mixins](#custom-breakpoint-mixins)  
        * [custom-breakpoint-show](#custom-breakpoint-show)  
        * [custom-breakpoint-hide](#custom-breakpoint-hide)  
        * [custom-breakpoint-style](#custom-breakpoint-style)  

## CSS Classes

#### Show Classes

#### Hide Classes

## SCSS Mixins

(Optional) including css classes into the scss

#### Helpers

##### advanced-media-queries-hide

Hides the content, equivalent to  `{ display: none !important; }`

Usage:

```scss
@include advanced-media-queries-hide;
```

#### Display Mixins

##### show-on-mobile

Usage:

```scss
@include show-on-mobile;
```

##### show-on-tablet

Usage:

```scss
@include show-on-tablet;
```

##### show-on-desktop

Usage:

```scss
@include show-on-desktop;
```

##### show-on-portrait

Usage:

```scss
@include show-on-portrait;
```

##### show-on-landscape

Usage:

```scss
@include show-on-landscape;
```

##### hide-on-mobile

Usage:

```scss
@include hide-on-mobile;
```

##### hide-on-tablet

Usage:

```scss
@include hide-on-tablet;
```

##### hide-on-desktop

Usage:

```scss
@include hide-on-desktop;
```

##### hide-on-portrait

Usage:

```scss
@include hide-on-portrait;
```

##### hide-on-landscape

Usage:

```scss
@include hide-on-landscape;
```

#### Style Mixins

##### mobile-only-style

Usage:

```scss
@include mobile-only-style { style_for_media_query };
```

##### tablet-only-style

Usage:

```scss
@include tablet-only-style { style_for_media_query };
```

##### desktop-only-style

Usage:

```scss
@include desktop-only-style { style_for_media_query };
```

##### portrait-only-style

Usage:

```scss
@include portrait-only-style { style_for_media_query };
```

##### landscape-only-style

Usage:

```scss
@include landscape-only-style { style_for_media_query };
```

#### Custom Breakpoint Mixins

##### custom-breakpoint-show

Usage:

```scss
@include custom-breakpoint-show($min: $show-min-breakpoint);
@include custom-breakpoint-show($max: $show-max-breakpoint);
@include custom-breakpoint-show($min: $show-min-breakpoint, $max: $show-max-breakpoint);
```

##### custom-breakpoint-hide

Usage:

```scss
@include custom-breakpoint-hide($min: $hide-min-breakpoint);
@include custom-breakpoint-hide($max: $hide-max-breakpoint);
@include custom-breakpoint-hide($min: $hide-min-breakpoint, $max: $hide-max-breakpoint);
```

##### custom-breakpoint-style

Usage:

```scss
@include custom-breakpoint-style($min: $style-min-breakpoint) { style_for_media_query };
@include custom-breakpoint-style($max: $style-max-breakpoint) { style_for_media_query };
@include custom-breakpoint-style($min: $style-min-breakpoint, $max: $style-max-breakpoint) { style_for_media_query };
```