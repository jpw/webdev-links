# webdev-links
Handy references for building web sites.

## accessibility (a11y)

* [Contextually Marking up accessible images and SVGs](https://www.scottohara.me/blog/2019/05/22/contextual-images-svgs-and-a11y.html)
* [Accessible SVG Line Graphs](https://tink.uk/accessible-svg-line-graphs/)
* https://a11ysupport.io/ - which browser supports what a11y feature

### alt's (are not as simple as you think)

* W3.org [alt authoring decision tree](https://www.w3.org/WAI/tutorials/images/decision-tree/)
* [Writing Alt Text for Data Visualization](https://medium.com/nightingale/writing-alt-text-for-data-visualization-2a218ef43f81)
* [Poet Training Tool](https://poet.diagramcenter.org/how.html) an image description resource that helps people learn when and how to describe various types of images

## dataviz

* Financial Times Visual Vocabulary [GH](https://github.com/Financial-Times/chart-doctor/tree/main/visual-vocabulary) [site](https://ft-interactive.github.io/visual-vocabulary/)

## GitHub

* [GitHub Standard Fork & Pull Request Workflow](https://gist.github.com/Chaser324/ce0505fbed06b947d962)

## Jest :weary:

* [A nice guide to mocking your code in Jest](https://codeburst.io/module-mocking-in-jest-ff174397e5ff)
* relatedly, [Mock Service Worker](https://mswjs.io/docs): mock the network, not your client.

## misc

* [Papers we love](https://github.com/papers-we-love/papers-we-love)
* [JSON Web Tokens](https://jwt.io/)
   JSON Web Tokens are an open, industry standard RFC 7519 method for representing claims securely between two parties.
* [Choose Boring Technology](http://boringtechnology.club/)
* [On Dogmatism](https://css-tricks.com/increasing-wariness-dogmatism/)

## node

* [Node best practices](https://github.com/i0natan/nodebestpractices)
* [JSDoc commenting for node](https://jsdoc.app/howto-commonjs-modules.html)
* [Node error handling](https://www.joyent.com/node-js/production/design/errors)
   * operational error in async function? create/pass Error to callback. Client handles in cb.
   * operational error in synchronous function? typically throw, sometimes return Error, or emit Error on an EventEmitter. Client handles in try/catch.
      * _either way a fn must not pass and throw_ because client code has to handle both cases.
   * programmer error? By default, throw and crash. The program is in an unpredictable state. Bail. "Send help!"
   * Bad input to fn, e.g. a String which is not really an IP? Throw. Be strict. Looseness is hard to fix later.
   * On rare occasions we must not crash, consider [domains](https://nodejs.org/api/domain.html) and [process.on('uncaughtException')](https://nodejs.org/api/process.html#process_event_uncaughtexception).
   * when making Errors:
      * Use Error objects (or subclasses) for all errors, and provide `name` and `message`.
      * Built-in JavaScript names you may want to reuse include "RangeError" and "TypeError".
      * Augment the Error object with properties that explain details, e.g. if you failed to connect to a server, use `remoteIp` to say which IP you tried to connect to. Sanitise it.

## npm

 * [An Open Source Maintainer's Guide to Publishing npm Packages](https://node.dev/post/an-open-source-maintainers-guide-to-publishing-npm-packages)


## web components

 * [All the Ways to Make a Web Component - June 2020 Update](https://webcomponents.dev/blog/all-the-ways-to-make-a-web-component/)
 
## web performance

* [Populating the page: how browsers work
](https://developer.mozilla.org/en-US/docs/Web/Performance/Populating_the_page:_how_browsers_work)
* [JavaScript Loading Priorities in Chrome](https://addyosmani.com/blog/script-priorities/)
  ![JavaScript Loading Priorities in Chrome table](img/js-prios.png?raw=true)
* [Deep dive into BlinkNG rendering](https://developer.chrome.com/docs/chromium/blinkng)
  
## UX

* https://www.nngroup.com/
* https://lawsofux.com/
* https://www.interaction-design.org/literature/article/what-is-interaction-design
* https://careerfoundry.com/en/blog/ux-design/what-is-user-experience-ux-design-everything-you-need-to-know-to-get-started/

