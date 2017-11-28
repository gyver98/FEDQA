# CSS Questions

#### What is the difference between classes and ID's in CSS?

*Not answered yet*

#### What's the difference between "resetting" and "normalizing" CSS? Which would you choose, and why?

<1>
- Resetting: Remove all the native styles provided by browsers
- Normalizing: Make the browser styles consistent

<2>
- Resetting: Removing all styling from every element - margins, padding, etc. All elements will have the same font-size, same line-height and no spacing. Eric Meyer's Reset is the most common approach: http://meyerweb.com/eric/tools/c... 
- Normalizing: Making elements render consistently across browsers.

<3>
It’s a short, often compressed (minified) set of CSS rules that resets the styling of all HTML elements to a consistent baseline.

Every browser has its own default ‘user agent’ stylesheet, that it uses to make unstyled websites appear more legible. For example, most browsers by default make links blue and visited links purple, give tables a certain amount of border and padding, apply variable font-sizes to H1, H2, H3 etc. and a certain amount of padding to almost everything.

Using a CSS Reset, CSS authors can force every browser to have all its styles reset to null, thus avoiding cross-browser differences as much as possible.

Source: http://www.cssreset.com/what-is-a-css-reset/

#### Describe Floats and how they work.

<1> There are `left`, `right` and `none` for `float`. Each value indicates how an
element should float. When `float` is set, each element will get out of its
normal flow and will be shifted to the specified direction, until it gets its
container or another floated element.


<2> It's a box that is pulled to the left or right and let the following content flow along its side.

They are still in the flow of the page, but whereas the elements used to be stacked vertically, now they're side by side. Very commonly used for things like navigations.

Has an annoying collapsing effect on the parent container. Fixed by clearing the float in the container.

<3>
When you float an element it becomes a block box. This box can then be shifted to the left or right on the current line. The markup options are “float: left”, “float: right” or “float: none”. A floated box is laid out according to the normal flow, then taken out of the flow and shifted to the left or right as far as possible. Content can flow down the right side of a left-floated box and down the left side of a right-floated box. You can also put several floats beside each other. If there isn’t enough horizontal room on the current line for the floated box, it will move downward, line by line, until a line has room for it. You should always set a width on floated items. If no width is set, the results can be unpredictable.

Elements following a floated element will wrap around the floated element. If you do not want this to occur, you can apply the “clear” property to these following elements. The four options are “clear: left”, “clear: right”, “clear: both” or “clear: none”.

Source: http://css.maxdesign.com.au/floatutorial/introduction.htm

#### Describe z-index and how stacking context is formed.

<1>
`z-index` tells how elements should be stacked in a screen. Stacking context
can be formed in several situations, but most famously, by a root element and
positioned elements. In each stacking context, `z-index` will be calculated
separately for its children and will stack the children in ascending order.

<2>
The z-index property in CSS controls the vertical stacking order of elements that overlap. As in, which one appears as if it is physically closer to you. z-index only effects elements that have a position value other than static (the default).

#### Describe BFC(Block Formatting Context) and how it works.

BFC is a part of rendering a webpage. It's used to determine from which
positioning and clearing should be done. The context is created by several
ways, but the most famously, by a root element, float, positioned elements.

#### What are the various clearing techniques and which is appropriate for what context?

```css
clear:both;
```

```css
overflow: hidden;
height: auto;
```

#### Explain CSS sprites, and how you would implement them on a page or site.

CSS sprite is combining multiple images into a merged one image and use CSS to
render each of them properly for each element.

It's usually implemented using `background: url(...) x-axis y-axis;`, or
both `background-image` and `background-position`.

#### What are your favourite image replacement techniques and which do you use when?

