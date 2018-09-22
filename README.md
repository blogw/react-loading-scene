# react-loading-scene

A React loading scene. Сan be used as a scene saver for the initial download of the application or as an overload scene for promises.

# DEMO
![demo.gif](https://i.yapx.ru/BQgeX.gif)
## Installation

```
npm install --save react-loading-scene
```

The modular approach of this library means you're much better off building it into your code with a module bundling system like browserify or webpack.

## Browser Support

Basically IE9+.

## Usage

```js
const Loadingscene = require('react-loading-scene');
// ... or with es2015
import Loadingscene from 'react-loading-scene';
```

## Server side rendering
Library uses [styled components](https://www.npmjs.com/package/styled-components), so follow official docs to configurate, it`s very simple, [go to instructions](https://www.styled-components.com/docs/advanced#server-side-rendering)

## Examples

For details about why the examples work, read the API documentation below.

You can also see full code of demo by looking in `example/`.

```js
import React from 'react'
//...
import Loadingscene from '../react-loading-scene'

//...
  <LoadingScene
    loading={true}
    bgColor='#f1f1f1'
    spinnerColor='#9ee5f8'
    textColor='#676767'
    logoSrc='/logo.png'
    text='Here an introduction sentence (Optional)'
  >
    // ...
    // here loadable content
    // for example, async data
    //<div>Loadable content</div>
  </LoadingScene>

```

## API

module is represented by a single component, let's call it Loadingscene, import as shown above


### `LoadingScene`

Root component, it includes three subcomponents, you can control them through properties

#### props

some of props are **REQUIRED**, if not mentioned prop is OPTIONAL.

**loading** { bool }: the content of the page is loaded or not (**required parameter**).

**bgColor** { string }: background color of loading sreen. deault `#ffffff` .

**spinnerColor** { string }: spinner color. If empty param - not showing.

**textColor** { string }: text under spinner. default `#676767`.

**logoSrc** { string }: url of image. If empty param  - not showing.

**text** { string }: background color of loading sreen. If empty param  - not showing.
