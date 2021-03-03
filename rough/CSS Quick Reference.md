<!-- css quick reference -->
# CSS Quick Reference
## Styles
On when printing
```css
@media print{
    div {
        display: none;
    }
}
```
Center non-text (e.g. in `div`):
```css
    div {
        display: block;
        margin: auto;
    }
```
Center text (e.g. in `div`):
```css
    div {
        text-align: center;
    }
```
## Selectors
Everything after an element (e.g. `div`)
```css
    div ~ * {
        color: auto;
    }
```
All elements of type after (sibling of) another e.g. `div`s of `article`:
```css
  article > div {
    color: auto;
  }
```
## Syntax
```
selector {
    property: value;
    property2: value2;
}
```
## Include external css file
```
<link rel="stylesheet" type="text/css" href="/style.css" />
```
#### Internal styles
```
<style type="text/css">
    div { color: #444;}
</style>
```
#### Inline styles
```
<tag style="property: value"> </tag>
```
<div id="grid"
	style="width=100%;display:grid;
		grid-template-columns:min-content 100%">
<div style="margin:0 1em;white-space: nowrap;"><code>*</code></div><div style="margin:0 1em;white-space: nowrap;">all elements</div>
<div style="margin:0 1em;white-space: nowrap;"><code>div</code></div><div style="margin:0 1em;white-space: nowrap;">all div tags</div>
<div style="margin:0 1em;white-space: nowrap;"><code>div,p</code></div><div style="margin:0 1em;white-space: nowrap;">all divs and paragraphs</div>
<div style="margin:0 1em;white-space: nowrap;"><code>div p</code></div><div style="margin:0 1em;white-space: nowrap;">paragraphs inside divs</div>
<div style="margin:0 1em;white-space: nowrap;"><code>div > p</code></div><div style="margin:0 1em;white-space: nowrap;">all p tags, one level deep in div</div>
<div style="margin:0 1em;white-space: nowrap;"><code>div + p</code></div><div style="margin:0 1em;white-space: nowrap;">p tags immediately after div</div>
<div style="margin:0 1em;white-space: nowrap;"><code>div ~ p</code></div><div style="margin:0 1em;white-space: nowrap;">p tags preceded by div</div>
<div style="margin:0 1em;white-space: nowrap;"><code>.classname</code></div><div style="margin:0 1em;white-space: nowrap;">all elements with class</div>
<div style="margin:0 1em;white-space: nowrap;"><code>#idname</code></div><div style="margin:0 1em;white-space: nowrap;">element with ID</div>
<div style="margin:0 1em;white-space: nowrap;"><code>div.classname</code></div><div style="margin:0 1em;white-space: nowrap;">divs with certain classname</div>
<div style="margin:0 1em;white-space: nowrap;"><code>div#idname</code></div><div style="margin:0 1em;white-space: nowrap;">div with certain ID</div>
<div style="margin:0 1em;white-space: nowrap;"><code>#idname *</code></div><div style="margin:0 1em;white-space: nowrap;">all elements inside #idname</div>
<div style="margin:0 1em;white-space: nowrap;grid-column:span 2;">Pseudo Classes</div>
<div style="margin:0 1em;white-space: nowrap;"><code>a:link</code></div><div style="margin:0 1em;white-space: nowrap;">link in normal state</div>
<div style="margin:0 1em;white-space: nowrap;"><code>a:active</code></div><div style="margin:0 1em;white-space: nowrap;">link in clicked state</div>
<div style="margin:0 1em;white-space: nowrap;"><code>a:hover</code></div><div style="margin:0 1em;white-space: nowrap;">link with mouse over it</div>
<div style="margin:0 1em;white-space: nowrap;"><code>a:visited</code></div><div style="margin:0 1em;white-space: nowrap;">visited link</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p::after{content:"yo";}</code></div><div style="margin:0 1em;white-space: nowrap;">add content after p</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p::before</code></div><div style="margin:0 1em;white-space: nowrap;">add content before p</div>
<div style="margin:0 1em;white-space: nowrap;"><code>input:checked</code></div><div style="margin:0 1em;white-space: nowrap;">checked inputs</div>
<div style="margin:0 1em;white-space: nowrap;"><code>input:disabled</code></div><div style="margin:0 1em;white-space: nowrap;">disabled inputs</div>
<div style="margin:0 1em;white-space: nowrap;"><code>input:enabled</code></div><div style="margin:0 1em;white-space: nowrap;">enabled inputs</div>
<div style="margin:0 1em;white-space: nowrap;"><code>input:focus</code></div><div style="margin:0 1em;white-space: nowrap;">input has focus</div>
<div style="margin:0 1em;white-space: nowrap;"><code>input:in-range</code></div><div style="margin:0 1em;white-space: nowrap;">value in range</div>
<div style="margin:0 1em;white-space: nowrap;"><code>input:out-of-range</code></div><div style="margin:0 1em;white-space: nowrap;">input value out of range</div>
<div style="margin:0 1em;white-space: nowrap;"><code>input:valid</code></div><div style="margin:0 1em;white-space: nowrap;">input with valid value</div>
<div style="margin:0 1em;white-space: nowrap;"><code>input:invalid</code></div><div style="margin:0 1em;white-space: nowrap;">input with invalid value</div>
<div style="margin:0 1em;white-space: nowrap;"><code>input:optional</code></div><div style="margin:0 1em;white-space: nowrap;">no required attribute</div>
<div style="margin:0 1em;white-space: nowrap;"><code>input:required</code></div><div style="margin:0 1em;white-space: nowrap;">input with requred attribute</div>
<div style="margin:0 1em;white-space: nowrap;"><code>input:read-only</code></div><div style="margin:0 1em;white-space: nowrap;">with readonly attribute</div>
<div style="margin:0 1em;white-space: nowrap;"><code>input:read-write</code></div><div style="margin:0 1em;white-space: nowrap;">no readonly attrib.</div>
<div style="margin:0 1em;white-space: nowrap;"><code>div:empty</code></div><div style="margin:0 1em;white-space: nowrap;">element with no children</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p::first-letter</code></div><div style="margin:0 1em;white-space: nowrap;">first letter in p</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p::first-line</code></div><div style="margin:0 1em;white-space: nowrap;">first line in p</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p:first-of-type</code></div><div style="margin:0 1em;white-space: nowrap;">first of some type</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p:last-of-type</code></div><div style="margin:0 1em;white-space: nowrap;">last of some type</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p:lang(en)</code></div><div style="margin:0 1em;white-space: nowrap;">p with en language attribute</div>
<div style="margin:0 1em;white-space: nowrap;"><code>:not(span)</code></div><div style="margin:0 1em;white-space: nowrap;">element that's not a span</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p:first-child</code></div><div style="margin:0 1em;white-space: nowrap;">first child of its parent</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p:last-child</code></div><div style="margin:0 1em;white-space: nowrap;">last child of its parent</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p:nth-child(2)</code></div><div style="margin:0 1em;white-space: nowrap;">second child of its parent</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p:nth-child(3n+1)</code></div><div style="margin:0 1em;white-space: nowrap;">nth-child (an + b) formula</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p:nth-last-child(2)</code></div><div style="margin:0 1em;white-space: nowrap;">second child from behind</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p:nth-of-type(2)</code></div><div style="margin:0 1em;white-space: nowrap;">second p of its parent</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p:nth-last-of-type(2)</code></div><div style="margin:0 1em;white-space: nowrap;">...from behind</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p:only-of-type</code></div><div style="margin:0 1em;white-space: nowrap;">unique of its parent</div>
<div style="margin:0 1em;white-space: nowrap;"><code>p:only-child</code></div><div style="margin:0 1em;white-space: nowrap;">only child of its parent</div>
<div style="margin:0 1em;white-space: nowrap;"><code>:root</code></div><div style="margin:0 1em;white-space: nowrap;">documents root element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>::selection</code></div><div style="margin:0 1em;white-space: nowrap;">portion selected by user</div>
<div style="margin:0 1em;white-space: nowrap;"><code>:target</code></div><div style="margin:0 1em;white-space: nowrap;">highlight active anchor</div>
<div style="margin:0 1em;white-space: nowrap;grid-column:span 2;">Attribute Selectors</div>
<div style="margin:0 1em;white-space: nowrap;"><code>a[target]</code></div><div style="margin:0 1em;white-space: nowrap;">links with a target attribute</div>
<div style="margin:0 1em;white-space: nowrap;"><code>a[target="_blank"]</code></div><div style="margin:0 1em;white-space: nowrap;">links which open in new tab</div>
<div style="margin:0 1em;white-space: nowrap;"><code>[title~="chair"]</code></div><div style="margin:0 1em;white-space: nowrap;">title element containing a word</div>
<div style="margin:0 1em;white-space: nowrap;"><code>[class^="chair"]</code></div><div style="margin:0 1em;white-space: nowrap;">class starts with chair</div>
<div style="margin:0 1em;white-space: nowrap;"><code>[class|="chair"]</code></div><div style="margin:0 1em;white-space: nowrap;">class starts with the chair word</div>
<div style="margin:0 1em;white-space: nowrap;"><code>[class*="chair"]</code></div><div style="margin:0 1em;white-space: nowrap;">class contains chair</div>
<div style="margin:0 1em;white-space: nowrap;"><code>[class$="chair"]</code></div><div style="margin:0 1em;white-space: nowrap;">class ends with chair</div>
<div style="margin:0 1em;white-space: nowrap;"><code>input[type="button"]</code></div><div style="margin:0 1em;white-space: nowrap;">specified input type</div>
</div>

