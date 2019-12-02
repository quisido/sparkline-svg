# Sparkline SVG  [![version](https://img.shields.io/npm/v/sparkline-svg.svg)](https://www.npmjs.com/package/sparkline-svg) [![minzipped size](https://img.shields.io/bundlephobia/minzip/sparkline-svg.svg)](https://www.npmjs.com/package/sparkline-svg) [![downloads](https://img.shields.io/npm/dt/sparkline-svg.svg)](https://www.npmjs.com/package/sparkline-svg) [![build](https://api.travis-ci.com/CharlesStover/sparkline-svg.svg)](https://travis-ci.com/CharlesStover/sparkline-svg/)

Generate a Sparkline as an SVG.

## Install

* `npm install sparkline-svg` or
* `yarn add sparkline-svg`

## Table of Contents

* [Use](#use)
  * [`d`](#get-d-string)
  * [`dataUri`](#get-datauri-string)
  * [`outerHTML`](#get-outerhtml-string)
  * [`setDecimals`](#setdecimalsdecimals-number-this)
  * [`setDesc`](#setdescdesc-string-this)
  * [`setDescription`](#setdescriptiondesc-string-this)
  * [`setFill`](#setfillfill-string-this)
  * [`setHeight`](#setheightheight-string-this)
  * [`setPreserveAspectRatio`](#setpreserveaspectratiopreserveaspectratio-string-this)
  * [`setStroke`](#setstrokestroke-string-this)
  * [`setStrokeWidth`](#setstrokewidthstrokewidth-number--string-this)
  * [`setTitle`](#settitletitle-string-this)
  * [`setValues`](#setvaluesvalues-number-this)
  * [`setViewBoxHeight`](#setviewboxheightviewboxheight-number-this)
  * [`setViewBoxWidth`](#setviewboxwidthviewboxwidth-number-this)
  * [`setWidth`](#setwidthwidth-string-this)

## Use

The `sparkline-svg` package exports a Sparkline class, which can be constructed with or without an array of values used to generate the sparkline.

```JavaScript
import Sparkline from 'sparkline-svg';

const sparkline= new Sparkline();
// or
const sparkline = new Sparkline(values);
```

### get d(): string

`sparkline.d` returns the `<path />`'s `d` attribute for the sparkline (stroke) itself.

### get dataUri(): string

`sparkline.dataUri` returns the sparkline SVG as a data URI, i.e. `data:image/svg+xml;base64,...`. This is particularly useful for CSS background images.

### get outerHTML(): string

`sparkline.outerHTML` returns a string of the HTML for an SVG containing the sparkline.

### setDecimals(decimals: number): this

Sets the number of decimal places used to generate the sparkline. A larger number of decimal places will result in better precision, but a larger file size.

_Default: 4_

### setDesc(desc: string): this

Sets the description of the sparkline. Used to populate the `<desc>` element.

_Default: 'A line graph representation of a value\'s change over time.'_

### setDescription(desc: string): this

Synonymous with `setDesc`.

### setFill(fill: string): this

Sets the color of the area underneath the sparkline.

_Default: 'transparent'_

### setHeight(height: string): this

Sets the height of the sparkline's SVG element. Not to be confused with `setViewBoxHeight`.

_Default: '100%'_

### setPreserveAspectRatio(preserveAspectRatio: string): this

Sets the `preserveAspectRatio` attribute of the SVG element.

_Default: 'none'_

### setStroke(stroke: string): this

Sets the color of the sparkline itself.

_Default: 'currentColor'_

### setStrokeWidth(strokeWidth: number | string): this

Sets the width of the sparkline itself. If using a number, this will be relative to the view box height and width.

_Default: '1%'_

### setTitle(title: string): this

Sets the title of the sparkline SVG by populating the `<title>` element. This is useful for accessibility purposes and often appears as a tooltip, similar to the `title` attribute on an anchor tag.

_Default: 'Sparkline'_

### setValues(values: number[]): this

Sets the values used to generate the sparkline. These can also be provided in the constructor.

_Default: []_

### setViewBoxHeight(viewBoxHeight: number): this

Sets the height of the sparkline's view box. Not to be confused with `setHeight`. The sparkline will always stretch to fit the view box.

_Default: 100_

### setViewBoxWidth(viewBoxWidth: number): this

Sets the width of the sparkline's view box. Not to be confused with `setWidth`. The sparkline will always stretch to fit the view box.

_Default: 100_

### setWidth(width: string): this

Sets the width of the sparkline's SVG element. Not to be confused with `setViewBoxWidth`.

_Default: '100%'_

## Sponsor 💗

If you are a fan of this project, you may
[become a sponsor](https://github.com/sponsors/CharlesStover)
via GitHub's Sponsors Program.
