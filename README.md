# Memory-watcher

## Installation

`npm i memory-watcher`

## Usage

```javascript
  const memoryWatcher = require('memory-watcher');
  const dumpsPath = path.join(__dirname, 'dumps');
  memoryWatcher(dumpsPath);
```

## Description

  Using this library you can detect memory leaks in your app and debug them easily even on production environment.
  
  at the beginning we start a `heapProfile`

  once there's a leak in your app, a `heapProfile` is written at this point to the provided path
  so you can check and detect which part of your code is causing the leak, this is very suitable in production.

  In `development` environment, an extra work will be done at the start we will write an inint `heapDump` and when there's a leak we will write another `heapDump` so you can use both the `heapDump`s and `heapProfile`s to detect the leak in your application.