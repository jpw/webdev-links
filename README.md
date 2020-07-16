# webdev-links
Handy references for building web sites.

## accessibility (a11y)

* [Contextually Marking up accessible images and SVGs](https://www.scottohara.me/blog/2019/05/22/contextual-images-svgs-and-a11y.html)

## GitHub

* [GitHub Standard Fork & Pull Request Workflow](https://gist.github.com/Chaser324/ce0505fbed06b947d962)

## misc

* [Papers we love](https://github.com/papers-we-love/papers-we-love)
* [JSON Web Tokens](https://jwt.io/)
   JSON Web Tokens are an open, industry standard RFC 7519 method for representing claims securely between two parties.
* [Choose Boring Technology](http://boringtechnology.club/)

## node

* [Node best practices](https://github.com/i0natan/nodebestpractices)
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

## web performance

* [Populating the page: how browsers work
](https://developer.mozilla.org/en-US/docs/Web/Performance/Populating_the_page:_how_browsers_work)
* [JavaScript Loading Priorities in Chrome](https://addyosmani.com/blog/script-priorities/)
