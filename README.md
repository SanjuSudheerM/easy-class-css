
## Style Structures & Pre-defined Classes

This is some set of mixins can be added on top of Bootstrap 4 to fasten the development by generating required utility classes by configuration on the fly.

The custom mixins are included in the `global.scss` file under `src/styles/core` directory, `core` has all the styles which are very generic to all the applications (feel free to add more styles if you feel that is necessary for your fast development). `theme` folder has a file `variable.scss` which is the configuration for all custom mixin.
`override.scss` & `responsiveness.scss` are free to use as per the requirement in the project.
We are suggesting to avoid component level styles to make the styles more organizable also to have a single point change.

## mixins
#### font-size:
To convert any pixel value to rem <br>
`Usage: font-size: font-size(20)` 
<br>
<br>
#### color-weight-generator:
Generating the 4 lighter & 4 darker version of the given color & generating classes in the following format<br>
`{given-color-name}-{weight}`<br>
`example - .primary-300`
<br>
<br>

#### color-weight:
Same as `color-weight-generator` but this one can be used inside other classed to handle different state or to set different property. (color weight out of 10)<br>
example: <br>
`@include color-weight(red, 7, background-color)`
<br>
<br>

#### typography-generator:
A basic typography generator. This is creating 6 classes with different font-size pair.<br>
Class names are `.main-title`, `.main-title-description`,`.sub-title`, `.sub-title-description`, `.normal-text`, `.small-text` <br>
All of these are generated based on the `$base-font` variable in `variable.scss` file.
<br>
<br>

#### frequent-color-class:
To generate required font-color classes. For this, configure the `$frequent-font-colors` variables in `varibles.scss` file.<br>
the generated class names are like <br>
`.custom-{name}-{property}`
`$frequent-background-colors: (white: #ffffff, black:#000000);`<br>
`custom-white-color` for font color
<br>
<br>
