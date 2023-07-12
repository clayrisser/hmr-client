# hmr-client

[![GitHub stars](https://img.shields.io/github/stars/codejamninja/hmr-client.svg?style=social&label=Stars)](https://github.com/codejamninja/hmr-client)

> A client for communicating with hot module replacement (HMR)

![](assets/hmr-client.png)

Please ★ this repo if you found it useful ★ ★ ★

![](assets/hmr-client.png)

## Features

* listen to connected event
* listen to close event
* listen to hash event
* listen to still-ok event
* listen to content-changed event
* listen to warnings event
* listen to errors event
* listen to ok event


## Installation

```sh
npm install --save hmr-client
```


## Dependencies

* [NodeJS](https://nodejs.org)
* [Hot Module Replacement (HMR)](https://webpack.js.org/concepts/hot-module-replacement)


## Usage

```js
import HRMClient from 'hmr-client';

const client = new HMRClient({ port: 3000 });
client.onConnected = () => {
  console.log('connected');
};
client.onHash = message => {
  console.log('hash', message.data)
};
client.onStillOk = () => {
  console.log('still-ok');
};
client.onOk = () => {
  console.log('ok');
};
client.onContentChanged = () => {
  console.log('content-changed');
};
client.onWarnings = message => {
  console.log('warnings', message);
};
client.onErrors = message => {
  console.log('errors', message);
};
client.onClose = () => {
  console.log('close');
  console.log(
    'The development server has disconnected.\n' +
      'Refresh the page if necessary.'
  );
};
```


## Support

Submit an [issue](https://github.com/codejamninja/hmr-client/issues/new)


## Screenshots

[Contribute](https://github.com/codejamninja/hmr-client/blob/master/CONTRIBUTING.md) a screenshot


## Contributing

Review the [guidelines for contributing](https://github.com/codejamninja/hmr-client/blob/master/CONTRIBUTING.md)


## License

[MIT License](https://github.com/codejamninja/hmr-client/blob/master/LICENSE)

[Jam Risser](https://codejam.ninja) © 2018


## Changelog

Review the [changelog](https://github.com/codejamninja/hmr-client/blob/master/CHANGELOG.md)


## Credits

* [Jam Risser](https://codejam.ninja) - Author


## Support on Liberapay

A ridiculous amount of coffee ☕ ☕ ☕ was consumed in the process of building this project.

[Add some fuel](https://liberapay.com/codejamninja/donate) if you'd like to keep me going!

[![Liberapay receiving](https://img.shields.io/liberapay/receives/codejamninja.svg?style=flat-square)](https://liberapay.com/codejamninja/donate)
[![Liberapay patrons](https://img.shields.io/liberapay/patrons/codejamninja.svg?style=flat-square)](https://liberapay.com/codejamninja/donate)
