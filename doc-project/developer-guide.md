# highlightjs-octave Developer Guide

This document is a guide and notes for developers working on highlightjs-octave (the third-party contributed language) itself. If you are a user of highlightjs-octave, or a core Highlight.js maintainer, you can ignore it entirely.

## General stuff

This project, while maintained by [Andrew Janke](https://apjanke.net), is hosted under the [`highlightjs` GitHub org](https://github.com/highlightjs), and needs to follow all their development and maintenance standards and procedures. See the Highlight.js [Language Contributor Checklist](https://highlightjs.readthedocs.io/en/latest/language-contribution.html) and [3rd-party Language Quickstart Guide](https://github.com/highlightjs/highlight.js/blob/main/extra/3RD_PARTY_QUICK_START.md).

This is a Node.js module, which is published on NPM. Any generic doco about Node.js modules and NPM publishing is relevant. [This article on auth0.com](https://auth0.com/blog/developing-npm-packages/) seems decent as an introductory guide. A lot of other articles you get when googling for "NPM module development" do not.

The main developer (Andrew) works primarily on macOS, but this module and repo should work on all of Mac, Linux, and Windows.

## Testing

To test this language definition, link it into a highlight.js repo checkout and run its tests, as described in the [Highlight.js 3rd Party Quickstart Guide](https://github.com/highlightjs/highlight.js/blob/main/extra/3RD_PARTY_QUICK_START.md).

These tests will currently fail, because this language definition will cause some examples to be detected as octave instead of matlab, breaking the matlag language definition tests. I can't yet figure out how to turn this off with `disableAutodetect: true` in the octave language definition. TODO: Figure this out.

## Things to do regularly

* Check the [Highlight.js Security Policy](https://github.com/highlightjs/highlight.js/security/policy) to see which major version is still supported, and upgrade to at least the oldest still-supported version.
* Check for security issues with `npm audit`.