### Properties
<div id="grid"
	style="width=100%;display:grid;
		grid-template-columns:min-content 100%">
<div style="margin:0 1em;white-space: nowrap;"><code>align-content</code></div><div style="margin:0 1em;white-space: nowrap;">behavior of the flex-wrap property</div>
<div style="margin:0 1em;white-space: nowrap;"><code>align-items</code></div><div style="margin:0 1em;white-space: nowrap;">alignment for items inside the container</div>
<div style="margin:0 1em;white-space: nowrap;"><code>align-self</code></div><div style="margin:0 1em;white-space: nowrap;">alignment for the selected item</div>
<div style="margin:0 1em;white-space: nowrap;"><code>all</code></div><div style="margin:0 1em;white-space: nowrap;">changes all properties</div>
<div style="margin:0 1em;white-space: nowrap;"><code>animation</code></div><div style="margin:0 1em;white-space: nowrap;">binds an animation to an element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>animation-delay</code></div><div style="margin:0 1em;white-space: nowrap;">delays animation start</div>
<div style="margin:0 1em;white-space: nowrap;"><code>animation-direction</code></div><div style="margin:0 1em;white-space: nowrap;">reverse animation or in alternate cycles</div>
<div style="margin:0 1em;white-space: nowrap;"><code>animation-duration</code></div><div style="margin:0 1em;white-space: nowrap;">animation duration in seconds or ms</div>
<div style="margin:0 1em;white-space: nowrap;"><code>animation-fill-mode</code></div><div style="margin:0 1em;white-space: nowrap;">style when the animation is not playing</div>
<div style="margin:0 1em;white-space: nowrap;"><code>animation-iteration-count</code></div><div style="margin:0 1em;white-space: nowrap;">number of an animation replays</div>
<div style="margin:0 1em;white-space: nowrap;"><code>animation-name</code></div><div style="margin:0 1em;white-space: nowrap;">name for the @keyframes animation</div>
<div style="margin:0 1em;white-space: nowrap;"><code>animation-play-state</code></div><div style="margin:0 1em;white-space: nowrap;">the animation is running or paused</div>
<div style="margin:0 1em;white-space: nowrap;"><code>animation-timing-function</code></div><div style="margin:0 1em;white-space: nowrap;">speed curve of an animation</div>
<div style="margin:0 1em;white-space: nowrap;"><code>backface-visibility</code></div><div style="margin:0 1em;white-space: nowrap;">is element visible when not facing the screen</div>
<div style="margin:0 1em;white-space: nowrap;"><code>background</code></div><div style="margin:0 1em;white-space: nowrap;">all background properties in one declaration</div>
<div style="margin:0 1em;white-space: nowrap;"><code>background-attachment</code></div><div style="margin:0 1em;white-space: nowrap;">is the background image fixed or scrolls</div>
<div style="margin:0 1em;white-space: nowrap;"><code>background-blend-mode</code></div><div style="margin:0 1em;white-space: nowrap;">blending mode of each background layer</div>
<div style="margin:0 1em;white-space: nowrap;"><code>background-clip</code></div><div style="margin:0 1em;white-space: nowrap;">painting area of the background</div>
<div style="margin:0 1em;white-space: nowrap;"><code>background-color</code></div><div style="margin:0 1em;white-space: nowrap;">background color</div>
<div style="margin:0 1em;white-space: nowrap;"><code>background-image</code></div><div style="margin:0 1em;white-space: nowrap;">background image</div>
<div style="margin:0 1em;white-space: nowrap;"><code>background-origin</code></div><div style="margin:0 1em;white-space: nowrap;">where the background image is positioned</div>
<div style="margin:0 1em;white-space: nowrap;"><code>background-position</code></div><div style="margin:0 1em;white-space: nowrap;">starting position of the background image</div>
<div style="margin:0 1em;white-space: nowrap;"><code>background-repeat</code></div><div style="margin:0 1em;white-space: nowrap;">the way the background image is repeated</div>
<div style="margin:0 1em;white-space: nowrap;"><code>background-size</code></div><div style="margin:0 1em;white-space: nowrap;">background image size</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border</code></div><div style="margin:0 1em;white-space: nowrap;">sets all border properties in one line</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-bottom</code></div><div style="margin:0 1em;white-space: nowrap;">bottom border properties in one line</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-bottom-color</code></div><div style="margin:0 1em;white-space: nowrap;">color of the bottom border</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-bottom-left-radius</code></div><div style="margin:0 1em;white-space: nowrap;">border bottom left radius</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-bottom-right-radius</code></div><div style="margin:0 1em;white-space: nowrap;">border bottom right radius</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-bottom-style</code></div><div style="margin:0 1em;white-space: nowrap;">border bottom style</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-bottom-width</code></div><div style="margin:0 1em;white-space: nowrap;">border bottom width</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-collapse</code></div><div style="margin:0 1em;white-space: nowrap;">border collapse</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-color</code></div><div style="margin:0 1em;white-space: nowrap;">border color</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-image</code></div><div style="margin:0 1em;white-space: nowrap;">sets an image as border</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-image-outset</code></div><div style="margin:0 1em;white-space: nowrap;">border image area extends beyond the border box</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-image-repeat</code></div><div style="margin:0 1em;white-space: nowrap;">border image repeated, rounded or stretched</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-image-slice</code></div><div style="margin:0 1em;white-space: nowrap;">how to slice the border image</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-image-source</code></div><div style="margin:0 1em;white-space: nowrap;">path to the border image</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-image-width</code></div><div style="margin:0 1em;white-space: nowrap;">border image width</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-left</code></div><div style="margin:0 1em;white-space: nowrap;">left border properties in one line</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-left-color</code></div><div style="margin:0 1em;white-space: nowrap;">border left color</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-left-style</code></div><div style="margin:0 1em;white-space: nowrap;">border left style</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-left-width</code></div><div style="margin:0 1em;white-space: nowrap;">border left width</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-radius</code></div><div style="margin:0 1em;white-space: nowrap;">border radius of the four rounded corners</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-right</code></div><div style="margin:0 1em;white-space: nowrap;">right border properties in one line</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-right-color</code></div><div style="margin:0 1em;white-space: nowrap;">border right color</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-right-style</code></div><div style="margin:0 1em;white-space: nowrap;">border right style</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-right-width</code></div><div style="margin:0 1em;white-space: nowrap;">border right width</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-spacing</code></div><div style="margin:0 1em;white-space: nowrap;">border spacing</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-style</code></div><div style="margin:0 1em;white-space: nowrap;">border style</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-top</code></div><div style="margin:0 1em;white-space: nowrap;">top border properties in one line</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-top-color</code></div><div style="margin:0 1em;white-space: nowrap;">border top color</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-top-left-radius</code></div><div style="margin:0 1em;white-space: nowrap;">border top left radius</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-top-right-radius</code></div><div style="margin:0 1em;white-space: nowrap;">border top right radius</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-top-style</code></div><div style="margin:0 1em;white-space: nowrap;">border top style</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-top-width</code></div><div style="margin:0 1em;white-space: nowrap;">border top width</div>
<div style="margin:0 1em;white-space: nowrap;"><code>border-width</code></div><div style="margin:0 1em;white-space: nowrap;">border width</div>
<div style="margin:0 1em;white-space: nowrap;"><code>bottom</code></div><div style="margin:0 1em;white-space: nowrap;">bottom offset for relative and absolute elements</div>
<div style="margin:0 1em;white-space: nowrap;"><code>box-shadow</code></div><div style="margin:0 1em;white-space: nowrap;">shadow to element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>box-sizing</code></div><div style="margin:0 1em;white-space: nowrap;">box sizing properties</div>
<div style="margin:0 1em;white-space: nowrap;"><code>caption-side</code></div><div style="margin:0 1em;white-space: nowrap;">placement of a table caption</div>
<div style="margin:0 1em;white-space: nowrap;"><code>clear</code></div><div style="margin:0 1em;white-space: nowrap;">deny floating of an element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>clip</code></div><div style="margin:0 1em;white-space: nowrap;">clip an absolutely positioned element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>color</code></div><div style="margin:0 1em;white-space: nowrap;">text color</div>
<div style="margin:0 1em;white-space: nowrap;"><code>column-count</code></div><div style="margin:0 1em;white-space: nowrap;">divide the content in columns</div>
<div style="margin:0 1em;white-space: nowrap;"><code>column-fill</code></div><div style="margin:0 1em;white-space: nowrap;">balanced fill or not</div>
<div style="margin:0 1em;white-space: nowrap;"><code>column-gap</code></div><div style="margin:0 1em;white-space: nowrap;">gap between the columns</div>
<div style="margin:0 1em;white-space: nowrap;"><code>column-rule</code></div><div style="margin:0 1em;white-space: nowrap;">separator between columns, like border</div>
<div style="margin:0 1em;white-space: nowrap;"><code>column-rule-color</code></div><div style="margin:0 1em;white-space: nowrap;">column rule color</div>
<div style="margin:0 1em;white-space: nowrap;"><code>column-rule-style</code></div><div style="margin:0 1em;white-space: nowrap;">column rule style</div>
<div style="margin:0 1em;white-space: nowrap;"><code>column-rule-width</code></div><div style="margin:0 1em;white-space: nowrap;">column rule width</div>
<div style="margin:0 1em;white-space: nowrap;"><code>column-span</code></div><div style="margin:0 1em;white-space: nowrap;">column span</div>
<div style="margin:0 1em;white-space: nowrap;"><code>column-width</code></div><div style="margin:0 1em;white-space: nowrap;">column width</div>
<div style="margin:0 1em;white-space: nowrap;"><code>columns</code></div><div style="margin:0 1em;white-space: nowrap;">set column-width and column-count</div>
<div style="margin:0 1em;white-space: nowrap;"><code>content</code></div><div style="margin:0 1em;white-space: nowrap;">insert content :before and :after elements</div>
<div style="margin:0 1em;white-space: nowrap;"><code>counter-increment</code></div><div style="margin:0 1em;white-space: nowrap;">count sections</div>
<div style="margin:0 1em;white-space: nowrap;"><code>counter-reset</code></div><div style="margin:0 1em;white-space: nowrap;">reset counter</div>
<div style="margin:0 1em;white-space: nowrap;"><code>cursor</code></div><div style="margin:0 1em;white-space: nowrap;">cursor type when element is hovered</div>
<div style="margin:0 1em;white-space: nowrap;"><code>direction</code></div><div style="margin:0 1em;white-space: nowrap;">writing direction, Arabic is using rtl</div>
<div style="margin:0 1em;white-space: nowrap;"><code>display</code></div><div style="margin:0 1em;white-space: nowrap;">box display type</div>
<div style="margin:0 1em;white-space: nowrap;"><code>empty-cells</code></div><div style="margin:0 1em;white-space: nowrap;">hide borders and background on empty table cells</div>
<div style="margin:0 1em;white-space: nowrap;"><code>filter</code></div><div style="margin:0 1em;white-space: nowrap;">image effects: grayscale, blur, invert etc.</div>
<div style="margin:0 1em;white-space: nowrap;"><code>flex</code></div><div style="margin:0 1em;white-space: nowrap;">item length, relative to others inside the container</div>
<div style="margin:0 1em;white-space: nowrap;"><code>flex-basis</code></div><div style="margin:0 1em;white-space: nowrap;">initial length of a flexible item</div>
<div style="margin:0 1em;white-space: nowrap;"><code>flex-direction</code></div><div style="margin:0 1em;white-space: nowrap;">direction of the flexible items</div>
<div style="margin:0 1em;white-space: nowrap;"><code>flex-flow</code></div><div style="margin:0 1em;white-space: nowrap;">shorthand for flex-direction and flex-wrap</div>
<div style="margin:0 1em;white-space: nowrap;"><code>flex-grow</code></div><div style="margin:0 1em;white-space: nowrap;">how much the item will grow relative other items</div>
<div style="margin:0 1em;white-space: nowrap;"><code>flex-shrink</code></div><div style="margin:0 1em;white-space: nowrap;">how to shrink the item relative to other items</div>
<div style="margin:0 1em;white-space: nowrap;"><code>flex-wrap</code></div><div style="margin:0 1em;white-space: nowrap;">wrap flexible items</div>
<div style="margin:0 1em;white-space: nowrap;"><code>float</code></div><div style="margin:0 1em;white-space: nowrap;">float elements left or right</div>
<div style="margin:0 1em;white-space: nowrap;"><code>font</code></div><div style="margin:0 1em;white-space: nowrap;">all font properties in one line</div>
<div style="margin:0 1em;white-space: nowrap;"><code>@font-face</code></div><div style="margin:0 1em;white-space: nowrap;">declare non-web-safe fonts</div>
<div style="margin:0 1em;white-space: nowrap;"><code>font-family</code></div><div style="margin:0 1em;white-space: nowrap;">font of the element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>font-size</code></div><div style="margin:0 1em;white-space: nowrap;">font size</div>
<div style="margin:0 1em;white-space: nowrap;"><code>font-size-adjust</code></div><div style="margin:0 1em;white-space: nowrap;">control font size if the first declared option is not available</div>
<div style="margin:0 1em;white-space: nowrap;"><code>font-stretch</code></div><div style="margin:0 1em;white-space: nowrap;">widen or narrow text</div>
<div style="margin:0 1em;white-space: nowrap;"><code>font-style</code></div><div style="margin:0 1em;white-space: nowrap;">font style: normal, italic, oblique</div>
<div style="margin:0 1em;white-space: nowrap;"><code>font-variant</code></div><div style="margin:0 1em;white-space: nowrap;">set small-caps</div>
<div style="margin:0 1em;white-space: nowrap;"><code>font-weight</code></div><div style="margin:0 1em;white-space: nowrap;">use bold or thin characters</div>
<div style="margin:0 1em;white-space: nowrap;"><code>hanging-punctuation</code></div><div style="margin:0 1em;white-space: nowrap;">can a punctuation mark be placed outside the line box?</div>
<div style="margin:0 1em;white-space: nowrap;"><code>height</code></div><div style="margin:0 1em;white-space: nowrap;">height of the element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>justify-content</code></div><div style="margin:0 1em;white-space: nowrap;">justifies flexible container's items horizontally if necessary</div>
<div style="margin:0 1em;white-space: nowrap;"><code>@keyframes</code></div><div style="margin:0 1em;white-space: nowrap;">specifies the animation code</div>
<div style="margin:0 1em;white-space: nowrap;"><code>left</code></div><div style="margin:0 1em;white-space: nowrap;">left offset for relative and absolute elements</div>
<div style="margin:0 1em;white-space: nowrap;"><code>letter-spacing</code></div><div style="margin:0 1em;white-space: nowrap;">space between characters</div>
<div style="margin:0 1em;white-space: nowrap;"><code>line-height</code></div><div style="margin:0 1em;white-space: nowrap;">line height of text or inline-block elements</div>
<div style="margin:0 1em;white-space: nowrap;"><code>list-style</code></div><div style="margin:0 1em;white-space: nowrap;">all list properties in one line</div>
<div style="margin:0 1em;white-space: nowrap;"><code>list-style-image</code></div><div style="margin:0 1em;white-space: nowrap;">replace the list item marker with an image</div>
<div style="margin:0 1em;white-space: nowrap;"><code>list-style-position</code></div><div style="margin:0 1em;white-space: nowrap;">list item markers inside or outside the content flow</div>
<div style="margin:0 1em;white-space: nowrap;"><code>list-style-type</code></div><div style="margin:0 1em;white-space: nowrap;">set the type of the list item marker</div>
<div style="margin:0 1em;white-space: nowrap;"><code>margin</code></div><div style="margin:0 1em;white-space: nowrap;">set the top, right, bottom and left margins in one line</div>
<div style="margin:0 1em;white-space: nowrap;"><code>margin-bottom</code></div><div style="margin:0 1em;white-space: nowrap;">bottom margin</div>
<div style="margin:0 1em;white-space: nowrap;"><code>margin-left</code></div><div style="margin:0 1em;white-space: nowrap;">left margin</div>
<div style="margin:0 1em;white-space: nowrap;"><code>margin-right</code></div><div style="margin:0 1em;white-space: nowrap;">right margin</div>
<div style="margin:0 1em;white-space: nowrap;"><code>margin-top</code></div><div style="margin:0 1em;white-space: nowrap;">margin top</div>
<div style="margin:0 1em;white-space: nowrap;"><code>max-height</code></div><div style="margin:0 1em;white-space: nowrap;">maximum height of element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>max-width</code></div><div style="margin:0 1em;white-space: nowrap;">maximum width of element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>@media</code></div><div style="margin:0 1em;white-space: nowrap;">see media queries</div>
<div style="margin:0 1em;white-space: nowrap;"><code>min-height</code></div><div style="margin:0 1em;white-space: nowrap;">minimum height</div>
<div style="margin:0 1em;white-space: nowrap;"><code>min-width</code></div><div style="margin:0 1em;white-space: nowrap;">minimum width</div>
<div style="margin:0 1em;white-space: nowrap;"><code>nav-down</code></div><div style="margin:0 1em;white-space: nowrap;">where to navigate when the the arrow-down button is pressed</div>
<div style="margin:0 1em;white-space: nowrap;"><code>nav-index</code></div><div style="margin:0 1em;white-space: nowrap;">sets sequential navigation order</div>
<div style="margin:0 1em;white-space: nowrap;"><code>nav-left</code></div><div style="margin:0 1em;white-space: nowrap;">where to navigate when the the arrow-left button is pressed</div>
<div style="margin:0 1em;white-space: nowrap;"><code>nav-right</code></div><div style="margin:0 1em;white-space: nowrap;">where to navigate when the the arrow-right button is pressed</div>
<div style="margin:0 1em;white-space: nowrap;"><code>nav-up</code></div><div style="margin:0 1em;white-space: nowrap;">where to navigate when the the arrow-up button is pressed</div>
<div style="margin:0 1em;white-space: nowrap;"><code>opacity</code></div><div style="margin:0 1em;white-space: nowrap;">transparency level of an element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>order</code></div><div style="margin:0 1em;white-space: nowrap;">reorder elements in a container</div>
<div style="margin:0 1em;white-space: nowrap;"><code>outline</code></div><div style="margin:0 1em;white-space: nowrap;">drow an outer border around elements</div>
<div style="margin:0 1em;white-space: nowrap;"><code>outline-color</code></div><div style="margin:0 1em;white-space: nowrap;">outline color</div>
<div style="margin:0 1em;white-space: nowrap;"><code>outline-offset</code></div><div style="margin:0 1em;white-space: nowrap;">gap between the element and the outline</div>
<div style="margin:0 1em;white-space: nowrap;"><code>outline-style</code></div><div style="margin:0 1em;white-space: nowrap;">outline style</div>
<div style="margin:0 1em;white-space: nowrap;"><code>outline-width</code></div><div style="margin:0 1em;white-space: nowrap;">outline width</div>
<div style="margin:0 1em;white-space: nowrap;"><code>overflow</code></div><div style="margin:0 1em;white-space: nowrap;">hide, display or scroll if the content overflows its container</div>
<div style="margin:0 1em;white-space: nowrap;"><code>overflow-x</code></div><div style="margin:0 1em;white-space: nowrap;">horizontal overflow</div>
<div style="margin:0 1em;white-space: nowrap;"><code>overflow-y</code></div><div style="margin:0 1em;white-space: nowrap;">vertical overflow</div>
<div style="margin:0 1em;white-space: nowrap;"><code>padding</code></div><div style="margin:0 1em;white-space: nowrap;">padding between the element border and content</div>
<div style="margin:0 1em;white-space: nowrap;"><code>padding-bottom</code></div><div style="margin:0 1em;white-space: nowrap;">padding bottom</div>
<div style="margin:0 1em;white-space: nowrap;"><code>padding-left</code></div><div style="margin:0 1em;white-space: nowrap;">padding left</div>
<div style="margin:0 1em;white-space: nowrap;"><code>padding-right</code></div><div style="margin:0 1em;white-space: nowrap;">padding right</div>
<div style="margin:0 1em;white-space: nowrap;"><code>padding-top</code></div><div style="margin:0 1em;white-space: nowrap;">padding top</div>
<div style="margin:0 1em;white-space: nowrap;"><code>page-break-after</code></div><div style="margin:0 1em;white-space: nowrap;">adds page break after an element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>page-break-before</code></div><div style="margin:0 1em;white-space: nowrap;">adds page break before an element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>page-break-inside</code></div><div style="margin:0 1em;white-space: nowrap;">allow page break inside an element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>perspective</code></div><div style="margin:0 1em;white-space: nowrap;">how many pixels the 3D element is placed from the view</div>
<div style="margin:0 1em;white-space: nowrap;"><code>perspective-origin</code></div><div style="margin:0 1em;white-space: nowrap;">where is the 3D element based in the x- and y-axis</div>
<div style="margin:0 1em;white-space: nowrap;"><code>position</code></div><div style="margin:0 1em;white-space: nowrap;">positioning type: absolute, fixed, relative, static</div>
<div style="margin:0 1em;white-space: nowrap;"><code>quotes</code></div><div style="margin:0 1em;white-space: nowrap;">set quotation marks to wrap an element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>resize</code></div><div style="margin:0 1em;white-space: nowrap;">declare resizable elements</div>
<div style="margin:0 1em;white-space: nowrap;"><code>right</code></div><div style="margin:0 1em;white-space: nowrap;">right offset for relative and absolute elements</div>
<div style="margin:0 1em;white-space: nowrap;"><code>tab-size</code></div><div style="margin:0 1em;white-space: nowrap;">tab character space length</div>
<div style="margin:0 1em;white-space: nowrap;"><code>table-layout</code></div><div style="margin:0 1em;white-space: nowrap;">table layout algorithm</div>
<div style="margin:0 1em;white-space: nowrap;"><code>text-align</code></div><div style="margin:0 1em;white-space: nowrap;">horizontal alignment of text</div>
<div style="margin:0 1em;white-space: nowrap;"><code>text-align-last</code></div><div style="margin:0 1em;white-space: nowrap;">horizontal alignment of last line of text</div>
<div style="margin:0 1em;white-space: nowrap;"><code>text-decoration</code></div><div style="margin:0 1em;white-space: nowrap;">overline, underline or line-through the text</div>
<div style="margin:0 1em;white-space: nowrap;"><code>text-indent</code></div><div style="margin:0 1em;white-space: nowrap;">indentation of the first line of the text</div>
<div style="margin:0 1em;white-space: nowrap;"><code>text-overflow</code></div><div style="margin:0 1em;white-space: nowrap;">the way how overflowed content is marked (ellipsis)</div>
<div style="margin:0 1em;white-space: nowrap;"><code>text-shadow</code></div><div style="margin:0 1em;white-space: nowrap;">text shadow</div>
<div style="margin:0 1em;white-space: nowrap;"><code>text-transform</code></div><div style="margin:0 1em;white-space: nowrap;">capitalization of text</div>
<div style="margin:0 1em;white-space: nowrap;"><code>top</code></div><div style="margin:0 1em;white-space: nowrap;">top offset for relative and absolute elements</div>
<div style="margin:0 1em;white-space: nowrap;"><code>transform</code></div><div style="margin:0 1em;white-space: nowrap;">2D 3D transformation. See widget.</div>
<div style="margin:0 1em;white-space: nowrap;"><code>transform-origin</code></div><div style="margin:0 1em;white-space: nowrap;">changes the position of transformed elements</div>
<div style="margin:0 1em;white-space: nowrap;"><code>transform-style</code></div><div style="margin:0 1em;white-space: nowrap;">render nested elements in 3D</div>
<div style="margin:0 1em;white-space: nowrap;"><code>transition</code></div><div style="margin:0 1em;white-space: nowrap;">transition properties in one line</div>
<div style="margin:0 1em;white-space: nowrap;"><code>transition-delay</code></div><div style="margin:0 1em;white-space: nowrap;">delay before transition effect start</div>
<div style="margin:0 1em;white-space: nowrap;"><code>transition-duration</code></div><div style="margin:0 1em;white-space: nowrap;">transition effect duration</div>
<div style="margin:0 1em;white-space: nowrap;"><code>transition-property</code></div><div style="margin:0 1em;white-space: nowrap;">which CSS property is the transition affecting</div>
<div style="margin:0 1em;white-space: nowrap;"><code>transition-timing-function</code></div><div style="margin:0 1em;white-space: nowrap;">speed curve of the transition</div>
<div style="margin:0 1em;white-space: nowrap;"><code>unicode-bidi</code></div><div style="margin:0 1em;white-space: nowrap;">should the text be overridden to support more languages</div>
<div style="margin:0 1em;white-space: nowrap;"><code>user-select</code></div><div style="margin:0 1em;white-space: nowrap;">disable user content selection</div>
<div style="margin:0 1em;white-space: nowrap;"><code>vertical-align</code></div><div style="margin:0 1em;white-space: nowrap;">vertical alignment</div>
<div style="margin:0 1em;white-space: nowrap;"><code>visibility</code></div><div style="margin:0 1em;white-space: nowrap;">visibility:hidden elements leave a gap</div>
<div style="margin:0 1em;white-space: nowrap;"><code>white-space</code></div><div style="margin:0 1em;white-space: nowrap;">how are white-spaces handled</div>
<div style="margin:0 1em;white-space: nowrap;"><code>width</code></div><div style="margin:0 1em;white-space: nowrap;">width of an element</div>
<div style="margin:0 1em;white-space: nowrap;"><code>word-break</code></div><div style="margin:0 1em;white-space: nowrap;">text breaking rules when text reaches the end of the container</div>
<div style="margin:0 1em;white-space: nowrap;"><code>word-spacing</code></div><div style="margin:0 1em;white-space: nowrap;">size of white space between words</div>
<div style="margin:0 1em;white-space: nowrap;"><code>word-wrap</code></div><div style="margin:0 1em;white-space: nowrap;">break long words and wrap onto the next line</div>
<div style="margin:0 1em;white-space: nowrap;"><code>z-index</code></div><div style="margin:0 1em;white-space: nowrap;">stack order of the element</div>
</div>

