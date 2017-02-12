# SASS Material
Recently I've built several sites using the Material color palette.  Built this so I would only have to keep track of the color variants rather than hex codes, and if I wanted to lighten or darken anything, I could make the change just by changing '500' to '600' rather than going and looking up the HEX code in the design spec.

## Here's How To Use It
#### 1. Import the SCSS File
Import it into your project's main SCSS file as such:
```sass
@import '_sass-material';
```
I recommend it being the first file you import so you can use it in any of the other files you're importing.

#### 2. Usage
There is a function built into the file so you can access it easily.  Here is the syntax:
```sass
material-color(%color%, %variant%);
```
So, if you wanted to make your <p> text color purple -> 800
```sass
p {
  color: material-color(purple, 800);
}
```

If you just want the base color, for example not purple -> 800 but just purple (which is 500), no need to add the 500.  You can just do this and it will default to 500 unless you specify another variation.
```sass
material-color(purple);
```

Refer to the official Material Design Spec for colors and variations (https://material.io/guidelines/style/color.html#color-color-palette).  Note that white and black are defined just by:
```sass
material-color(white);
material-color(black);
```


For colors with multiple words associated with them, just hyphenate where the [space] would be.  Just make sure everything stays lowercase:
```sass
material-color(light-blue, 200);
```

Hope this helps you out!
