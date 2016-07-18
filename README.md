# meanie-angular-key-codes

[![npm version](https://img.shields.io/npm/v/meanie-angular-key-codes.svg)](https://www.npmjs.com/package/meanie-angular-key-codes)
[![node dependencies](https://david-dm.org/meanie/angular-key-codes.svg)](https://david-dm.org/meanie/angular-key-codes)
[![github issues](https://img.shields.io/github/issues/meanie/angular-key-codes.svg)](https://github.com/meanie/angular-key-codes/issues)
[![codacy](https://img.shields.io/codacy/52a227e315104dc48b9e8d715e23f088.svg)](https://www.codacy.com/app/meanie/angular-key-codes)
[![Join the chat at https://gitter.im/meanie/meanie](https://img.shields.io/badge/gitter-join%20chat%20%E2%86%92-brightgreen.svg)](https://gitter.im/meanie/meanie?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

An Angular service to facilitate handling of keyboard input events

Contains a map of common key codes as well as several utility helper functions.

![Meanie](https://raw.githubusercontent.com/meanie/meanie/master/meanie-logo-full.png)

## Installation

You can install this package using `npm`:

```shell
npm install meanie-angular-key-codes --save
```

Include the script `node_modules/meanie-angular-key-codes/release/meanie-angular-key-codes.js` in your build process, or add it via a `<script>` tag to your `index.html`:

```html
<script src="node_modules/meanie-angular-key-codes/release/meanie-angular-key-codes.js"></script>
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

Please report any bugs, issues, suggestions and feature requests in the [meanie-angular-key-codes issue tracker](https://github.com/meanie/angular-key-codes/issues).

## Contributing

Pull requests are welcome! If you would like to contribute to Meanie, please check out the [Meanie contributing guidelines](https://github.com/meanie/meanie/blob/master/CONTRIBUTING.md).

## Credits

* Meanie logo designed by [Quan-Lin Sim](mailto:quan.lin.sim+meanie@gmail.com)

## License

(MIT License)

Copyright 2016, [Adam Buczynski](http://adambuczynski.com)
