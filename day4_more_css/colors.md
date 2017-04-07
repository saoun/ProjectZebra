# Colors

There is more than one way to add color to something.

1. You can color something with color names

```css
body {
    background: green;
}

```

2. You can color something with HEX values
    - HEX values are a code that translates into a color
    - They all start with a #
    - Then the next 2 numbers decide how much RED
    - The next 2 decide how much GREEN to mix in
    - The next 2 decide how much BLUE to mix in
    - Use a tool like http://htmlcolorcodes.com/ to help you

3. Finally, you can use RGBA to color something.
    - Stands for RED, GREEN, BLUE, and ALPHA (or opacity)
    - Each value goes from 0-255 except for ALPHA which is 0-1
    - Allows you to make see-through colors.

These are all the same blue color:
```css
body {
    background: blue;
    background: #0000FF;
    background: rgba(0,0,255,1)
}
```


Open up JS fiddle and play with coloring the body (entire background)!
https://jsfiddle.net/