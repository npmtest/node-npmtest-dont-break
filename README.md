# npmtest-dont-break

#### test coverage for  [dont-break (v1.3.0)](https://github.com/bahmutov/dont-break)  [![npm package](https://img.shields.io/npm/v/npmtest-dont-break.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-dont-break) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-dont-break.svg)](https://travis-ci.org/npmtest/node-npmtest-dont-break)

#### Checks if the current version of your package would break dependent projects

[![NPM](https://nodei.co/npm/dont-break.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/dont-break)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-dont-break/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-dont-break/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-dont-break/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-dont-break/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-dont-break/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-dont-break/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-dont-break/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-dont-break/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-dont-break/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-dont-break/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-dont-break/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-dont-break/build/test-report.html](https://npmtest.github.io/node-npmtest-dont-break/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-dont-break/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-dont-break/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-dont-break/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-dont-break/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-dont-break/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-dont-break/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-dont-break/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-dont-break/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Gleb Bahmutov"
    },
    "bin": {
        "dont-break": "./bin/dont-break"
    },
    "bugs": {
        "url": "https://github.com/bahmutov/dont-break/issues"
    },
    "config": {
        "pre-git": {
            "commit-msg": "simple",
            "pre-commit": [
                "npm run mocha",
                "npm test"
            ],
            "pre-push": [
                "npm run e2e",
                "npm run size"
            ],
            "post-merge": []
        }
    },
    "contributors": [],
    "dependencies": {
        "chdir-promise": "0.2.1",
        "check-more-types": "2.23.0",
        "commander": "2.9.0",
        "debug": "2.2.0",
        "ggit": "^1.11.1",
        "hr": "0.1.3",
        "lazy-ass": "1.5.0",
        "lodash": "3.10.1",
        "npm-registry": "0.1.13",
        "npm-utils": "1.9.0",
        "os-tmpdir": "1.0.2",
        "q": "2.0.3",
        "quote": "0.4.0",
        "rimraf": "^2.5.4",
        "strip-json-comments": "2.0.1",
        "top-dependents": "1.0.0",
        "update-notifier": "0.5.0"
    },
    "description": "Checks if the current version of your package would break dependent projects",
    "devDependencies": {
        "git-issues": "1.3.1",
        "matchdep": "1.0.1",
        "mocha": "2.3.3",
        "pre-git": "3.10.0",
        "semantic-release": "4.3.5",
        "standard": "8.5.0"
    },
    "directories": {},
    "dist": {
        "shasum": "328e2cb67e780c00314522323b1f676ca69534c6",
        "tarball": "https://registry.npmjs.org/dont-break/-/dont-break-1.3.0.tgz"
    },
    "engines": {
        "node": ">= 0.12.0",
        "npm": ">= 3.0.0"
    },
    "files": [
        "bin",
        "index.js",
        "src/*.js",
        "!src/*-spec.js"
    ],
    "gitHead": "3372684550f79ba9f757c4b3fec88f5b8fd89f51",
    "homepage": "https://github.com/bahmutov/dont-break",
    "keywords": [
        "check",
        "dependency",
        "semver",
        "test",
        "update"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "bahmutov"
        }
    ],
    "name": "dont-break",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/bahmutov/dont-break.git"
    },
    "scripts": {
        "e2e": "./test/e2e.sh",
        "issues": "git-issues",
        "lint": "standard --verbose --fix bin/*.js src/*.js",
        "mocha": "mocha src/**/*-spec.js",
        "pretest": "npm run lint",
        "semantic-release": "semantic-release pre && npm publish && semantic-release post",
        "show-help": "./bin/dont-break --help",
        "size": "t=\"$(npm pack .)\"; wc -c \"${t}\"; tar tvf \"${t}\"; rm \"${t}\";",
        "test": "npm run show-help",
        "test-empty": "node src/test/run-dont-break.js"
    },
    "version": "1.3.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
