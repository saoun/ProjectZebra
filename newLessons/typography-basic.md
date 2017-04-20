# Basic Typography
 - CSS lesson

## What we'll cover

 - Styling font really good


[Butterick's Practical Typography](http://practicaltypography.com/) has a ton of amazing advice on typography topics.

I'll use some page-layout and text-styling guidelines from the book to demonstrate how to style your text with CSS.

Specifically we'll cover:

- Fonts
- Line height & spacing
- How to center the text body & align the text
- text decorations

Please open up a JS Fiddle to follow along.
https://jsfiddle.net/

First, let's copy some HTML containing a title and 2 paragraphs into the fiddle and click "run" each time we make a change.

(this text was written with [cat ipsum](http://www.catipsum.com/) by the way)

```html
<h1>Friends are not food</h1>

<p>Purr when being pet go into a room to decide you didn't want to be in there anyway kick up litter chase after silly colored fish toys around the house
Cat slap dog in face hide at bottom of staircase to trip human so refuse to leave cardboard box but purr while eating purr when being pet, yet hola te quiero. Stand in front of the computer screen demand to be let outside at once, and expect owner to wait for me as i think about it kitty poochy friends are not food. Find something else more interesting i cry and cry and cry unless you pet me, and then maybe i cry just for fun sit in window and stare ooo, a bird! yum.</p>

<p>Stare at ceiling chase dog then run away but has closed eyes but still sees you so use lap as chair. Run outside as soon as door open lick butt, hola te quiero scratch the postman wake up lick paw wake up owner meow meow. When in doubt, wash meow but purr when being pet, or eat grass, throw it back up. Pelt around the house and up and down stairs chasing phantoms. Thinking longingly about tuna brine sit by the fire i cry and cry and cry unless you pet me, and then maybe i cry just for fun and find a way to fit in tiny box. Roll over and sun my belly. Meow meow, i tell my human stare at ceiling, for licks your face. Licks your face pose purrfectly to show my beauty. Find a way to fit in tiny box stare at the wall, play with food and get confused by dust, friends are not food.</p>
```

Looks pretty bad, right? Everything is squished together and the text stretches from one end of the window to the next.

### Font Size & Line spacing
According Buttericks, we should style the body text first before anything else. So let's choose a font (scary!), size it, and adjust the line spacing.

##### font-family { }
"Helvetica Neue" is probably the most popular font on the internet. So let's start with this.

`font-family` lets you add several fonts as backups in case the user's computer doesn't have the first one installed. Make sure to have a backup or else it will default to the mortifyingly ugly `Times New Roman`.

According to [this blog](http://www.georgejaros.com/content/tutorials/font_tutorial/index.html), the safest web fonts are `Times`, `Helvetica`, `Arial`, `Verdana`, and `Courier New` because everyone has them installed.

The last part of `font-family` lets you specify the font type such as `serif`, `sans-serif`, and `monospace` among others. This usually only works with custom fonts.

```CSS
p {
  font-family: "Helvetica Neue", "Helvetica", "Arial", sans-serif;
}
```

##### font-size { }
According to Butterick's guide, [website font size](http://practicaltypography.com/point-size.html) for body text is ideally between 15-25px. However, it's important to note that two different fonts with the same `font-size` may end up with different sized *paragraphs* because of other factors such as `letter-spacing` and `font-kerning`, which is a bit too obscure to cover here.

```CSS
p {
  font-family: "Helvetica Neue", "Helvetica", "Arial", sans-serif;
  font-size: 22px;
}
```

##### line-height { }

Again according to Butterick's, [the ideal line spacing](http://practicaltypography.com/line-spacing.html) for body text is around 120-145%. This is the whitespace in between each line. Setting it to 200% is equal to double-spacing.

With CSS, we use the `line-height` property to set the spacing.

```CSS
p {
  font-family: "Helvetica Neue", "Helvetica", "Arial", sans-serif;
  line-height: 140%;
}
```

##### font-weight { }

Finally, a very popular font style on the internet is very *thin* Helvetica font. You can set the width of the font with `font-weight`. This takes a number from 100 to 800. 200 is a good *thin* size, 300 is normal, 600 is **bold**. Not all fonts come with a full range of weights, but `Helvetica Neue` does!

```CSS

p {
  font-family: "Helvetica Neue", "Helvetica", "Arial", serif;
  font-size: 22px;
  line-height: 140%;
  font-weight: 200;
}

```

Apply these styles to your CSS box in the jsfiddle and click "run".

What a difference!

### Centering and Aligning the text

So, Buttericks (you're sick of this name aren't you?) has a [very precise](http://practicaltypography.com/line-length.html) recommendation for how wide your text bodies should be and where they should be.

Obviously, we want the text to be in the center of the page, aligned to the left, and not touching the edges of the window.

##### Setting the width

I personally find that a `max-width` of `500-700px` looks very nice for most body text (and gets you very close to Butterick's recommendation of 45-90 characters per line).

```CSS
p {
  font-family: "Helvetica Neue", "Helvetica", "Arial", serif;
  font-weight: 200;
  font-size: 22px;
  line-height: 140%;
  max-width: 600px;
}
```

##### Centering it

But the text is not centered. To do this, we're going to use the `margin` and a very cool centering trick.

As you may know, `margin` can be broken down into `margin-top`, `margin-left`, etc. If you leave it as just `margin`, though, you can put two numbers in there and apply those values to both `top and bottom`, and `left and right` like so:

`margin: 20px 200px;` (20px top and bottom, 200 left and right)

If we use a special value called `auto`, it will automatically calculate and evenly divide the space among both sides - thus centering the text.

We also need to add some space between the paragraphs, so let's add about `20px` to the `top and bottom` to space them out.

```CSS
p {
  font-family: "Helvetica Neue", "Helvetica", "Arial", serif;
  font-weight: 200;
  font-size: 22px;
  line-height: 140%;
  max-width: 600px;
  margin: 20px auto;
}
```
Try resizing the JSFIDDLE when you add this and see for yourself how it automatically stays centered!

##### Aligning the text

Just like in MSWord or any other writing software, you can align the text to the `left`, `center`, `right`, or `justify` it. Let's keep the paragraphs aligned to the left (they are by default) and just center the header.

```CSS
h1 {
  text-align: center
}
```

##### Text Decoration

Sometimes, you want your text to be `bold`, `italics`, `underline`, or have a `line-through`.

Let's add an underline to the title.

```CSS
h1 {
  text-align: center;
  text-decoration: underline;
}
```

Style the header some more with some of the tricks you learned!


###### Full code:

```CSS
p {
  font-family: "Helvetica Neue", "Helvetica", "Arial", serif;
  font-weight: 200;
  font-size: 22px;
  line-height: 140%;
  max-width: 600px;
  margin: 20px auto;
}

h1 {
  text-align: center;
  text-decoration: underline;
}
```
