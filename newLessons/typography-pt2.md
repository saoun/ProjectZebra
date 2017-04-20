# Typography pt 2

 - CSS lesson

## What We'll cover

 - importing custom fonts
 - indenting the first line of a paragraph

*****
 #### Importing Custom fonts
*****

Using the paragraphs and code from the last example (Basic Typography), let's open our JS Fiddle up again. https://jsfiddle.net/

Sometimes you'll want a non-standard font or a really beautiful font found on the internet. There are a lot of places to get free fronts from. Here's a couple:

1. Google Fonts https://fonts.google.com/
2. Adobe Fonts https://edgewebfonts.adobe.com/fonts#/?collection=abril-fatface

Let's go to Google Fonts and import the `Roboto` font into our JS fiddle.

When you find it, click on the red `+` symbol and open up the popup that appears.

They should give you two lines of code:

HTML:
```HTML

<link href="https://fonts.googleapis.com/css?family=Roboto" rel="stylesheet">

```

and

CSS"
```
font-family: 'Roboto', sans-serif;
```

The easiest way you load a custom font onto your website is to use a `<link>` tag inside of our `<html>` to download it directly to your browser each time you visit.

If you paste the `HTML` inside the JSFIDDLE, it won't work (this is JSFIDDLE's fault). Fortunately, there's a [second way](http://stackoverflow.com/questions/26717116/how-to-include-google-font-in-jsfiddle) to import a custom font by using CSS.

CSS:
```css
@import url(//https://fonts.googleapis.com/css?family=Roboto);
```
- Make note that both methods use the same URL `https://fonts.googleapis.com/css?family=Roboto` but wrap it in a different method.

- Put this line at the very top of your CSS file.

Next, replace the old `font-family` line with the new one given to you by Google and click `RUN`

How does it look? Try to change `sans-serif` to `serif`, `monospace`, or `fantasy`. Try adjusting the `font-weight`. Try finding another google font and importing it!

*****
 #### Making paragraph indentation
*****

Paragraph indentation is very easy, but it's not very obvious how you do it. You can't just press the `tab` key and expect it to work. Luckily, there's a specific line of code for us to use called `text-indent`.

Add this line to your `p` in CSS:

```css
text-indent: 40px;
```
