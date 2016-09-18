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
<div v-svg="home"></div>
```

While the below will just add the appropriate `<use>` into the `<svg>`

```html
<svg v-svg="home"></svg>
```
