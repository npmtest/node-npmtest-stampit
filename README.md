# npmtest-stampit

#### test coverage for  [stampit (v3.1.2)](https://github.com/stampit-org/stampit#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-stampit.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-stampit) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-stampit.svg)](https://travis-ci.org/npmtest/node-npmtest-stampit)

#### Create objects from reusable, composable behaviors.

[![NPM](https://nodei.co/npm/stampit.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/stampit)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-stampit/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-stampit/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-stampit/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-stampit/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-stampit/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-stampit/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-stampit/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-stampit/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-stampit/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-stampit/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-stampit/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-stampit/build/test-report.html](https://npmtest.github.io/node-npmtest-stampit/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-stampit/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-stampit/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-stampit/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-stampit/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-stampit/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-stampit/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-stampit/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-stampit/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Eric Elliott",
        "url": "https://ericelliottjs.com"
    },
    "bugs": {
        "url": "https://github.com/stampit-org/stampit/issues"
    },
    "dependencies": {},
    "description": "Create objects from reusable, composable behaviors.",
    "devDependencies": {
        "babel-cli": "^6.10.1",
        "babel-preset-es2015": "^6.16.0",
        "benchmark": "^2.1.1",
        "check-compose": "^3.2.0",
        "dependency-check": "^2.5.0",
        "eslint": "^3.7.0",
        "eslint-config-airbnb-base": "^11.0.0",
        "eslint-plugin-import": "^2.0.1",
        "istanbul": "^1.1.0-alpha.1",
        "lodash": "^4.16.1",
        "magic-string": "^0.19.0",
        "nsp": "^2.1.0",
        "require-all": "^2.0.0",
        "rimraf": "^2.3.4",
        "rollup": "^0.41.1",
        "rollup-plugin-buble": "^0.15.0",
        "rollup-plugin-filesize": "^1.0.0",
        "rollup-plugin-uglify": "^1.0.0",
        "tape": "^4.2.2",
        "watch": "^1.0.1"
    },
    "directories": {},
    "dist": {
        "shasum": "8bd956b2f1ccbdb1ed2bec4af4fce4a0120a0388",
        "tarball": "https://registry.npmjs.org/stampit/-/stampit-3.1.2.tgz"
    },
    "gitHead": "be8d00a6eec289f2f0d94e81cdb3c7efbfd2b4d9",
    "homepage": "https://github.com/stampit-org/stampit#readme",
    "jsnext:main": "dist/stampit.mjs",
    "keywords": [
        "object",
        "prototype",
        "object oriented",
        "browser",
        "inheritance",
        "oop",
        "node",
        "factory",
        "class",
        "stamp"
    ],
    "license": "MIT",
    "main": "dist/stampit.full.js",
    "maintainers": [
        {
            "name": "koresar"
        }
    ],
    "name": "stampit",
    "npmFileMap": [
        {
            "basePath": "/dist/",
            "files": [
                "stampit.full.js",
                "stampit.full.min.js"
            ]
        }
    ],
    "npmName": "stampit",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/stampit-org/stampit.git"
    },
    "scripts": {
        "audit": "nsp check",
        "build": "babel-node --presets=es2015 build",
        "check": "npm run audit && npm run deps",
        "clean": "rimraf dist/*",
        "cov": "npm run cov:clean && npm run cov:generate",
        "cov:clean": "rimraf ./coverage/",
        "cov:generate": "babel-node --presets=es2015 ./node_modules/.bin/istanbul cover test",
        "deps": "npm run deps:missing && npm run deps:extra",
        "deps:extra": "dependency-check package.json --extra --no-dev --ignore",
        "deps:missing": "dependency-check package.json",
        "lint": "eslint src && eslint test",
        "posttest": "node test/benchmark",
        "prebuild": "npm run clean",
        "precheck": "npm test",
        "prepublish": "npm run check",
        "pretest": "npm run build",
        "test": "babel-node --presets=es2015 test && npm run lint",
        "watch": "watch 'clear && npm -s test' test/ src/"
    },
    "version": "3.1.2"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