### Reset CSS
<code>
html,body,div,span,applet,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,pre,a,abbr,acronym,address,big,cite,code,del,dfn,em,img,ins,kbd,q,s,samp,small,strike,strong,sub,sup,tt,var,b,u,i,center,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td,article,aside,canvas,details,embed,figure,figcaption,footer,header,hgroup,menu,nav,output,ruby,section,summary,time,mark,audio,video { <code style="color:CornflowerBlue;">margin: <code style="color: firebrick;">0</code>; padding: <code style="color: firebrick;">0</code>; border: <code style="color: firebrick;">0</code>; font-size: <code style="color: firebrick;">100%</code>; font: <code style="color: green;">inherit</code>; vertical-align: <code style="color: green;">baseline</code>;</code>}
article,aside,details,figcaption,figure,footer,header,hgroup,menu,nav,section { <code style="color:CornflowerBlue;">display: <code style="color: green;">block</code>;</code>}
body { <code style="color: CornflowerBlue;">line-height</code>: <code style="color: firebrick;">1</code>;}
ol,ul { <code style="color:CornflowerBlue;">list-style: <code style="color: green;">none</code>;}
blockquote,q { <code style="color:CornflowerBlue;">quotes: <code style="color: green;">none</code>;</code>}
<code style="color: CornflowerBlue;">blockquote</code>: <code style="color: green;">before</code>,<code style="color: CornflowerBlue;">blockquote</code>: <code style="color: green;">after</code>,<code style="color: CornflowerBlue;">q</code>: <code style="color: green;">before</code>,<code style="color: CornflowerBlue;">q</code>: <code style="color: green;">after</code> { <code style="color:CornflowerBlue;"><code style="color: CornflowerBlue;">content</code>: <code style="color: firebrick;">''</code>; content: <code style="color: green;">none</code>;</code>}
table { <code style="color:CornflowerBlue;">border-collapse: <code style="color: green;">collapse</code>; border-spacing: <code style="color: firebrick;">0</code>;</code>}</code>

#### Clearfix
```
.clearfix:after {
    clear: both;
    content: " ";
    display: block;
    font-size: 0;
    height: 0;
    visibility: hidden;
}
.clearfix { display: inline-block; }
* html .clearfix { height: 1%; }
.clearfix { display: block; }
```
