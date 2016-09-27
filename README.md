# vue-svg-directive for Vue 2

A Vue.js 2 directive to make [SVG sprites](https://icomoon.io/app/) much simpler to use.

# Setup

```javascript
import svg from 'vue-svg-directive'
// ...
Vue.use(svg, {
  sprites: '/static/sprites.svg', // Path to your SVG sprite
  prefix: 'icon-',  // The prefix all your icons have in your sprite (optional)
  class: 'icon' // This class will be applied to your <svg> elements (optional)
});
```

# Usage

The below will insert an ```<svg />``` within its parent element

```html
<div v-svg="'home'"></div>
```

While the below will just add the appropriate `<use>` into the `<svg>`

```html
<svg v-svg="'home'"></svg>
```

####Important!

**Starting from Vue.js 2.0 directives accept expressions, not literal strings.**

This means that if your sprite is named `home`, you will need to use single quotes inside double quotes to pass them along as a string (`v-svg="'home'"`), otherwise Vue.js will look for a Vue property called `home`. (Which is a perfectly fine usecase too, btw.)
