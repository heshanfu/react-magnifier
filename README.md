# react-magnifier

[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/samuelmeuli/react-magnifier/blob/master/LICENSE)
[![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/samuelmeuli/react-magnifier/pulls)

**React component for zooming in on images**

* simple and customizable
* supports touch screens
* allows using different files for large image and magnifying glass (e.g. thumbnail and high-resolution image)

→ **[Demo](https://samuelmeuli.github.io/react-magnifier)**

<p align="center">
  <img src=".github/demo.gif" width=600 alt="Demo">
</p>


## Usage

Install the package using NPM:

```
npm install react-magnifier
```

Add the component to your React application:

```jsx
import Magnifier from 'react-magnifier';
import yourImage from './path/to/image';

// Somewhere in your code:
<Magnifier src={yourImage} width={500} />
```


## Configuration

Prop | Type | Default | Description
---- | ---- | ------- | -----------
`src` (required) | String | – | URL/path of the large image
`alt` | String | – | Alternate text for the large image
`width` | Number/String | `'100%'` | Image width (absolute or relative values possible)
`height` | Number/String | `'auto'` | Image width (absolute or relative values possible)
`zoomImgSrc` | String | – | URL/path of the image inside the magnifying glass (if not specified, the large image will be used)
`zoomFactor` | Number | `1.5` | Factor by which the zoom image will be scaled (based on the size of the large image)
`mgWidth` | Number | `150` | Width of the magnifying glass in px
`mgHeight` | Number | `150` | Height of the magnifying glass in px
`mgShape` | String | `'circle'` | Shape of the magnifying glass (possible values: `'circle'`, `'square'`)
`mgMouseOffsetX` | Number | `0` | Horizontal offset of the magnifying glass in px when hovering with a mouse
`mgMouseOffsetY` | Number | `0` | Vertical offset of the magnifying glass in px when hovering with a mouse
`mgTouchOffsetX` | Number | `-50` | Horizontal offset of the magnifying glass in px when dragging on a touch screen
`mgTouchOffsetY` | Number | `-50` | Vertical offset of the magnifying glass in px when dragging on a touch screen


## Custom styling

```scss
.magnifier {
  // styles for <div> around image and magnifying glass
}

.magnifier-image {
  // styles for large image
}

.magnifying-glass {
  // styles for magnifying glass
}
```


## Development

* `git clone`
* `npm install`
* `npm start` to generate the library bundle using [Rollup](https://github.com/rollup/rollup)
* Open `localhost:3000` to see the component in action using [Storybook](https://github.com/storybooks/storybook)
