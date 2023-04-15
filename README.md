# **CSS DOCUMENTATION** (_Cascading Style Sheet_).

## **Introduction**  

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

### ANATOMY OF CSS
Syntax = `` selector{ property: value; } ``  
Selectors are simply used to select a particular element and apply any styles over it.  
Different Selectors are -
> - class selector ``.class_name{}``  
> - id selector ``#id_name{}``  
> - element selector ``element{}``
> - group selector  ``element1,element2{}`` 
> - universal selector  ``*{}`` 

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

## **Colors**
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
