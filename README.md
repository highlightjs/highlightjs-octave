# highlightjs-octave

This is a Highlight.js syntax definition for [GNU Octave](https://octave.org).

## Usage

Simply include the `highlight.js` script package in your webpage or Node app, load up this module, and apply it to `hljs`.

If you're not using a build system and just want to embed this in your webpage:

```html
<script src="https://cdn.jsdelivr.net/npm/highlightjs"></script>
<script src="https://cdn.jsdelivr.net/npm/highlightjs-octave"></script>
<script>
  hljs.registerLanguage("octave", window.hljsDefineVue);
  hljs.initHighlightingOnLoad();
</script>
```

If you're using webpack / rollup / browserify / node:

```javascript
var hljs = require("highlightjs");
var hljsDefineVue = require("highlightjs-octave");

hljsDefineVue(hljs);
hljs.initHighlightingOnLoad();
```

## License

![BSD 3-Clause License](https://img.shields.io/github/license/highlightjs/highlightjs-vue?logo=License%20BSD-3-Clause)

BSD 3-Clause License.
