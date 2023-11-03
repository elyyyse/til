# Create a range slider with precise values

Range inputs are typically meant for [things that don't require a precise value](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/range), like volume. But if you do need a [slider that limits the user to certain inputs](https://github.com/elyyyse/Interactive-pricing-component), and those values are not evenly spaced (meaning you can't rely on 'step'), here's what you can do:

### Create your `<input>`

```
// set 'min' to 0, set 'max' to limit your slider
// to the number of valid values you have

<input
  type='range'
  min={0}
  max={4}
  step={1}
></input>;
```

### Create an array to store your valid values

```
// simple use case
const VALID_VALUES = [8, 12, 16, 24, 36];

// more complex use case
const VALID_VALUES = [
  {pricePerMonth: 8, pricePerYear: 72, pageviews: '10K'},
  {pricePerMonth: 12, pricePerYear: 108, pageviews: '15K'},
  // ...etcetera
];
```

### And then you can capture those specific values

```
const slider = document.querySelector('input[type='range]');

VALID_VALUES[slider.value].pageviews
VALID_VALUES[slider.value].pricePerMonth
VALID_VALUES[slider.value].pricePerYear
```
