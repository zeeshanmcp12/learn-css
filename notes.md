# Learn CSS - Notes and Example

## Level 1

- HTML - Structure/Layout
- CSS - Style (Cascading Style Sheet)
  - It's a language to do styling on a webpage.
  - It is used to describe the style of a document.
- JS - Logic

### Basic Syntax

- Selector
  - HTML ka wo element jis par ham styling apply karte hain.
  - For example h1, h2, div, form etc
- Property
  - Yahan wo value hoti hai jis type ka 'style' hamne apply karna hai.
  - For example, color, background-color, etc
- Value
  - Jo bhi style apply karna hai.
  - For example, red, large, larger, etc
- Basic syntax

```css
h1 {
    color: red;
}
```

>Note: `h1` is 'selector', `color` is 'property', and `red` is 'value'.

### Method to add Styling in webpage

- Inline
  - Styling will be added in html file, separately in each element or in selector
- Style tag
  - is main bhi ham styling same html file main add karte hain
- External Stylesheet
  - We create separate css file to add styling in our webpage.
  - External file ko hame `index.html` main link bhi karna hota hai.
  - For example, `style.css`

>Note: Agar ham apni "External Stylesheet" ko inline se replace karenge tu priority inline style ko hoti hai

### CSS Properties

#### Color Property

- It is used to set the color of foreground.
  - Kisi bhi layout k 2 portions hote hain.
    - Background
    - Foreground - Wo cheez jo samne ki taraf dikhai de rahi hai.
  - Foreground - Ye elements foreground main atay hain.
    - Text
    - Button
    - link
- `Color` property foreground ka color set karne k liye use hoti hai, such as 'text', 'button', 'link' etc

```css
h1 {
  color: red;
}

button {
  color: black
}
```

#### Background Color Property

- It is used to set the color of *background*.

```css
body {
  background-color: black;
}

button {
  background-color: white;
}
```

#### Color Systems

- RGB - Most frequently used color system (Red Green Blue)
  - 0 to 255 - colors ka mixture 0 to 255 numbers tak banta hai
  - Red: will be first in RGB - syntax: `color: rgb(255,0,0)`
  - Green: will be second - syntax: `color: rgb(0,255,0)`
  - Blue: will be third - syntax: `color: rgb(0,0,255)`
- Hex - Most frequently used color system
  - To understand the "Hex" color system, let's first understand number system.
    - Binary
      - Bin means 2 - These are numbers from 0 and 1 so numbers will be 01011110
    - Decimal
      - Dec means 10 - These numbers from 0 to 9 so number 103 will be a decimal number
    - Hexadecimal
      - Hex means 6
      - Dec means 10
        - These are number from 0 to 15 so the digits will be 16
          - 0-9 and ABCDEF
  - Jab bhi Hex main colors banayenge:
    - RGB wala **0** Hex main **00** ho jayega
    - RGB wala **255** Hex main **ff** ho jayega.
    - For example:
      - RGB: 255,0,0
      - Hex: #ff0000
        - Hex color banate waqt start main `#` sign lagate hain
- HSLA

##### Syntax

- RGB - Let's create some RGB colors:

```css
h1 {
  color: rgb(255,255,0);
  color: rgb(0,255,255);
  color: rgb(255,0,255);
}
```

- Hex - Syntax

```css
h1 {
  color: #ff0000;
  color: #00ff00;
  color: #0000ff;
  color: #feabff;
  color: rgb(255, 32, 110);
  color: #41ead4

}
```

##### Color picker

- Search on Google
  - It will generate RGB, CMYK, HSV, HSL and HEX

##### Color Palettes