Image replacement technique is to replace a normal text element with an image.
There are many methods such as H5BP and Scott Kellum, as suggested [here](https://css-tricks.com/the-image-replacement-museum/).

My faviourite is H5BP, as it is the simplest and most intuitive one.

#### How would you approach fixing browser-specific styling issues?

http://www.smashingmagazine.com/2010/06/07/the-principles-of-cross-browser-css-coding/

<1>
Progressive enhancement enables us to establish a solid baseline of cross-browser support and then enhance the design with advanced CSS features for supportive browsers

<2>
Check features of HTML5 and CSS3 on caniuse.com to see what browser support there is for something new I want to use and avoid things that have sketchy support at this time.

Develop all of the views at the same time and test across browsers and operating systems as I go to avoid getting something that looks nice in my favorite browser, but breaks in other places that I then have to fix later with the potential of having to start from scratch.

Realize that we don’t have to make the display on every browser exactly identical as long as what we make looks good in each browser. Graceful degradation means that your design is able to fall back to a decent, but simplified, version of the layout rather than just looking broken in browsers that don’t support certain features of HTML or CSS.
Use BrowserStack for more intense cross-browser testing.


*Not answered yet*

#### How do you serve your pages for feature-constrained browsers?
###### What techniques/processes do you use?

*Not answered yet*

#### What are the different ways to visually hide content (and make it available only for screen readers)?

*Not answered yet*

#### Have you ever used a grid system, and if so, what do you prefer?

Yes, but not so many. I prefer Bootstrap.

#### Have you used or implemented media queries or mobile specific layouts/CSS?

Yes.

#### Are you familiar with styling SVG?

*Not answered yet*

#### How do you optimize your webpages for print?

```css
@media print {
  ...
}
```

#### What are some of the "gotchas" for writing efficient CSS?

Usually about CSS selectors.

- Avoid key selector for large numbers of elements
- Prefer class and ID selector to tag selector
- Avoid redundant selectors
- Care of batching

#### What are the advantages/disadvantages of using CSS preprocessors?
###### Describe what you like and dislike about the CSS preprocessors you have used.

*Not answered yet*

#### How would you implement a web design comp that uses non-standard fonts?

- `@font-face` to write my own `font-family`
- `@import` to import prepared web font(e.g. Google Webfonts)

#### Explain how a browser determines what elements match a CSS selector.

- Reads right-to-left
  - Check matching elements for the key(right-most) selector
  - Check if the elements are matching parents for the next selectors

#### Describe pseudo-elements and discuss what they are used for.

It's to style a part of an element, like `::first-letter` or `::before`.

They can be used to add a special symbol before a paragraph, change color of
first character of a line, etc.

#### Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models.

*Not answered yet*

#### What does ```* { box-sizing: border-box; }``` do? What are its advantages?

*Not answered yet*

#### List as many values for the display property that you can remember.

*Not answered yet*

#### What's the difference between inline and inline-block?

*Not answered yet*

#### What's the difference between a relative, fixed, absolute and statically positioned element?

*Not answered yet*

#### The 'C' in CSS stands for Cascading.  How is priority determined in assigning styles (a few examples)?  How can you use this system to your advantage?

CSS priority is determined by [specificity and inheritance](https://www.smashingmagazine.com/2010/04/css-specificity-and-inheritance/).

- Specificity: ID > class, psuedo-class > element, psudo-element
- Inheritence: specified value → computed value → used value → actual value

#### What existing CSS frameworks have you used locally, or in production? How would you change/improve them?

*Not answered yet*

#### Have you played around with the new CSS Flexbox or Grid specs?

Yes.

- http://flexboxfroggy.com
- https://scotch.io/tutorials/a-visual-guide-to-css3-flexbox-properties

#### How is responsive design different from adaptive design?

- Responsive: There is one basic layout, and it changes responsively to
  screen changes
- Adaptive: For each possible screen size, there is a distinct layout.

#### Have you ever worked with retina graphics? If so, when and what techniques did you use?

```css
@media (-webkit-min-device-pixel-ratio: 1.25), (min-resolution: 120dpi) {
  ...
}
```

#### Is there any reason you'd want to use `translate()` instead of *absolute positioning*, or vice-versa? And why?

*Not answered yet*
