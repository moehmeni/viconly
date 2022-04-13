# Viconly
Vue.js component wrapper for a free and nice-looking icon pack, [Iconly](https://piqodesign.gumroad.com/l/iconly).
You can see all the styles and names [here](https://amirrezajef.ir/iconly/demo.html)

<img height="320" src="https://beatly-video.s3.ir-thr-at1.arvanstorage.com/viconly_poster.jpg" />

## Installation (add to the project)
```
yarn add viconly
```
Or
```
npm install viconly
```

## Usage
Declare the component globally
```js
import Viconly from 'viconly'

Vue.component('ic', Viconly)
```
then in your `.vue` template
```vue
<ic icon="Home" />
```
or with more customizations
```vue
<ic icon="Home" bold color="green" size="1.5" />
```
_Note:_ the `size` property unit is `rem`


## Nuxt usage
You can use Viconly component globally using Nuxt [plugins directory](https://nuxtjs.org/docs/directory-structure/plugins/).
create a `viconly.js` in `plugins` directory of your Nuxt project (create the directory itself if it doesn't exist) then declare the component and CSS styles in `nuxt.config.js`.

`/plugins/viconly.js`
```js
import Vue from 'vue'
import Viconly from 'viconly'

Vue.component('ic', Viconly)
```
`nuxt.config.js`
```js
plugins: [
  { src: "@/plugins/viconly.js" },
],
css: [
  "viconly/src/iconly/style.css",
  "viconly/src/iconly/bulk-style.css",
],
```
After this you're able to use the `ic` (or whatever you named it) component globally in any of your Nuxt project templates.
