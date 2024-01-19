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

#### Units in CSS

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