<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Electric Imp Build API v4 Client](#electric-imp-build-api-v4-client)
  - [Installation](#installation)
  - [Reference](#reference)
    - [.apiKey](#apikey)
    - [.debug](#debug)
    - [.listDevices()](#listdevices)
    - [.getDevice()](#getdevice)
    - [.updateDevice()](#updatedevice)
    - [.restartDevice()](#restartdevice)
    - [.listModels()](#listmodels)
    - [.createModel()](#createmodel)
    - [.deleteModel()](#deletemodel)
    - [.getModel()](#getmodel)
    - [.updateModel()](#updatemodel)
    - [.restartModel()](#restartmodel)
    - [.listRevisions()](#listrevisions)
    - [.createRevision()](#createrevision)
    - [.getRevision()](#getrevision)
    - [.getDeviceLogs()](#getdevicelogs)
    - [.streamDeviceLogs()](#streamdevicelogs)
  - [Example](#example)
  - [License](#license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Electric Imp Build API v4 Client

Node.js client for [Build API v4](https://electricimp.com/docs/buildapi/).

This package deprecates https://www.npmjs.com/package/imp-api.

## Installation

```bash
npm i -g imp-build-api-v4
```

Node.js 4.0+ is required.

## Reference

_BuildAPIClient_:

### .apiKey

_(property)_

_string_

Gets/sets Build API key.

### .debug

_(property)_

_boolean_

Enables/disables debug output.

### .listDevices()

`.listDevices([name], [deviceId], [modelId])`

{Promise}

### .getDevice()

`.getDevice(deviceId)`

### .updateDevice()

`.updateDevice(deviceId, [name], [modelId])`

### .restartDevice()

`.restartDevice(deviceId, [name], [modelId)`

### .listModels()

`.listModels(deviceId, [name], [modelId])`

### .createModel()

`.createModel(deviceId, [name], [modelId])`

### .deleteModel()

`.deleteModel(deviceId, [name], [modelId])`

### .getModel()

`.getModel(deviceId, [name], [modelId])`

### .updateModel()

`.updateModel(deviceId, [name], [modelId])`

### .restartModel()

`.restartModel(deviceId, [name], [modelId])`

### .listRevisions()

`.listRevisions(deviceId, [name], [modelId])`

### .createRevision()

`.createRevision(deviceId, [name], [modelId])`

### .getRevision()

`.getRevision(deviceId, [name], [modelId])`

### .getDeviceLogs()

`.getDeviceLogs(deviceId, [name], [modelId])`

### .streamDeviceLogs()

`.streamDeviceLogs(deviceId, [name], [modelId])`

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
