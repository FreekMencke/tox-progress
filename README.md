# ToxProgress
![test](https://thumbs.gfycat.com/LimpAmpleCuckoo-size_restricted.gif)
<center><a href="https://toxsickcoder.github.io/ToxProgress/index.html">Click here for the live version</a></center>

## Introduction

This library was made to easily create **animated radial progress bars**.

The goal of these animated radial progress bars is to add a stylized way to show numbers/statistics on your website.

## How to use

The way to include a **ToxProgressBar** to your website is to link the `tox-progress.js` and `tox-progress.css` files on your web page. You can then add a ToxProgressBar by using this tag:

``` javascript
<div class="tox-progress" data-size="180" data-thickness="12" data-color="#229922" data-background="#ffffff" data-progress="25" data-speed="500"></div>
```

The div needs to have the `class="tox-progress"`. This makes the div visible to the library. There also are a few properties we can see:
- **Size**: The diameter of the radial progress bar circle.
- **Thickness**: This is the thickness of the radial progress bar.
- **Color**: The foreground color. This is the color the radial progress bar will be.
- **Background**: The background color. This should to be the same color as your website. You can also use another color to create some interesting effects
- **Progress**: A number from 0-100 which marks the progress of the radial progress bar.
- **Speed**: The speed in ms in which the animation would do a full circle.

There is also the possibility to add content inside the radial progress bar. Add this div inside the `class="tox-progress"` div:

``` javascript
<div class="tox-progress" data-size="180" data-thickness="12" data-color="#229922" data-background="#ffffff" data-progress="25" data-speed="500">
     <div class="tox-progress-content" data-vcenter="true">
         //Add content here
     </div>
 </div>
 ```

So first add the `class="tox-progress-content"` to the div. If you want this content vertically centered add the `data-vcenter="true"` property. You can add any content you want in here.

Then include the following code on your website:

``` javascript
<script type="text/javascript">
    document.addEventListener('DOMContentLoaded', function () {
        ToxProgress.create();
        ToxProgress.animate();
    });
</script>
```

The `ToxProgress.create();` function generates everything needed. It has to be called before the `ToxProgress.animate();` function. The `ToxProgress.animate();` function can be called whenever you want.

If you want to reset the animation, call `ToxProgress.create();` before you call `ToxProgress.animate();` again.