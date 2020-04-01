# Siri

## Usage

```js
import Siri from '@xes/siri';
```

## Instantitate

Create a div container and instantiate a Siri object

```html
<div id="siri-container"></div>
<script>
var siribox = new Siri({
	container: document.getElementById('siri-container'),
	width: 640,
	height: 200,
	autostart: true,
	style: 'ios9',
	waveColors: [
		{
			color: '255,255,255',
			supportLine: true,
		},
		{
			// blue
			color: '255, 255, 255',
		},
		{
			// red
			color: '173, 57, 76',
		},
		{
			// green
			color: '100, 100, 1000',
		},
	]
});
</script>
```

## Constructor options

| Key        | Type          | Description                                                            | Default    | Required |
| ---------- | ------------- | ---------------------------------------------------------------------- | ---------- | -------- |
| container  | DOMElement    | The DOM container where the DOM canvas element will be added.          | null       | yes      |
| style      | "ios", "ios9" | The style of the wave.                                                 | "ios"      | no       |
| ratio      | Number        | Ratio of the display to use. Calculated by default.                    | calculated | no       |
| speed      | Number        | The speed of the animation.                                            | 0.2        | no       |
| amplitude  | Number        | The amplitude of the complete wave-form.                               | 1          | no       |
| frequency  | Number        | The frequency of the complete wave-form. Only available in style "ios" | 6          | no       |
| color      | String        | Color of the wave. Only available in style "ios"                       | "#fff"     | no       |
| cover      | Bool          | The `canvas` covers the entire width or height of the container        | false      | no       |
| autostart  | Bool          | Decide wether start the animation on boot.                             | false      | no       |
| pixelDepth | Number        | Number of step (in pixels) used when drawed on canvas.                 | 0.02       | no       |
| lerpSpeed  | Number        | Lerp speed to interpolate properties.                                  | 0.01       | no       |
| waveColors  | Array        | line color                                                             | 0.01       | no       |

## API

#### `start()`

Start the animation

#### `stop()`

Stop the animation.

#### `setSpeed(newValue)`

Set the new value of speed (animated)

#### `setAmplitude(value)`

Set the new value of amplitude (animated)
