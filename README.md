# N-API Hello, world!

## Preface
This example is tested on CentOS 8.

## Setup global build environment.
```
npm install -g yarn

yum install gcc
yum install gcc-c++
yum install python3
yum install make

yarn global add node-gyp
```

## Create package.json
```
yarn init
```
Edit package.json as you need.

## Add bindings package.
```
yarn add bindings
```

## Create addon.

See `hello.cc`

## Configure node-gyp.

See `binding.gyp`

Insert next line to top block of `package.json`.
```
  "gypfile": true
```
Don't forget comma separator.

## Build
```
node-gyp configure
node-gyp build
```

## Test

### Create test code.

See `hello.js`

### Configure test.

Insert next lines to top block of `package.json`.
```
  "scripts": {
    "test": "node hello.js"
  }
```
Don't forget comma separator.

### Run test.

```
yarn test
```

## See
https://github.com/nodejs/abi-stable-node-addon-examples/tree/master/1_hello_world/napi
