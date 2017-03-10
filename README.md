# Fluid Vertical Rythym

A set of Sass mixins for creating fluid vertical ryhtm using the vw unit and calc.

## What is it?

Using the vw unit we can create `fluid typography`. This means we can scale the font size depending on the width of the browser. Fluid vr handles this with certain parameters when doing so to ensure we have control over the font size and the breakpoints in which it scales. On top of this we create a fluid baseline that scales with the font size to create a beautiful vertical rythm. 

## How to use it?

Fluid Vr needs some variables in order to work:

1. Minimum Font Size: The smallest you want the base font to scale to as a pixel value.

`$fv-min-fs: 14px;`

2. Maximum Font Size: The largest you want the base font to scale to as a pixel value.

`$fv-max-vw: 18px;`

3. Minimum View Width: The minimum browser width size to begin scaling the font from as a pixel value.

`$fv-min-vw: 320px`

4. Maximum View Width: The maximum browser width size from which the font will stop scaling as a pixel value.

`$fv-max-vw: 1200px`

5. Line Height: The chosen line height based on your design and font choices as a unitless value.

`$fv-line-height: 1.5`

6. Cap Height: The cap height of your chosen font as a unitless value. This value is used to help generate the baseline. It is worth taking the time to ensure this is correct.

`$fv-cap-height: 0.68;`

*After* you have declared your variables include `_fluid-vr.scss` in your project.

Use the `fluid-type` mixin on the html element to set the base to build your fluid rythym upon:

```
html {
    @include fluid-type();
}
```

On any elements you want to create a baseline for, use the `fluid-baseline` mixin. This takes in a font size in pixels and cap height ( if it differs to the base cap height ):

```
h1 {
    @include fluid-baseline(22px, 0.66);
}
```

Attach a margin bottom to elements to create vertical ryhtm among other elemements with the `fluid-mb` mixin: 

```
blockquote {
    @include fluid-mb;
}
```

To see full example see `example.scss`.

## To Do

- Write todos lol
