# stylelint-config-cssrecipes

> cssrecipes shareable config for stylelint

## Install

```console
$ npm install stylelint-config-cssrecipes
```

## Usage

As a JavaScript library

```js
var fs = require("fs")
var postcss = require("postcss")
var cssnext = require("cssnext")
var cssrecipesConfig = require("stylelint-config-cssrecipes")
var reporter = require("postcss-reporter")
var stylelint = require("stylelint")

var input = fs.readFileSync("index.css", "utf8")

var output = postcss()
  .use(stylelint(cssrecipesConfig))
  .use(reporter())
  .use(cssnext())
  .process(input)

  fs.writeFileSync("dist/index.css", output)
```


## Contributing

Work on a branch, install dev-dependencies, respect coding style & run tests before submitting a bug fix or a feature.

```console
$ git clone https://github.com/stylelint/stylelint-config-cssrecipes.git
$ git checkout -b patch-1
$ npm install
$ npm test
```

## [Changelog](CHANGELOG.md)

## [License](LICENSE)

---
