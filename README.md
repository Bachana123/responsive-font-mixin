# responsive-font-mixin
@author Bachana Papunashvili

responsive font @mixin for scss

@example  @include responsive-font(14, 30, 320, 1600);

```scss
//
// responsive font
/// @author Bachana Papunashvili
/// @param min-font-size minimal font size on your page
/// @param max-font-size  maximal font size on your page
/// @param min-width  min width of your page
/// @param max-width  max width of your page
/// @example  @include responsive-font(14, 30, 320, 1600);

@mixin responsive-font($min-font-size, $max-font-size, $min-width: 320, $max-width: 1600) {
  font-size: calc(#{$min-font-size}px + (#{$max-font-size} - #{$min-font-size}) * ((100vw - #{$min-width}px) / (#{$max-width} - #{$min-width})));
}
```
