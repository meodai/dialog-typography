![dialog(typography)](media/logo.png)

# dialog(typography) :book:

[![GitHub version](https://badge.fury.io/gh/meodai%2Fdialog-typography.svg)](https://badge.fury.io/gh/meodai%2Fdialog-typography)
[![npm version](https://badge.fury.io/js/dialog-typography.svg)](https://badge.fury.io/js/dialog-typography)
[![travis build](https://api.travis-ci.org/meodai/dialog-typography.svg?branch=master)](https://travis-ci.org/meodai/dialog-typography)

Provides a central place to manage your typography across multiple breakpoints.

## Installation 💾

```
npm install dialog-typography
```

## Usage ☝️

1. Set up your favorite breakpoint mixin.
   `typo` will call a mixin called `bp($breakpointname)`. So it **important** to
   set up your own breakpoint mixin within a mixin called `bp`.

   For example:

   ```scss
   $breakpoints: (
      desktop: 'min-width: 701px',
      mobile: 'max-wdith: 700px'
   );

   @mixin bp($name) {
     @media (#{map-get($breakpoints, $name)}) {
       @content
     }
   }
   ```

   Or you could also use any [popular breakpoint mixin](https://github.com/inuitcss/tools.responsive/blob/master/_tools.responsive.scss)

   ```scss
   @mixin bp($name)
     @inlcude media-query($name) {
       @content
     }
   }
   ```

2. Import `dialog-typography.scss` after the creation of the `bp` mixin.

    ```scss
    @import 'dialog-typography/dist/dialog-typography';
    ```
    PS: make sure to add `node_modules` to your [import paths](https://github.com/sass/node-sass#includepaths)

3.


## License 👮🏼

Created with ♥ by [meodai](//github.com/meodai). Licensed under the [MIT License](LICENSE).
