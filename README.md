# advanced-media-queries
CSS classes and Sass mixins useful in responsive design.

**Table of Contents**

* [Installing](#installing)  
* [Browser Support](#browser-support)  
* [CSS Classes](#css-classes)  
    * [Show Classes](#show-classes)  
        * [show-on-mobile](#show-on-mobile)  
        * [show-on-tablet](#show-on-tablet)  
        * [show-on-desktop](#show-on-desktop)  
        * [show-on-portrait](#show-on-portrait)  
        * [show-on-landscape](#show-on-landscape)  
    * [Hide Classes](#hide-classes)  
        * [hide-on-mobile](#hide-on-mobile)  
        * [hide-on-tablet](#hide-on-tablet)  
        * [hide-on-desktop](#hide-on-desktop)  
        * [hide-on-portrait](#hide-on-portrait)  
        * [hide-on-landscape](#hide-on-landscape)  
* [SCSS Mixins](#scss-mixins)  
    * [Display Mixins](#display-mixins)  
        * [show-on-mobile](#mixin-show-on-mobile)  
        * [show-on-tablet](#mixin-show-on-tablet)  
        * [show-on-desktop](#mixin-show-on-desktop)  
        * [show-on-portrait](#mixin-show-on-portrait)  
        * [show-on-landscape](#mixin-show-on-landscape)  
        * [hide-on-mobile](#mixin-hide-on-mobile)  
        * [hide-on-tablet](#mixin-hide-on-tablet)  
        * [hide-on-desktop](#mixin-hide-on-desktop)  
        * [hide-on-portrait](#mixin-hide-on-portrait)  
        * [hide-on-landscape](#mixin-hide-on-landscape)  
    * [Style Mixins](#style-mixins)  
        * [mobile-only-style](#mixin-mobile-only-style)  
        * [tablet-only-style](#mixin-tablet-only-style)  
        * [desktop-only-style](#mixin-desktop-only-style)  
        * [portrait-only-style](#mixin-portrait-only-style)  
        * [landscape-only-style](#mixin-landscape-only-style)  
    * [Custom Breakpoint Mixins](#custom-breakpoint-mixins)  
        * [custom-breakpoint-show](#mixin-custom-breakpoint-show)  
        * [custom-breakpoint-hide](#mixin-custom-breakpoint-hide)  
        * [custom-breakpoint-style](#mixin-custom-breakpoint-style)  

## Installing

```scss
// Advanced Media Queries
@import "advanced-media-queries";

// or Advanced Media Queries with css classes available
// automatically includes the normal package
@import "advanced-media-queries-classes";
```

## Browser Support

## CSS Classes

#### Show Classes

##### show-on-mobile

Elements with this class are only displayed on mobile.

```css
.show-on-mobile
```

##### show-on-tablet

Elements with this class are only displayed on tablet.

```css
.show-on-tablet
```

##### show-on-desktop

Elements with this class are only displayed on desktop.

```css
.show-on-desktop
```

##### show-on-portrait

Elements with this class are only displayed on portrait.

```css
.show-on-portrait
```

##### show-on-landscape

Elements with this class are only displayed on landscape.

```css
.show-on-landscape
```

#### Hide Classes

##### hide-on-mobile

Elements with this class are hidden on mobile.

```css
.hide-on-mobile
```

##### hide-on-tablet

Elements with this class are hidden on tablet.

```css
.hide-on-tablet
```

##### hide-on-desktop

Elements with this class are hidden on desktop.

```css
.hide-on-desktop
```

##### hide-on-portrait

Elements with this class are hidden on portrait.

```css
.hide-on-portrait
```

##### hide-on-landscape

Elements with this class are hidden on landscape.

```css
.hide-on-landscape
```

## SCSS Mixins

(Optional) including css classes into the scss

#### Helpers

##### @mixin advanced-media-queries-hide;

Hides the content, equivalent to  `{ display: none !important; }`

Usage:

```scss
@include advanced-media-queries-hide;
```

#### Display Mixins

##### @mixin show-on-mobile;

Selectors with this mixin included are only displayed on mobile.

Usage:

```scss
@include show-on-mobile;
```

##### @mixin show-on-tablet;

Selectors with this mixin included are only displayed on tablet.

Usage:

```scss
@include show-on-tablet;
```

##### @mixin show-on-desktop;

Selectors with this mixin included are only displayed on desktop.

Usage:

```scss
@include show-on-desktop;
```

##### @mixin show-on-portrait;

Selectors with this mixin included are only displayed on portrait.

Usage:

```scss
@include show-on-portrait;
```

##### @mixin show-on-landscape;

Selectors with this mixin included are only displayed on landscape.

Usage:

```scss
@include show-on-landscape;
```

##### @mixin hide-on-mobile;

Selectors with this mixin included are hidden on mobile.

Usage:

```scss
@include hide-on-mobile;
```

##### @mixin hide-on-tablet;

Selectors with this mixin included are hidden on tablet.

Usage:

```scss
@include hide-on-tablet;
```

##### @mixin hide-on-desktop;

Selectors with this mixin included are hidden on desktop.

Usage:

```scss
@include hide-on-desktop;
```

##### @mixin hide-on-portrait;

Selectors with this mixin included are hidden on portrait.

Usage:

```scss
@include hide-on-portrait;
```

##### @mixin hide-on-landscape;

Selectors with this mixin included are hidden on landscape.

Usage:

```scss
@include hide-on-landscape;
```

#### Style Mixins

##### @mixin mobile-only-style { @content };

Usage:

```scss
@include mobile-only-style { style_for_media_query };
```

##### @mixin tablet-only-style { @content };

Usage:

```scss
@include tablet-only-style { style_for_media_query };
```

##### @mixin desktop-only-style { @content };

Usage:

```scss
@include desktop-only-style { style_for_media_query };
```

##### @mixin portrait-only-style { @content };

Usage:

```scss
@include portrait-only-style { style_for_media_query };
```

##### @mixin landscape-only-style { @content };

Usage:

```scss
@include landscape-only-style { style_for_media_query };
```

#### Custom Breakpoint Mixins

##### @mixin custom-breakpoint-show ([$min], [$max]);

Usage:

```scss
@include custom-breakpoint-show($min: $show-min-breakpoint);
@include custom-breakpoint-show($max: $show-max-breakpoint);
@include custom-breakpoint-show($min: $show-min-breakpoint, $max: $show-max-breakpoint);
```

##### @mixin custom-breakpoint-hide ([$min], [$max]);

Usage:

```scss
@include custom-breakpoint-hide($min: $hide-min-breakpoint);
@include custom-breakpoint-hide($max: $hide-max-breakpoint);
@include custom-breakpoint-hide($min: $hide-min-breakpoint, $max: $hide-max-breakpoint);
```

##### @mixin custom-breakpoint-style ([$min], [$max]) { @content };

Usage:

```scss
@include custom-breakpoint-style($min: $style-min-breakpoint) { style_for_media_query };
@include custom-breakpoint-style($max: $style-max-breakpoint) { style_for_media_query };
@include custom-breakpoint-style($min: $style-min-breakpoint, $max: $style-max-breakpoint) { style_for_media_query };
```