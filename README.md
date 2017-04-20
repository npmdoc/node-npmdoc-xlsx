# npmdoc-xlsx

#### api documentation for  [xlsx (v0.9.11)](https://oss.sheetjs.com/js-xlsx/)  [![npm package](https://img.shields.io/npm/v/npmdoc-xlsx.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-xlsx) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-xlsx.svg)](https://travis-ci.org/npmdoc/node-npmdoc-xlsx)

#### Excel (XLSB/XLSX/XLSM/XLS/XML) and ODS (ODS/FODS/UOS) spreadsheet parser and writer

[![NPM](https://nodei.co/npm/xlsx.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/xlsx)

- [https://npmdoc.github.io/node-npmdoc-xlsx/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-xlsx/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-xlsx/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-xlsx/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-xlsx/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-xlsx/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "xlsx",
    "version": "0.9.11",
    "author": "sheetjs",
    "description": "Excel (XLSB/XLSX/XLSM/XLS/XML) and ODS (ODS/FODS/UOS) spreadsheet parser and writer",
    "keywords": [
        "excel",
        "xls",
        "xlsx",
        "xlsb",
        "xlsm",
        "ods",
        "office",
        "spreadsheet"
    ],
    "bin": {
        "xlsx": "./bin/xlsx.njs"
    },
    "main": "./xlsx",
    "browser": {
        "node": false,
        "crypto": false,
        "stream": false,
        "fs": false
    },
    "dependencies": {
        "exit-on-epipe": "~1.0.0",
        "ssf": "~0.9.0",
        "codepage": "~1.8.0",
        "cfb": "~0.11.1",
        "crc-32": "~1.0.0",
        "adler-32": "~1.0.0",
        "commander": "~2.9.0"
    },
    "devDependencies": {
        "mocha": "",
        "xlsjs": "",
        "uglify-js": ""
    },
    "repository": {
        "type": "git",
        "url": "git://github.com/SheetJS/js-xlsx.git"
    },
    "scripts": {
        "pretest": "git submodule init && git submodule update",
        "test": "make travis"
    },
    "config": {
        "blanket": {
            "pattern": "xlsx.js"
        }
    },
    "homepage": "https://oss.sheetjs.com/js-xlsx/",
    "bugs": {
        "url": "https://github.com/SheetJS/js-xlsx/issues"
    },
    "license": "Apache-2.0",
    "engines": {
        "node": ">=0.8"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