- [coolors.co](https://coolors.co)

#### Selectors

- Universal Selector
  - Ye selector pooray webpage par styling apply karta hai
    - `* {}` - asterisk selector
    - Isko ham global selector bhi kehte hain
- Element Selector
  - Ye HTML tags par apply hone wale selectors hote hain.
  - For example: `h1`, `button`, etc

- Syntax for note:

>Note: CSS main top to bottom styling apply hoti hai. Agar hamne pehle `universal` selector par styling apply ki hai and then `element` selector ko styling denge tu 'element' selector wali styling ko priority mil jayegi.

```css
* {
    color: blue;
}

h1 {
    color: darkgreen;
}

p {
    color:brown;
}

button {
    color:rgb(255, 32, 110);
    background-color: #ffd449;
}
```

>Note: asterisk `* {}` selector styling has been replaced with all selectors.

- Id Selector
  - Is main ham HTML element ko aik 'id' assign kardete hain.
  - Us element par styling apply karne k liye CSS file main `#<id_name>` k sath style de sakte hain. For example
  - `#headingOne { color: black}`
- Syntax:

```html
<h1 id="headingOne">Heading</h1>
```

```css
#headingOne {
  color : blue;
}
```

- Class Selector
  - Is main bhi ham HTML element ko aik 'class' assign kar dete hain but difference ye hai k agar hamne multiple elements par same styling apply karni ho tu un tamam HTML elements ko signle id assign karna bad practice consider hoga. Is situation ko handle karne k liye ham class use karte hain. For example:
  - Syntax

```html
<p class="simplePara">This is simple paragraph.</p>
<p class="simplePara">This is another paragraph.</p>
```

```css
.simplePara {
  color: magenta
}
```

- Another method to do styling on multiple elements.
- Syntax

```css
h1, h2, h3 {
  color: lightblue;
}
```

### Practice Set 1 🚀

#### Q1

- Create a simple div with an id "box".
- Add some text content inside the div.
- Set it's background color to blue.

#### Q2

- Create 3 headings with h1, h2, h3.
- Give them all a class "heading" & set color of "heading" to red.

#### Q3

- Create a button & set its background color to:
  - green using css stylesheet
  - blue using `<style>` tag
  - pink using inline style

#### Text Properties

##### Text Align

- text-align
  - left, right, center
- text by default left-align hota hai.
  - `text-align: right;`
- By Default 'heading' left align hoti hai.
- text-align ki property whole document k hisab se work nahi karti bal k ye parent tag k hisab se work karti hai.
  - For example, agar hamne paragraph likha hai or ye paragraph kisi div k andar hai tu paragraph ki alignment sirf `div` tag k according hogi. Means k wo sirf div k center main ayega, whole body k center main nahi ayega.
- Example to validate above point:

```html
<h1>Heading One</h1>
<div class="box">
  <h1>Heading Inside Div</h1>
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat nisi voluptate non. Exercitationem explicabo ut quos amet, beatae totam ducimus est mollitia temporibus id sunt aliquam ea voluptate quo? Impedit!
</div>
```

```css
h1 {
color: green;
text-align: center;
}

.box {
    border: 2px solid black;
    width: 460px;
}
```

- CSS3 main `text-align` k liye 2 new properties introduce hoi hain.
  - `start` - the function of this property is same as `left`
  - `end` - the function this property is same as `right`

##### Text Decoration

- `text-decoration`
  - underline
  - overline
  - linethrough
  - none - Ye us waqt use hoti hai jab hame anchor tag se underline ko hatana ho.
    - `a {text-decoration: none;}`
  - underline wavy
  - underline wavy green
  - refer to mdn docs for more properties

>Note: mdn text-decoration

##### Font Weight

- font-weight
  - normal
  - bold
  - bolder
  - lighter
- By default font-weigth range:
  - 100 to 900
    - lightest is 100
    - darkest is 900
- bold is set to 400
- 400 se upper value required ho tu bolder set kar sakte hain
- 400 se kam value required ho tu lighter set kar sakte hain

##### font-family

- Type of font
- Style of font
- `font-family: arial, roboto, Tahoma, TimesNewRoman`
  - Single property k sath multiple font styles de sakte hain.
  - Iska reason ye hain browser ki compatibitlies ki wajah se jo font bhi browser k compatible hoa wo chal jayega.
  - comma de kar font style apply karne ka matlab ye hota hai k pehli priority hai isko apply kardo. Agar ye exist nahi karta tu dosre ko apply kardo.
  - This is called `fallback mechanism`
    - Agar aik fail ho jaye tu dosra apply kardo

- Two types of font families
  - 5 Generic Font Families
    - Is main different fonts hote hain
  - Specific Front Families
    - Is main bhi different fonts hote hain

##### Units in CSS

- There are two types of 'units' in CSS.
  - Unit ka relation hota hai size k sath. Means k koi bhi chez kitni big and small hai.
- Absolute Units
  - These are so many
    - px
    - 96px = 1 inch = 2.54cm
      - How do we use it?
        - font-size: 2px;
      - Normally paragraph ka default size 16px hot hai.
- Relative Units

> Note: Absolute units main 'pixel' unit sab se zyada use hota hai.

##### Line Height

- line-height
  - Ye property decide karti hai k hamare text ki height kitni honi chahiye.
- `line-height: 50px`

##### Text Transform

- Upper-case to lower-case and vice versa
- `text-transform: capitalize`
- `text-transform: upppercase`
- `text-transform: lowercase`
- `text-transform: none`
  - Agar pehle css main kahin text-tranform use kiya hai tu ye un sab ko invalid kardega.

### Practice Set 2 🚀

#### P2-Q1

- Create a heading centred on the page with all of its text capitalized by default.

#### P2-Q2

- Set the font family of all the content in the document to "Times New Roman".

#### P2-Q3

- Create one div inside another div.
  - Set id & text "outer" for the first one & "inner" for the second one.
  - Set the outer div text size to 25px & inner div text size to 10px.

>Note: In this code, jo styling parent ko apply hogi wohi uske child ko bhi apply hogi:
```html
<div><p>This is outer div!</p>
  <div><p>This is inner div</p></div>
</div>
```

>Note: Kuch properties aisi hoti hain k jis main parent par jo styling apply karte hain, child par bhi same properties apply ho jati hain.

```html
<div style="font-size: 25px;">AnotherOuter
            <div>AnotherInner</div>
        </div>
```

>Note: Level 1 is complete here.

## Level 2

- We will look at **Box** model in this level.
- According to CSS, 'HTML' k jitne bhi elements hain, such as span, img, div, p etc ye sab eventually aik "box" ki form main hote hain.
- Box model in CSS
  - Height
  - Width
  - Border
  - Padding
  - Margin

### Box Model

>Note: When we will refer the term (word) 'content', it will be anything, button, paragraph, heading, div etc

- Padding
  - Content k around jo extra space hoti hai use ham 'padding' kehte hain.
- Border
  - Content ki boundry ko ham border kehte hain.
  - Kisi bhi content ko jo cheez enclosed karti hai use ham border kehte hain.
- Height
  - Content jitna vertical area leta hai use ham height kehte hain. For example, top to bottom ya bottom to top
- Width
  - Content jitna horizontal area leta hai use ham  width kehte hain. For example, left to right or right to left
- Margin
  - Two boxes k between ki 'space' ko margin kehte hain.

#### Height - in box model

- Content ka wo area jo vertically cover hota hai.
- Example:

```css
div {
  height: 10px
}
```

#### Width

- 'Width' property content k horizontally area ko 'width' dene k liye use hoti hai.

#### Border

- `border-width`
- `border-style`
- `border-color`
- Content k border ko set karne k liye ham 'Border' property use karte hain.
- border ki bhi further properties hain
  - border-style
    - solid
    - dotted
    - dashed
    - wazy
    - ...etc
  - border-width
    - 10px
    - ...etc
  - border-color
    - any color

#### Border (Shorthand)

- We can combine 'width', 'style', and 'color' together to make the border.
- `border: 2px solid black`
  - 2px -> width
  - solid -> style
  - black -> color

#### Border Radius

- `border-radius`
  - ye property border ko radius (curve) dene k liye use hoti hai
  - border ko radius do tarah se de sakte hain.
    - px main
    - percentage main for example '50%' etc
  - Syntax
    - `border-radius: 10px`
    - `border-radius: 50%`

>Note: CSS main koi bhi shape create karne k liye ham use 'height' and 'width' de sakte hain.
>Note: But Circle k liye ham (shape ki) height 100, width 100 and `border-radius` 50% rakhenge tu circle create ho jayega.

Syntax:

```css
div {
  height: 100px;
  width: 100px;
  border-radius: 50%;
}
```

#### Padding

- Border or content k between jo area hota hai use 'padding' kehte hain.
- 'Padding' all sides se apply ki ja sakti hai.
  - `padding-left`
  - `padding-right`
  - `padding-top`
  - `padding-bottom`

##### Padding Shorthand

- `padding: 10px` -> it means, 10px from each side
- `padding: 5px 5px 5px 5px`

>Note: **Padding Shorthand** main clock-wise style apply hota hai. Means k pehle top, then right, then bottom and then left. For example: `padding: 20px(top) 10px(right) 5px(bottom) 5px(left)`

#### Margin

- Two boxes k between jo area hota hai usay 'margin' kehte hain.
- 'Margin' all sides se apply ki jasakti hai.
  - `margin-left`
  - `margin-right`
  - `margin-top`
  - `margin-bottom`

##### Margin Shorthand

- `margin: 10px` -> it means, 10px from each side
- `margin: 20px 10px 5px 5px`

>Note: **Margin Shorthand** main clock-wise style apply hota hai. Means k pehle top, then right, then bottom and then left. For example: `margin: 20px(top) 10px(right) 5px(bottom) 5px(left)`

### Practice Set 3 🚀

#### P3-Q1

- Create a div with height & width of 100px.
- Set its background color to green & the border radius to 50%

#### P3-Q2

- Create the following navbar
  - amazon.com - text size - 25px
  - color - #0f1111
  - anchor tags - Account MyCart Contact Us
  - gap between anchor tags - 200px
  - height - 60px
  - Search bar button color - #f08804
  - placeholder in search bar - `search Amazon.com

### inline/block elements

- HTML main kuch 'inline' elements hote hain and kuch 'block' elements hote hain.
  
#### Block-level elements

- Ye wo elements hote hain jo new line se start hote hain or browser automatically in elements k start and end par space (margin) add kardeta hai.
- Block-level elements full available width lete hain. Left and right se jahan tak strech hota hai ye elements space consume karte hain.
- Most commonly used block-level elements are `p` and `div`
- Syntax

```html
<p>Simple Paragraph</p>
<div>This is div</div>
```

```css
p {
  background-color: aqua;
  border: 2px solid black
}

div {
  background-color: aqua;
  border: 2px solid black;
}
```

- `address`
- `article`
- `aside`
- `blockquote`
- `canvas`
- `dd`
- `div`
- `dl`
- `dt`
- `fieldset`
- `figcaption`
- `figure`
- `footer`
- `form
- `<h1>-<h6>`
- `header`
- `hr`
- `li`
- `main`
- `nav`
- `noscript`
- `ol`
- `p`
- `pre`
- `section`
- `table`
- `tfoot`
- `ul`
- `video`

#### Inline Elements

- inline elements new line se start nahi hote.
- Ye sirf utni hi space consume karte hain jitni zaroorat hoti hai.
- `span` is an inline element

- inline ko block element main and block ko inline main convert kiya ja sakta hai using `display` property.
- Jab ham block ko inline main convert karte hain tu wo elements same line main ajate hain.

- `a`
- `abbr`
- `acronym`
- `b`
- `bdo`
- `big`
- `br`
- `button`
- `cite`
- `code`
- `dfn`
- `em`
- `i`
- `img`
- `input`
- `kbd`
- `label`
- `map`
- `object`
- `output`
- `q`
- `samp`
- `script`
- `select`
- `small`
- `span`
- `strong`
- `sub`
- `sup`
- `textarea`
- `time`
- `tt`
- `var`

>Note: An Inline element cannot contain a block-level element!
>Note: Converting `<button></button>` element to 'block' does not work at the time of writing these notes.

#### Display Property

- `display` inline - block element ko inline element main convert karteda hai.
  - Iska drawback ye hain k
    - Ye element ko same line main le ata hai
    - top and bottom se 'margin' apply nahi hotin
- `display` block - inline element ko block element main convert kardeta hai.
- `display` inline-block: is property ko use karne se 'padding' and 'margin' proper add ho sakti hai.
  - Ye property similar to inline hai but we can set margin & padding.
    - Means k hamari element ki type inline type ki hogi but ham additionally margin and padding bhi apply kar sakenge.
  - Is se margin and padding bhi apply ho jati hai or ye benefit bhi hota hai k elements same line main hi rehte hain.
  - Try the code below for `display: inline-block`
- `display` none: Agar hame us element ko apne document flow se bilkul hi remove karna hai tu ham ye property use karte hain.
  - Is property ki wajah se us element ki koi jaga bhi nahi rehti.
  - Means k wo element document se bilkul gayib ho jata hai.
  - `display: none`

>Note: In simple words, agar ham kisi bhi element ko inline bana chahte hain but sath hi sath ham ye bhi chahte hain k ham us element par saari properties apply kar saken tu us k liye hame `display` ko `inline-block` set karna hoga.

```html
    <h1>Playing around with <code>display</code> property</h1>
    <div id="box-one">Box 1</div>
    <div id="box-two">Box 2</div>
    <div id="box-three">Box 3</div>
```

```css
#box-one {
    width: 100px;
    height: 100px;
    margin: 25px;
    padding: 25px;
    border: 2px solid black;
    background-color: aqua;
    display: inline-block;
}
#box-two {
    width: 100px;
    height: 100px;
    margin: 25px;
    padding: 25px;
    border: 2px solid black;
    background-color: burlywood;
    display: inline-block;
}
#box-three {
    width: 100px;
    height: 100px;
    margin: 25px;
    padding: 25px;
    border: 2px solid black;
    background-color: blanchedalmond;
    display: inline-block;
}
```

#### Visibility

- `visibility: hidden | visible | collapse`
- `visibility` - element will completely invisible but the space is still reserved or in other words, layout will still be effected.
- document main se element completely invisible ho jayega but uski space still reserve rahegi.
- Syntax
  - `visibility: hidden`

>Note: `display` property ko `none` set karte hain tu document flow main space reserve nahi hoti. Jab k `visibility` property ko `hidden` set karte hain tu space reserve rehti hai.

### Alpha Channel

- Alpha channel decides the opacity.
  - Means k koi bhi color kitna zyada dikh raha hai.
  - Opacity starts from 0 to 1
- RGB k sath 'A' add karne se alpha channel ban jata hai.
  - RGBA
    - R = Red
    - G = Green
    - B = Blue
    - A = Alpha - means opacity
  - `rgba(0,255,0,0.75)`
  - `rgba(255,0,0,0.50)`
  - `rgba(0,0,255,0.25)`

>Note: Level 2 is complete here.

### Practice Set 4 🚀

#### P4-Q1

- Create a webpage layout with a header, a footer & a content area containing 3 divs.
- Set the height and width of divs to 100px.
  - (add the previous navbar in the header)

#### P4-Q2

- Add borders to all the divs.

#### P4-Q3

- Add a different background color to each div with an opacity of 0.5

#### P4-Q4

- Give the content area an appropriate height.

## Level 3

- In this level, we will discuss about 'Units' in CSS.
- Ab tak hamne 'Units' main 'Absolute' unit discuss kiya hai jiska matlab hota hai k size fix rahega. Ab chahay wo pixels main ho, inch main ho ya kisi or unit main.
- We will discuss about 'Relative Units' in this level.

### Units in CSS - Relative

- Most popular relative units
- %
  - percentage parent k comparison main hota hai. For example, agar parent main hamne 100px width set ki and us k child ki width ham `20%` set karenge tu ye hoga 20px, because 20% of 100 is 20px
  - % (percentage) unit main agar hamne margin set karni ho tu parent child ki value parent ki width k according hogi.
    - For example, agar parent ki width 200px ho or child ki margin 20% set karen tu 200 ka 20% hoga 40, hence margin set hogi 40px.
  - Syntax

```css
#box1 {
    height: 100px;
    width: 200px;
    border: 1px solid black;
    background-color: aqua;
}

#box2 {
    height: 50px;
    width: 20%;
    background-color: blanchedalmond;
    margin-left: 20px;
}
```

- em
  - It is pronounce as 'm'.
  - 'em' unit font-size k according hota hai.
  - Sometimes 'em' ka size parent element k according set hota hai and sometimes "itself" element k according set hota hai.
  - Means k agar parent element k font ka size 20px hai or child k font ka size 'em' unit use karte hoe `1em` set karenge tu child k font ka size 20px hi hoga.
  - Agar parent element k font ka size 20px ho or child k font ka size 'em' unit use karte hoe `2em` set karenge tu font ka size 40px hoga.
  - Agar parent element k font ka size 20px ho or child k font ka size 'em' unit use karte hoe `0.5em` set karenge tu font ka size 10px hoga.
  - Syntax

```css
#box1 {
  height: 100px;
  width: 100px
  font-size: 20px;
}

#box2 {
  height: 100px;
  width: 50px;
  /* font-size: 1em; */
  /* font-size: 2em; */
  font-size: 0.5em;
}
```
>Note: font-size property main font-size of parent dekha jata hai. width property main 'font-size of element itself' dekha jata hai. For example, Syntax:

```css
#box1 {
    height: 100px;
    width: 200px;
    background-color: aquamarine;
    font-size: 10px;
}

#box2 {
    height: 50px;
    background-color: brown;
    text-align: center;
    margin-left: 10%;
    font-size: 1em;
    width: 5em;
}
```
>Note: `em` unit wese tu font-size property k sath commonly use hota hai. But iska use dosri properties k sath bhi kiya ja sakta hai. For example: `padding`, `margin`, `width` etc. For example - Syntax:

```css
#box3 {
    height: 100px;
    width: 100px;
    border: 1px solid black;
    background-color: burlywood;
    font-size: 16px;
    padding: 0.5em;
}
```
>Note: Yahan padding: 0.5 ka matlab hai k element ki padding 8px hogi because is element k font-size property ki value 16px hai. In simple words, padding for all four sides will be 8px.

- rem (Root em)
  - Yahan par apne parent element ka nahi bal k root element (jo sabse bahar hai jese k html ya body tag us) k font-size k hisab se properties set hongi.

>Note: body tag k andar koi bhi text likhenge jo kisi bhi tag ka part na ho by default uska font-size '16' hai mere browser k hisab se. For example - syntax:

```css
#box3 {
    height: 3em;
    width: 3em;
    border: 1px solid black;
    background-color: burlywood;
    font-size: 16px;
    padding: 2rem;
}
```

- Agar main box2 ki width 5rem set kardon or root element main text ka font-size 16 ho tu box2 ki width ka size 80px set hoga. Because rem (Root em) main root element k font-size k according property set hoti hain.

- vh (viewport height)
  - Hamari screen ki jitni bhi height hai uskay 1% k hisab se element ko size assign hota hai.
  - In `vh`, 1vh means 1%. So agar page height is 824 and we set box3 size to 50vh, it will be calculated as 50% of the browser's page which is 412.
  - If page height is 915 and we set box3 height to 50vh, it is 457.5
  - For example - Syntax:

```css
#box3 {
    height: 50vh;
    width: 100px;
    border: 1px solid black;
}
```

- vw
  - viewport width
    - Ye bhi similar to vh (viewport height) hi hai. Bas is main width ka size set hota hai.

### Position property in CSS

- Hamare document (ya website) par konsa element konsi position par hai.
- Jo property kisi button, div ya or kisi or element ki position ko set karti hai use ham `position` kehte hain.
- Ham apni website ya document par jo bhi element create karte hain uski koi na koi position hoti hai. For example left, top, bottom, and right
- Ham `Position` property ko use karte hoe apne element ko document par kahin bhi place kar sakte hain.
- `position` property main hamare pas 4 ya 5 possible values hoti hain:
  - static
  - relative
  - absolute
  - fixed
  - sticky
- `position` se related hamare pas kuch properties mazeed hoti hain. For example
  - top
  - right
  - bottom
  - left
  - z-index

#### static

- By default saray elements static hote hain. In elements ki `property` static set karne se koi differnece nahi ata or na hi wo apni position change karte hain.
- ye 4ron (top, right, bottom, left and z-index) properties `static` k sath work nahi karti.
- Syntax

```css
div {
    height: 100px;
    width: 100px;
    background-color: bisque;
    border: 2px solid black;
    display: inline-block;
}

#box1 {
    position: static;
    top: 100px;
}

```

#### relative

- `relative` property ka matlab k element 'relative to itself' hoga. Means k kisi element ko `relative` karne k bad us par `position` ki jo bhi property (top, right, bottom, left) apply karenge wo element apne apko usi hisab se move karega.
- Syntax

```css
#box2 {
    background-color: aqua;
    position: relative;
    top: 20px;
}
```

#### absolute

- Jis element par ham ye property apply karenge wo element apne closest positioned ancestor k according work karega.
- `absolute` main position closest positioned ancestor k according set hoti hai. Means k agar box3(div) ki position absolute set ki hai tu uska parent dekha jayega k konsa hai.
- Agar closest ancestor `body` hoga to postions (top, right, bottom, and left) usi k according set hogi.
- Syntax

```css
#box3 {
    background-color: cadetblue;
    position: absolute;
    top: 20px;
}
```

- Yahan top se hamne 10px kardiya and closest positioned ansector body tag hai so box3 ki position bilkul top se 10px set ho jayegi.

>Note: See the difference between `relative` and `absolute` position property. Dono ki position top se 20px set hai but `relative` ki position closest positioned ansector na hone ki wajah se document k bilkul top se set nahi ho rahi. Jab k `absolute` ki position closest positioned ansector (body element) hone ki wajah se bilkul top se set ho rahi hai.

#### fixed

- `fixed` main position browser ki windows k according set hoti hai. Is main closest positioned ansector nahi dekha jata.
- Is main position browser ya poray document k according set hogi.
- `absolute` k case position kabhi browser and kabhi `closest positioned ansector` k according set hoti hai but `fixed` main **relative to browser** hoti hai.
- is case main element document flow se hat jayega.
- Jo websites k 'headers' ya 'footers' hote hain us main ham ye property use karte hain. Means k header/footer ko ham top or bottom par fix kar dete hain.
- For example, see syntax

```css
#box4 {
    background-color: chartreuse;
    position: fixed;
    /* right: 10px; */
    bottom: 0;
    display: block;
    width: 100vw;
}
```

- yahan box4 poray k poray document k right se 10px agay ho jayega.
- Agar hame box4 ko footer main convert karna hai aur bottom par fix karna hai tu ham bottom ko 0 kardenge and iski width ko 100px kardenge ya 100vw kardenge.

#### sticky

- Ye additional property hai jo user k scroll k according work karti hai. Means k agar ham kisi box ki position **sticky** set karden aur position ki value koi rakhen, let's say top:50px, tu ab user ki scrolling jese hi is box tak ayegi uski position top se 50px set ho jayegi.
- Syntax
  - Click [here](./Practice%20Set%205/style.css) for the syntax along with example.

#### z-index

- Hamare page par boxes overlap kar sakte hain. By default jo div pehle likha hai wo niche (under) chala jayega and jo bad main likha hai wo oper (above) chala jayega. But ham is cheez ko control kar sakte hain using **z-index** property.
- By default har element ka z-index 0 hota hai.
- **z-index** ki value positive main denge tu position oper ho jayegi means k wo element oper show hoga.
- **z-index** ki value negative main dene se element (box) ki position niche ho jayegi.
- Click [here](./CSS-Levels/level3/style.css) for syntax and example.

>Note: [unsplash.com](https://unsplash.com)

### Background Image

- `background-image`
  - `background-image: url(image_name)`

### Background Size

- `background-size`
  - cover
  - contain
  - auto
- `background-size: cover`
- `background-size: contain`
- `background-size: auto`

#### Syntax For Background Image/Size

```css
#box1 {
    background-image: url('kitten-image1.jpg');
    background-size: cover;
}

#box2 {
    background-image: url('kitten-image2.jpg');
    background-size: cover;
    /* background-repeat: no-repeat; */
    background-position: center;
}
```

## Level 4

### Flexbox

- Flexible Box Layout

#### Flexbox model

- Flex container
- Flex Item
- main axis - Horizontal/Vertical direction
- cross axis - Horizontal/Vertical direction

##### How to make container a *Flexbox*?

- Set `display` property to `flex`

##### Flexbox Direction

- `flex-direction: row;` this is by default.
- `flex-direction: row-reverse;`
- `flex-direction: column;`
- `flex-direction: column-reverse;`

##### Flex Properties

- justify-content: flex-start/flex-end/center/space-around/space-between/space-evenly
  - space-around main left-most and right-most ki space center wali spaces se half hogi
- flex-wrap
- align-items
- align-content
  - `align-items` and `align-content` has to be revised for more clarity. There is little difference between both of them.
  - Jab hamne flex k items ko wrap kiya ho and `align-items` se usko `flex-start` ya `center` karenge tu center space ajayegi because items wrapped hain.
  - `align-content` ko use karne se wo space khatam ho jayegi.
  - Syntax:

```css
div {
    height: 50px;
    width: 150px;
    border: 2px solid black;
    display: inline-block;
}
#container {
    height: 600px;
    width: 600px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: flex-start;
    align-content: center;
}
#box1 {
    background-color: aqua;
}
#box2 {
    background-color: cadetblue;
    height: 200px;
}
```

>Note: Agar ham kisi container ko flex box bana denge tu us k andar jitne bhi items honge wo sab k sab container main hi apne ap fit karenge and bahar nahi niklenge.
>Note: But ye us waqt tak hoga jab tak in k andar ka content allow kare. Means k jab tak font size exceed nahi kar raha us waqt tak usi container main fit hoga and jese hi item (div) ki height font-size se choti hogi then ab ye item (div) us main fit nahi hoga.

##### Flex Properties for Flex Item

- `align-self`
  - Ye us waqt work karti hai jab ham ye chahte hon k koi individual element ya box separately align ho na k container k saaray elements k sath.
  - iski highest priority hoti hai as compare to jo ham container par apply karte hain.
  - Means k agar hamne kisi individual element ko `align-self` ki property set kardi tu us element ki priority highest hogi.
- `flex-shrink`
  - Agar kisi element ko jaldi se shrink karwana hai tu uske factor ko 1 se bara kar sakte hain.
  - Agar kisi element ko der se shrink karwana hai tu uske factor ko 1 se decrease kar sakte hain.
  - Factor matlab hai k equally shrink ho raha hai ya dosre elements k comparison main kam ya zyada shrink ho raha hai.
  - Agar ham ye chahte hain k element ki width bilkul bhi shrink na ho and jesi hai wesi hi rahay tu ham uski shrink property ko 0 set karte hain.
    - `flex-shrink: 0`
  - Differences:
    - `flex-shrink: 0` - Element bilkul shrink nahi hoga
    - `flex-shrink: 1` - Element equally shrink hoga
    - `flex-shrink: 0.5` - Element slowly shrink hoga, means k dosray elements k comparison main kam shrink hoga
- `flex-grow`
  - Is main ye hota hai k agar container ki width zyada ho or us container k flex items ki width kam ho tu ham jis flex item ki property `flex-grow` with any value for example `flex-grow:1` set karenge wo flex item expand ho kar us container ki saari jaga lelega.
- Syntax

```css
#container {
    border: 2px solid black;
    height: 300px;
    width: 800px;
    display: flex;
    flex-direction: row;
    align-content: flex-start;
}

div {
    border: 2px solid black;
    /* display: flex; */
    height: 100px;
    width: 50px;
}

#box2 {
    background-color: bisque;
    height: 200px;
    flex-grow: 2;
}

#box4 {
    background-color: cadetblue;
    flex-grow: 2;
}
```

##### Difference b/w align-items and justify-content

- `justify-content`
  - `Main-axis` (left-to-right) main rehte hoe agar content (items) ko center align karna hai tu us k liye ham `justify-content` use karenge.
- `align-items`
  - `Cross-axis` top-to-bottom main rehte hoe content (items) ko center align karna hai tu k liye ham `align-items` use karenge.

### Media Query

- Apne web page ko responsive banane k liye ham media queries use karte hain.
- Media queries main ham range define karte hain jis main ham width batatay hain.
- For example, agar width 600px ho tu font size etc change ho jaye
- Syntax

```css
@media (width: 600px) {
  div {
    font-size: large
  }
}

@media (min-width: 300px) and (max-width: 400px) {
  div {
    font-size: larger
  }
}
```

#### Practice Set 7

- Add a media query to implement the following:
  - the color of a div changes to green for viewport width less than 300px
  - the color of a div changes to pink for width between 300px & 400px
  - the color of a div changes to red for width between 400px & 600px
  - the color of a div changes to blue for width above 600px

## Level 5

### Transition

- transition-property - element ki jitni bhi properties hain un sab par transition apply karna. Jese k `font-size`, `width` etc
- transition-duration - transition kitni der tak us element par apply rahegi. For example: 2s / 4ms etc
- transition-timing-function - is main different functions hain, jese k ease-in / ease-out / linear / steps etc
- transition-delay - transition kitni der bad apply hogi. For example, agar hamne `div` ko `hover` set kiya hai tu jab ham mouse ko div par hover karenge to 2 second bad transition apply hoga.

#### Transition Shorthand

- property name | duration | timing-function | delay
  - Syntax `all 2s ease-in 1s`

#### State change

- Pseudo class
  - Syntax: div:hover{ color:red}

#### CSS Transform

##### CSS Transform - Rotate

- elements ko 2D and 3D form main rotate karna
- Chezon ko rotate karna
- Chezon ko size main bara karna, small karna
  - Syntax `transform: rotate`
    - Syntax `transform: rotate(45deg)` - 45 deg rotate
- Agar ham 3D form main rotate karna chahte hain tu us k liye syntax ye hoga:
  - Syntax: `rotate: x 60deg`

##### Important about x axis, y axis and z axis

- x axis horizontal jata hai (left to right)
- y axis vertical jata hai (top to bottom)
- z axis bahar ki taraf araha hota hai

##### CSS Transform - Scale

- Scale ka matlab hai koi bhi element kitna bara hota hai (means k scale hota hai)
- scale(1) - iska matlab hai k na bara hona na chota
- scale(2) - jo size abhi hai uska double ho jana
- scale(0.5) - jo size abhi hai us se half ho jana
- Syntax:
  - `transform: scale(2);`
  - `transform: scale(0.5);`
  - `transform: scale(3);`
- Agar x and y axis, dono k around scale karna hai tu syntax ye hoga:
  - Syntax: `transform:scale(2,3)
- Ham individually bhi scale property ko use kar sakte hain with transform
  - Syntax: `transform: scaleX(3)
  - Syntax: `transform: scaleY(5)

##### CSS Transform - translate

- translate ka matlab hai k ham element ko jis axis (x and y) main jitne pixel bhi set karenge, hamara element utna hi screen par move karega.
- Syntax
  - `transform: translate(200px); - X axis main move karega

##### CSS Transform - skew

- skew main element ki shape change ho jati hai.
  - Syntax:
    - `transform: skew(40deg);`

### Animations

- It works simlar to transition but add additional features to make the animations more creative

#### Keyframe in Animations

- Jis tarah hamne responsiveness k liye media queries use ki thin usi tarah animations use karne se pehle hame uski templating/blueprint create karne hote hain.
- Syntax

```css
@keyframe animation_name {
  from {css_property:value}
  to {css_property:value}
}

/* Create template */
@keyframe colorAnimate {
  from {background-color: aquamarine}
  to {background-color: red}
}

/* Use Animation */
#box-for-animation {
  
}
```

#### Animations Properties

- In previous step, we created a template (or we call it keyframe) to use it for animation. Now, we will utilize this template.
- Animation template ko use karne k liye CSS main kuch properties hain:
  - animation-name
    - Yahan us template (keyframe) ka name use hoga jo hamne in previous step create kiya hai
  - animation-timing-function
  - animation-duration
  - animation-delay
  - animation-directon
    - jo bhi direction set karenge usi k according animation chalegi.
    - For example
      - `animation-direction: normal` - `from` se `to` wali animation
      - `animation-direction: reverse` - `to` se `from` wali animation
  - animation-iteration-count
    - For example
      - `animation-iteration-count: infinite`

#### Animation Shothand

- Syntax:
  - `animation: name duration timing-function delay iteration direction`
  - `animation: boxAnimator 3s linear 1 infinite/any_number normal/reverse`

#### % in Animation

- Jab ham kisi element par animation apply karte hain tu uska matlab ye hota hai k ham uski state change kar rahe hain.
  - Jab kisi element ki state change hogi tu initially wo 0% hoga and jab animation complete ho jayegi tu wo us element ki state 100% ho jayegi.
  - Yehi % (percentage) ka concept hai.
- Ham Animation ki templating karte waqt `from` or `to` k bajaye, `%` ka use kar sakte hain.
- `0%` ka matlab hai k animation apply hona start hogi
- `100%` ka matlab hai k animation completely apply hogayi
- ham `0%` to `100%` k between bhi koi state add kar sakte hain. For example:

```css

@keyframes boxAnimator {
  0% {background-color: violet}
  50% {background-color: orange}
  100%{background-color: aquamarine}
}

@keyframes colorChangeAnimation {
    0% {background-color: red;}
    14% {background-color: orange;}
    28% {background-color: yellow;}
    42% {background-color: green;}
    56% {background-color: blue;}
    70% {background-color: indigo;}
    100% {background-color: violet;}
}
```

#### Practice Set 8

- Create a simple loader using CSS
  - Step 1: Create a div with circular shape & a thick border from one end (top/bottom/left/right)
  - Step 2: To make it spin create an animation which transforms it from 0deg to 360deg
  - Step 3: Add the animation property to the loader with infinite duration.

##### Solution

- Click [here](./Practice%20Set%208/style.css) to see the solution

>Note: Here, we've completed the basics of CSS.

## Project - Amazon Clone

- Create Amazon Clone

### Fontawesome

- To get free icons
- Import fontawesome css in your project and add the cdn link to your html file
  - Once imported, we can use different icons in our code without having to download it in our local system.

### Project Base Setup

- Create HTML file
- Create CSS file
- Link CSS file with HTML
- Import fontawesome cdn in HTML file
- set the margin of body to 0
- set font family with what your like.
- set border to `border-box`. kisi element k border ko `border-box` set karne ka matlab ye hai k element ko jitni bhi padding milay ya jitna bhi border size us element ko mile wo uski height/width k andar consider ho naa k bahar.
  - For example, agar hamne kisi element ki heigh/width 100px set or usko 2px ka border diya tu us element ki total height/width 104px hogi. Because 2 2 pixels top/bottom and 2 2 pixels left/right se usko mil jayenge.
  - Iska matlab ye hoa k border set karne se wo border us element k outside consider hota hai.
  - `border-box` property set karne se ye faida hoga k wo border ka size element k andar consider hoga.
  - combined example
  - `* {margin: 0, font-family: Arial, border:border-box}`

## Emmets

- lorem
  - Ye likhne se pora paragraph generate ho jayega jo random words par based karta hoga
- lorem*10
  - Is case main lorem wala text 10 times ayega.
- .myClass - (starting with dot)
  - Ye likhne se new `div` element create ho jayega jis ko automatically `myClass` name ki class mil jayegi.
- #myId - (starting with hash)
  - Ye likhne se new `div` element create ho jayega jis ko automatically `myId` name ki id mil jayegi.
- Syntax

```html
    <div class="new-box"></div>
    <div id="new-id"></div>
    <div>
      <p>lorem</p>
    </div>
```

## Some Extras

- Kisi bhi big project par kam start karne se pehle 'Universal' element ki padding and margin 0 (zero) rakhte hain. For example

```css
* {
    padding: 0;
    margin: 0;
}
```

- Jese hi ham div ko add karte hain wese hi sara content next line main chala jata hai.
- Different types of structure for website
  - Linear
  - Hierarchical
  - Webbed
- Active Space
- Passive Space
- `list-style-type:none` this property is used to remove dots from list style type.