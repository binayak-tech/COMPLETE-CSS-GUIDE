# **CSS DOCUMENTATION** (_Cascading Style Sheet_).

## **CHAPTER 1** 
### **Introduction**  

CSS is used to style the web pages created by html.

There are three ways to attach css in a html file.

> 1. Inline CSS = It is written inside of a html tag, but it is considered as a bad practice to use inline css.
```
    <hr style="width:50px; color:limegreen;"> 
```

> 2. Internal CSS = It is written inside the head tag of html.
```
    <head>
        <style>
            p{color:red;}
        </style>
    </head>
```
> 3. External CSS = It is considered as best practice to style html code. It uses an external file with a .css extension and it can be linked inside head of a html document by using- 
```
    <link rel="stylesheet" href="address">
```
HTML and CSS use a top down approach to parse the code so whichever styles are parsed last will be applied in case you applied multiple styles to the same tag.

**ANATOMY OF CSS**
Syntax = `` selector{ property: value; } ``  
Selectors are simply used to select a particular element and apply any styles over it.  
Different Selectors are -
- class selector ``.class_name{}``  
- id selector ``#id_name{}``  
- element selector ``element{}``
- group selector  ``element1,element2{}`` 
- universal selector  ``*{}`` 

It can also be a combination of multiple selectors ``p.class_name{}`` in this case the selector will select all the p elements with a specific class name.  
To select a nested element ``p span{ background-color: gold; }``  
CSS has many propety and their associated values for styling any element. for example -  
```
    p,h1,h2{
        color: navy;
        text-align: center;
    }
```
Here p,h1,h2 are the selectors, color,text-align are the properties and navy, center are the values for those properties.  
The more specific selector can overrule the less specific slectors properties. 
```
    <style>
    p{color: blue;}
    .second{color: red;}
    #first{color: yellow;}
    </style>

    <p class = "second" id = "first">Hie there!</p>
```
Here id selector will override all to render the paragraph as yellow as the specificity of css is ``id > class > element``. But as inline css, id selector is also not a good practice.  
You can use important flag to make any selector property value as highest priority such as 
```
    p{ color: purple!important;}
```
**COMMNENTS**  
In CSS comments can be written inside `` /* here */ ``. 

### **Colors**
In CSS colors can be represented using
> 1. Color Names- ``red, yellow, blue, aqua, gold ...``  

> 2. RGB values- ``rgb(0,0,0) to rgb(255,255,255) | rgba(22,33,234,0.6)``

> 3. HEX values- ``#rrggbb rr-red, gg-green, bb-blue are hexadecimal values ranging from 00-ff same as decimal (0-255) | #ffad47``

> 4. HSL values- ``hsl(hue, saturation, lightness) | hsl(0,50%,100%) | an alpha(opacity) 0-1 value also can be used hsla(15,100%,35%,0.5)``  

The color property can be used for text coloring, background coloring and border coloring.
```
h1{
    color: #ffca53; 
    background-color: rgb(144,33,234);
    border-color: violet;
}
```

### **Background**
In CSS various background properties are used to effect the background of the element. It has various properties but in this section we will discuss about the following properties.  

- [**background-image:**](https://developer.mozilla.org/en-US/docs/Web/CSS/background-image)
- [**background-repeat:**](https://developer.mozilla.org/en-US/docs/Web/CSS/background-repeat)
- [**background-position:**](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position)
- [**background-color:**](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color)
- [**background-attachment:**](https://developer.mozilla.org/en-US/docs/Web/CSS/background-attachment)
- [**background:**](https://developer.mozilla.org/en-US/docs/Web/CSS/background)
- [**background-clip:**](https://developer.mozilla.org/en-US/docs/Web/CSS/background-clip)

 

### **Border**
The border property allows us to specify the color, width and style of a element's border.  
  
1. <u>**border-width**</u>  
The border-width property tells how thick the border can be. border-widht: top right down left;  
example - ``border-width: 25px 10px 4px 35px;``  

2. <u>**border-style**</u>  
The border-style propety styles to border, example- ``border-style: dotted;``  
Various other values are - ``dashed, solid, double, groove, ridge, inset, outset, none, hidden``...  

3. <u>**border-color**</u>  
The border-color property is used to set color to the border.  
Example - ``border-color: limegreen;``

4. <u>**border-radious**</u>  
The border-radious property is used to give a rounded corners to the borders, and it also can completely change the shape of the border.  
Example - ``border-radious: 15px;``..

5. <u>**sides**</u>  
Indivisual sides of the border can be accessed to style them differently.  
Example - ``border-top-width: 2px;  ``
``border-bottom-style: dotted;  border-left-color: purple;  border-right-radious: 3px;``

5. <u>**shorthand**</u>  
The border shorthand property can be used to make it easy. border: width style color;
Example - ``border: 2px solid black;``  
``border-top: 5px dotted red;``




