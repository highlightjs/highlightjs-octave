# highlightjs-octave

This is a Highlight.js syntax definition for [GNU Octave](https://octave.org).

## Usage

Include the `highlight.js` script package in your web page or Node app, load up this module, and apply it to `hljs`.

### Static website or simple usage

If you're not using a build system and just want to embed this in your webpage, load the module after loading Highlight.js. You'll use the minified version found in the dist directory. This module is just a CDN build of the language, so it will register itself as the JavaScript is loaded.

```html
<script type="text/javascript" src="/path/to/highlight.min.js"></script>
<script type="text/javascript" src="/path/to/octave.min.js"></script>
<script>
  hljs.highlightAll();
</script>
```

### With Node or another build system

If you're using Node.js/Webpack/Rollup/Browserify/etc, require the language module, and then register it with Highlight.js:

```javascript
var hljs = require("highlightjs");
var hljsOctave = require("highlightjs-octave");

hljs.registerLanguage("octave", hljsOctave);
hljs.highlightAll();
```

## Requirements

Highlightjs-octave works with the latest major version of Highlight.js (as described in the [Highlight.js Security Policy](https://github.com/highlightjs/highlight.js/security/policy)). As of February 2022, this is Highlight.js version 11.x.

## License

![BSD 3-Clause License](https://img.shields.io/github/license/highlightjs/highlightjs-vue?logo=License%20BSD-3-Clause)

BSD 3-Clause License.

## Credits

Highlightjs-octave is written by [Andrew Janke](https://apjanke.net).

Code is largely based on the [Highlight.js Matlab language definition](https://github.com/highlightjs/highlight.js/blob/master/src/languages/matlab.js) by Denis Bardadym <bardadymchik@gmail.com>, Eugene Nizhibitsky <nizhibitsky@ya.ru>, and Egor Rogov <e.rogov@postgrespro.ru>.

Packaging stuff is based on the [`highlightjs-view` package](https://github.com/highlightjs/highlightjs-vue).
