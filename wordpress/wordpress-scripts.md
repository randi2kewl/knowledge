---
description: A build system built for building custom WordPress blocks.
---

# @wordpress/scripts

## Introduction

### Setup

#### Using Yarn Package Manager:

`yarn add @wordpress/scripts`  


#### Package.json

```javascript
{
    "name": "some-block-name",
    "main": "index.js",
    "scripts": {
        "start": "wp-scripts start",
        "build": "wp-scripts build"
    }
}
```

#### Running it

To build for development with "watch" running:

`yarn start`  


To build for production:

`yarn build`  


### Resources

* [NPM: @wordpress/scripts](https://www.npmjs.com/package/@wordpress/scripts)
* [Github](https://github.com/WordPress/gutenberg/tree/master/packages/scripts)

