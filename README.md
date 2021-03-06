# @meanie/angular-key-codes

[![npm version](https://img.shields.io/npm/v/@meanie/angular-key-codes.svg)](https://www.npmjs.com/package/@meanie/angular-key-codes)
[![node dependencies](https://david-dm.org/meanie/angular-key-codes.svg)](https://david-dm.org/meanie/angular-key-codes)
[![github issues](https://img.shields.io/github/issues/meanie/angular-key-codes.svg)](https://github.com/meanie/angular-key-codes/issues)
[![codacy](https://img.shields.io/codacy/aeb62c52c95d45ff92eca4fcfc32e6ef.svg)](https://www.codacy.com/app/meanie/angular-key-codes)


An Angular service to facilitate handling of keyboard input events

Contains a map of common key codes as well as several utility helper functions.

![Meanie](https://raw.githubusercontent.com/meanie/meanie/master/meanie-logo-full.png)

## Installation

You can install this package using `yarn` or `npm`:

```shell
#yarn
yarn add @meanie/angular-key-codes

#npm
npm install @meanie/angular-key-codes --save
```

Include the script `node_modules/@meanie/angular-key-codes/release/angular-key-codes.js` in your build process, or add it via a `<script>` tag to your `index.html`:

```html
<script src="node_modules/@meanie/angular-key-codes/release/angular-key-codes.js"></script>
```

Add `KeyCodes.Service` as a dependency for your app.

## Usage

```js
angular.module('App.MyModule').controller('MyController', function($keyCodes) {
  angular.element('input').on('keydown', event => {

    //Compare against common key codes
    if (event.keyCode === $keyCodes.ENTER) {
      //...do something
    }

    //Check if input type was numeric
    if ($keyCodes.isNumeric(event)) {
      //...do something
    }

    //Check if input type was alpha
    if ($keyCodes.isAlpha(event)) {
      //...do something
    }

    //Check if input type was alphanumeric
    if ($keyCodes.isAlphaNumeric(event)) {
      //...do something
    }

    //Check if input type was a control key
    if ($keyCodes.isControl(event)) {
      //...do something
    }

    //Check if input type was numeric or additional whitelisted keys
    let whitelist = [$keyCodes.DASH, $keyCodes.SPACE];
    if ($keyCodes.isNumeric(event, whitelist)) {
      //...do something
    }
  });
});
```

## Issues & feature requests

Please report any bugs, issues, suggestions and feature requests in the [@meanie/angular-key-codes issue tracker](https://github.com/meanie/angular-key-codes/issues).

## Contributing

Pull requests are welcome! If you would like to contribute to Meanie, please check out the [Meanie contributing guidelines](https://github.com/meanie/meanie/blob/master/CONTRIBUTING.md).

## Sponsor

This package has been kindly sponsored by [Hello Club](https://helloclub.com?source=meanie), an [all in one club and membership management solution](https://helloclub.com?source=meanie) complete with booking system, automated membership renewals, online payments and integrated access and light control. Check us out if you happen to belong to any kind of club or if you know someone who helps run a club!

## License

(MIT License)

Copyright 2016-2020, Adam Reis
