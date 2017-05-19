
# ember-cli-stylelint-suave

An Ember-CLI addon that allows easy integration with [stylelint](http://stylelint.io/) and the DockYard best practices configuration.
This is heavily influenced by [ember-cli-stylelint](https://raw.githubusercontent.com/billybonks/ember-cli-stylelint).

## Installation

`ember install ember-cli-stylelint-suave`

## Syntax
By default syntax is `scss`, if you want to use another one you need to configure the option in your `ember-cli-build`

```javascript
var app = new EmberApp(defaults, {
  stylelint: {
    linterConfig:{
      syntax: 'less'
    },
  }
});
```

You can use one of the following values for `syntax`
- scss
- css
- less
- sugarss

## Configuration

Linting configuration can be added in a

* a stylelint property in package.json
* a .stylelintrc file
* a stylelint.config.js file exporting a JS object

as required by [stylelint](http://stylelint.io/user-guide/configuration/).

the parent key is `styleLint`

## Options

Options are any options accepted by [broccoli-stylelint](https://github.com/billybonks/broccoli-stylelint) as well as:

`includePaths` {array of strings}

Paths representing trees to lint. The app tree itself will always be included.
In an addon, that path is `tests/dummy/app/styles/` (by default). Addon authors
can set `includePaths: [ 'app/styles' ]` to also lint styles in `app/styles/`.

## Running Tests

Tests still need to be added.
