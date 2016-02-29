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

<br />

[![Build Status](https://travis-ci.org/electricimp/imp-build-api-v4.svg?branch=master)](https://travis-ci.org/electricimp/imp-build-api-v4)

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

`.restartDevice(deviceId)`

### .listModels()

`.listModels([name])`

### .createModel()

`.createModel(name)`

### .deleteModel()

`.deleteModel(modelId)`

### .getModel()

`.getModel(modelId)`

### .updateModel()

`.updateModel(modelId, [name])`

### .restartModel()

`.restartModel(modelId)`

### .listRevisions()

`.listRevisions(modelId, [since], [until], [buildMin], [buildMax])`

### .createRevision()

`.createRevision(modelId, [deviceCode], [agentCode], [releaseNotes])`

### .getRevision()

`.getRevision(modelId, buildNumber)`

### .getDeviceLogs()

`.getDeviceLogs(deviceId, [since])`

### .streamDeviceLogs()

`.streamDeviceLogs(deviceId, callback)`

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
