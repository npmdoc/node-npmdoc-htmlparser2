# npmdoc-htmlparser2

#### api documentation for  [htmlparser2 (v3.9.2)](https://github.com/fb55/htmlparser2#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-htmlparser2.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-htmlparser2) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-htmlparser2.svg)](https://travis-ci.org/npmdoc/node-npmdoc-htmlparser2)

#### Fast & forgiving HTML/XML/RSS parser

[![NPM](https://nodei.co/npm/htmlparser2.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/htmlparser2)

- [https://npmdoc.github.io/node-npmdoc-htmlparser2/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-htmlparser2/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-htmlparser2/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-htmlparser2/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-htmlparser2/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-htmlparser2/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Felix Boehm"
    },
    "browser": {
        "readable-stream": false
    },
    "bugs": {
        "url": "http://github.com/fb55/htmlparser2/issues"
    },
    "dependencies": {
        "domelementtype": "^1.3.0",
        "domhandler": "^2.3.0",
        "domutils": "^1.5.1",
        "entities": "^1.1.1",
        "inherits": "^2.0.1",
        "readable-stream": "^2.0.2"
    },
    "description": "Fast & forgiving HTML/XML/RSS parser",
    "devDependencies": {
        "coveralls": "^2.11.4",
        "eslint": "^2.12.0",
        "istanbul": "^0.4.3",
        "mocha": "^2.2.5",
        "mocha-lcov-reporter": "^1.2.0"
    },
    "directories": {
        "lib": "lib/"
    },
    "dist": {
        "shasum": "1bdf87acca0f3f9e53fa4fcceb0f4b4cbb00b338",
        "tarball": "https://registry.npmjs.org/htmlparser2/-/htmlparser2-3.9.2.tgz"
    },
    "files": [
        "lib"
    ],
    "gitHead": "e1f12f626f65cf4a082f89bdde89081b54187818",
    "homepage": "https://github.com/fb55/htmlparser2#readme",
    "keywords": [
        "html",
        "parser",
        "streams",
        "xml",
        "dom",
        "rss",
        "feed",
        "atom"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "feedic"
        }
    ],
    "name": "htmlparser2",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/fb55/htmlparser2.git"
    },
    "scripts": {
        "coveralls": "npm run lint && npm run lcov && (cat coverage/lcov.info | coveralls || exit 0)",
        "lcov": "istanbul cover _mocha --report lcovonly -- -R spec",
        "lint": "eslint lib test",
        "test": "mocha && npm run lint"
    },
    "version": "3.9.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
