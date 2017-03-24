# VueCkeditor

Vue2.0 Ckeditor component.

## Install

```bash
yarn add vueckeditor
```

## Usage

`VueCkeditor` is using `ckeditor` external.

To start using CKEditor on your website, add a single `<script>` tag to your HTML page:

```html
<script src="//cdn.ckeditor.com/4.6.2/full/ckeditor.js"></script>
```

Or visit the official [CKEditor Download](http://ckeditor.com/download) site. And click the **Download CKEditor** button to get the `.zip` installation file. If you want to try out more editor features, you can download the Full Package instead.

Unpack (extract) the downloaded `.zip` archive to the `ckeditor` directory in the root of your website.

```html
<script src="/path/to/ckeditor.js"></script>
```

## Import VueCkeditor to your page

Single ckeditor

```vue
<template lang="pug">
  #app
    vue-ckeditor(v-model="content")
</template>

<script>
  import VueCkeditor from 'vueckeditor';

  export default {
    components: {
      VueCkeditor
    },
    data() {
      return {
        content: 'Hello World!',
      };
    }
  }
</script>
```

Multi ckeditor

```vue
<template lang="pug">
  #app
    vue-ckeditor(v-model="contentA" id="editor-a")
    vue-ckeditor(v-model="contentB" id="editor-b")
</template>

<script>
  import VueCkeditor from '../src/vueckeditor.vue';

  export default {
    components: {
      VueCkeditor
    },
    data() {
      return {
        contentA: 'Hello World!',
        contentB: 'Hello World!',
      };
    }
  }
</script>
```

## Props

### id

- Type: `String`
- Required: false
- Default: `null`

### height

- Type: `String`
- Required: false
- Default: `300px`

### toolbar

You can find toolbar list of [Toolbar Configurator](http://nightly.ckeditor.com/17-03-19-07-08/full/samples/toolbarconfigurator/index.html#advanced).

- Type: `Array`
- Required: false
- Default:

```js
[
  'Format',
  ['Bold', 'Italic', 'Strike', 'Underline'],
  ['BulletedList', 'NumberedList', 'Blockquote'],
  ['JustifyLeft', 'JustifyCenter', 'JustifyRight', 'JustifyBlock'],
  ['Link', 'Unlink'],
  ['FontSize', 'TextColor'],
  ['Image'],
  ['Undo', 'Redo'],
  ['Source', 'Maximize']
]
```

### language

- Type: `String`
- Required: false
- Default: `'zh-cn'`

### extraplugins

- Type: `String`
- Required: false
- Default: `''`

## TIP!!

Update components value with id:
[https://jsfiddle.net/zhuowenli/okx75cem/](https://jsfiddle.net/zhuowenli/okx75cem/)


## Folder structure

- `src/`: Source files for this component
  - `vueckeditor.vue` The component itself
- `example/`: Example for demonstrating this component
  - `index.js`: Entry for the example
  - `App.vue`: The root component which we use to load this component
- `vbuild.example.js`: Config file for your example
- `vbuild.component.js`: Config file for your component
- `vbuild.unit.js`: Config file for vbuild to run unit tests
- `package.json`: App manifest
- `.editorconfig`: Ensure consistent editor behaivor
- `.gitignore`: Ignore files we don't need to push

## Development

- `yarn example`: Run example in development mode
- `yarn deploy`: Deploy example to gh-pages
- `yarn build:cjs`: Build component in commonjs format
- `yarn build:umd`: Build component in umd format
- `yarn build`: Build component in both format
- `yarn lint`: Run eslint
- `yarn test:unit`: Run unit tests using [vbuild-karma](https://github.com/egoist/vbuild-karma)

Check out your npm scripts, it's using [vbuild](https://github.com/egoist/vbuild) under the hood.

---

Generated by [create-vue-app](https://github.com/egoist/create-vue-app)
