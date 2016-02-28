# Electric Imp Build API v4 Client

Node.js client for [Build API v4](https://electricimp.com/docs/buildapi/).

This package deprecates https://www.npmjs.com/package/imp-api.

## Installation

```bash
npm i -g imp-build-api-v4
```

Node.js 4.0+ is required.

## Example

```js
const BuildAPIClient = require('imp-build-api-v4');

let client = new BuildAPIClient();
client.apiKey = '<your Build API key>';

// print list of devices
client.listDevices()
  .then((res) => {
    console.log('Devices:', res.devices);
  })
  .catch(console.error);
```

## License

[MIT](./LICENSE)
