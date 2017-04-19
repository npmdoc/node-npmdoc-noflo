# npmdoc-noflo

#### api documentation for  [noflo (v0.8.3)](http://noflojs.org/)  [![npm package](https://img.shields.io/npm/v/npmdoc-noflo.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-noflo) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-noflo.svg)](https://travis-ci.org/npmdoc/node-npmdoc-noflo)

#### Flow-Based Programming environment for JavaScript

[![NPM](https://nodei.co/npm/noflo.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/noflo)

- [https://npmdoc.github.io/node-npmdoc-noflo/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-noflo/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-noflo/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-noflo/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-noflo/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-noflo/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Henri Bergius"
    },
    "bin": {
        "noflo": "./bin/noflo",
        "noflo-cache-preheat": "./bin/noflo-cache-preheat"
    },
    "bugs": {
        "url": "https://github.com/noflo/noflo/issues"
    },
    "dependencies": {
        "coffee-script": "~1.12.0",
        "debug": "^2.5.2",
        "fbp": "~1.5.0",
        "fbp-graph": "^0.1.0",
        "fbp-manifest": "~0.1.13"
    },
    "description": "Flow-Based Programming environment for JavaScript",
    "devDependencies": {
        "chai": "^3.5.0",
        "coffee-loader": "^0.7.2",
        "fbp-loader": "^0.1.1",
        "grunt": "^1.0.1",
        "grunt-cli": "^1.2.0",
        "grunt-coffeelint": "^0.0.16",
        "grunt-contrib-coffee": "^1.0.0",
        "grunt-contrib-connect": "^1.0.1",
        "grunt-contrib-watch": "~1.0.0",
        "grunt-mocha-phantomjs": "^4.0.0",
        "grunt-mocha-test": "^0.13.2",
        "grunt-noflo-browser": "^1.1.4",
        "json-loader": "^0.5.4",
        "mocha": "^3.1.2"
    },
    "directories": {},
    "dist": {
        "shasum": "4237921da5159383ad1870701a9f005ef5fc0fe7",
        "tarball": "https://registry.npmjs.org/noflo/-/noflo-0.8.3.tgz"
    },
    "docco_husky": {
        "output_dir": "docs",
        "project_name": "NoFlo"
    },
    "engines": {
        "node": ">= 4"
    },
    "gitHead": "4be2f0c5cddcd6165640e4a656a2dd29ab6f40c5",
    "homepage": "http://noflojs.org/",
    "keywords": [
        "fbp",
        "workflow",
        "flow",
        "noflo"
    ],
    "license": "MIT",
    "main": "./lib/NoFlo",
    "maintainers": [
        {
            "name": "bergie"
        }
    ],
    "name": "noflo",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/noflo/noflo.git"
    },
    "scripts": {
        "test": "grunt test"
    },
    "version": "0.8.3"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
