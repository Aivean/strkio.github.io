# strkio.github.io [![Build Status](https://travis-ci.org/strkio/strkio.github.io.svg?branch=develop)](https://travis-ci.org/strkio/strkio.github.io) 

[strk.io](http://strk.io/)

- For latest updates and announcements, follow on Twitter: [@strkio](https://twitter.com/strkio).
- Live discussion: [![Join the chat at https://gitter.im/strkio/strkio.github.io](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/strkio/strkio.github.io?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge).
- Bugs, suggestions, feature requests: [GitHub Issues](https://github.com/strkio/strkio.github.io/issues).

## Features
- Responsive 
  
  Designed mobile-first. Use it on your phone, tablet or desktop.

- Transparent

  Your data always stays with you (as a private Gist).
  Whenever you make a change, your browser talks to the GitHub API directly.
  There is nothing else in between.

- Offline

  You don't have to be connected to the Internet to update your streaks (or to keep strk.io tab open for that matter). Everything is kept locally, just in case. 
  
- Hackable

  strk.io provides a simple <a href="https://github.com/strkio/strkio-api-server">HTTP API</a> for easier integration with external services/tools.

## Development

> PREREQUISITE: [Node.js](http://nodejs.org/) >= 0.10, NPM, [Bower](http://bower.io/) and [Gulp](http://gulpjs.com/). 

```sh
$ git clone https://github.com/strkio/strkio.github.io
$ cd strkio.github.io
$ npm install && bower install
$ gulp serve
```

## Testing 

> If you intend to use [PhantomJS](https://github.com/ariya/phantomjs), it MUST be >= 2.0.0 (for MacOSX/Linux builds 
  [look here](https://github.com/eugene1g/phantomjs/releases)). 

```sh
$ # run unit tests
$ gulp test:unit

$ # run specific unit test(s)
$ gulp test:unit --grep '<substring>'

$ # run e2e tests on phantomjs
$ gulp test:e2e
 
$ # run e2e tests on chrome/firefox/... 
$ gulp test:e2e --browser=<name_1> --browser=<name_2>

$ # run e2e tests on Sauce Labs
$ SAUCE_USERNAME=<username> SAUCE_ACCESS_KEY=<password> gulp test:e2e --browser=saucelabs

$ # run e2e tests sequentially or in parallel (default is 2)
$ gulp test:e2e --concurrency=1

$ # run specific e2e test(s) 
$ gulp test:e2e --mochaArg=-g --mochaArg="<name>"
 
$ # test <subdomain>.ngrok.com instead of localhost:8000 (e2e) 
$ gulp test:e2e --target=<subdomain>.ngrok.com  
```

## Deploying to GitHub Pages

> (note to the maintainers) 'git push' to the 'stable' branch triggers deployment (via 
[Travis CI](https://travis-ci.org/strkio/strkio.github.io)) automatically.

```sh
$ gulp build && gulp deploy
```

## Contributing

In lieu of a formal styleguide, please take care to maintain the existing coding style.
Executing `gulp lint` within project directory should not produce any errors.

## Latest test results

[![Sauce Test Status](https://saucelabs.com/browser-matrix/strkio.svg)](https://saucelabs.com/u/strkio)

## License

[MIT](http://opensource.org/licenses/mit-license.php).
