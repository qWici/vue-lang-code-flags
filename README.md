# Flags by language codes

Vue component which shows the flag of the country from which the language comes from

<p align="center">
  <img src="https://img.shields.io/badge/vue%202.x-compatible-green.svg" alt="Vue.js 2 compatible">
  <a href="https://www.npmjs.com/package/vue-lang-code-flags"><img src="https://img.shields.io/badge/npm-1.0.8-blue.svg" alt="Version"></a>
  <a href="https://www.npmjs.com/package/vue-lang-code-flags"><img src="https://img.shields.io/badge/license-MIT-green.svg" alt="License"></a>
</p>

## How to install

Get the package from NPM:

```bash
npm install vue-lang-code-flags --save
or
yarn add vue-lang-code-flags --save
```

## How to use

Register `LangFlag` component in your app. You can use two approaches:

- in `main.js` you can mount it as a global Vue component:

```js
import Vue from 'vue';
import LangFlag from 'vue-lang-code-flags';

Vue.component('lang-flag', LangFlag);
```

- in a specific component (e.g.: `Component.vue`):

```js
import LangFlag from 'vue-lang-code-flags';

new Vue({
  components: {
    LangFlag,
  },
});
```

Then, after the proper mounting, in your template you can call it like this:

```html
<lang-flag iso="en" />
<lang-flag iso="ja" squared="false" />
<lang-flag iso="zh" title="Some title" />
```

### API

Mandatory properties

| Property | Description                              | Type     | Value                                              |
| :------- | :--------------------------------------- | :------- | :------------------------------------------------- |
| iso      | **ISO 639-1** identifier of the language | `String` | one of the values defined [here](#available-flags) |

Optional properties

| Property | Description  | Type      | Default |
| :------- | :----------- | :-------- | :------ |
| squared  | Squared flag | `Boolean` | `true`  |
| title    | Title        | `String`  | `null`  |

## Available Flags

Here follows the list of the currently available flags.
They are identified using the [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) standard.

| Language    | Code |
| :---------- | :--- |
| Arabic      | ar   |
| Armenian    | am   |
| Azerbaijani | az   |
| Belarusian  | be   |
| Bengali     | bn   |
| Bulgarian   | bg   |
| Chinese     | zh   |
| Catalan     | ca   |
| Czech       | cs   |
| English     | en   |
| Estonian    | et   |
| French      | fr   |
| German      | de   |
| Hausa       | ha   |
| Hindi       | hi   |
| Hungarian   | hu   |
| Italian     | it   |
| Japanese    | ja   |
| Javanese    | jv   |
| Khmer       | km   |
| Korean      | ko   |
| Latvian     | lv   |
| Malay       | ms   |
| Marathi     | mr   |
| Persian     | fa   |
| Polish      | pl   |
| Portuguese  | pt   |
| Romanian    | ro   |
| Russian     | ru   |
| Spanish     | es   |
| Swahili     | sw   |
| Tamil       | ta   |
| Telugu      | te   |
| Thai        | th   |
| Turkish     | tr   |
| Uzbek       | uz   |
| Vietnamese  | vi   |

## Contributing

Please follow the guidelines [here](https://github.com/qWici/vue-lang-code-flags/blob/master/CONTRIBUTING.md).
