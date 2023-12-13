# ICM: Image Compare module


## Description

Light Vanilla Javascript library (8kb minified) to compare multiples images with
sliders. Also, you can add text and filters to your images.

## Installation

And import it to your project.

```html
<link rel="stylesheet" href="icm.min.css">
<script src="icm.min.js"></script>
```

## Usage

You only have to create a container and add your images. You can add all
images you want!! If you add the `alt` attribute, you will view the text
in the image comparison.

```html
<div class="icm">
    <img src="01.jpg">
    <img src="02.jpg" alt="Japan Yellow">
    <img src="03.jpg" alt="Japan Orange">
    <img src="04.jpg" alt="Japan Black & White">
</div>
```

Finally, you need to initialize the component like this.

```javascript
new Dics({
    container: document.querySelector('.icm')
});
```

Or this.

```javascript
new Dics({
    container: document.querySelectorAll('.icm'),
    linesOrientation: 'vertical',
    textPosition: 'left',
    arrayBackgroundColorText: ['#000000', '#FFFFFF'],
    arrayColorText: ['#FFFFFF', '#000000'],
    linesColor: 'rgb(0,0,0)'
});
```

## Options

If you want you can include different options.

| Option | Description | Example |
| --- | --- | --- |
| container | **REQUIRED**: HTML container | `document.querySelector('.icm')` |
| filters | Array of CSS string filters  |`['blur(3px)', 'grayscale(1)', 'sepia(1)', 'saturate(3)']` |
| hideTexts | Show text only when you hover the image container |`true`,`false`|
| textPosition | Set the prefer text position  |`'center'`,`'top'`, `'right'`, `'bottom'`, `'left'` |
| linesOrientation | Change the orientation of lines  |`'horizontal'`,`'vertical'` |
| rotate | Rotate the image container (not too useful but it's a beatiful effect. String of rotate CSS rule)  |`'45deg'`|
| arrayBackgroundColorText | Change the bacground-color of sections texts with an array |`['#000000', '#FFFFFF']`|
| arrayColorText | Change the color of texts with an array  |`['#FFFFFF', '#000000']`|
| linesColor | Change the lines and arrows color  |`'rgb(0,0,0)'`|
