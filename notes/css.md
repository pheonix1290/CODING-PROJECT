# CSS Notes

## What is CSS?

Cascading Style Sheets

Used for:
- Styling webpage
- Formating
- Styling content of ur webpage

-----------------------------------------------------------------------------------------

## Types of Styling Sheets

- CSS (Cascading Style Sheet)
- Sass (Syntactically Awesome Style Sheet) 
- Less (Leaner Styling Sheet)

-----------------------------------------------------------------------------------------

## How to Add CSS

# Inline:
- this is best used for applying style to a single element
<tag style="css"></tag> for e.g <html style="background:red"></html>

# Internal:
- this is best used for applying style to a single webpage
<head>                               
    <style>
        selector{
            property: value;
        }
    </style>
</head>
for e.g
<head>
   <style>
       html{
        background: blue;
       }
   </style>      
</head>

# External:
- this is best used for multipage website if you wnat apply same style all throught
- involves creating a seperate file for css can be named anything but end with(.css)
- also involves a <link/> elemnt within the html file 
  <head>
      <link rel="stylesheet" href="./style.css"/>
  </head>

-----------------------------------------------------------------------------------------

## Types of selector

# Universal selector:
- this is used when you want to select all element and apply the same style 
- it is represented with an (*)
   *{
    colour:purple;
   } 

# Type/ element selector:
- this is best used when you want to select all tags that bear the name of that element
   tag{                          
    property:value; 
   }
                                    <!--CSS-->
   <style>
   div{
    colour:white;
   } 
   </style>  

#   class selector: 
- best used when you want to select all element which bear the same class
- class selector in css is written with a fullstop before the selector(.class)
- used when you want to apply same style declarations to multiple elemnts
e.g 
   <div class="alert-text"></div>
    <!-- CSS -->
   <style> 
   .alert-text{
          colour:red;
   }
   </style>

# ID selector:
- best used when you want to select all element which bear the same id
- ID selector in css is written with a sharp(#) brfore the selector(#ID)
- used to apply style to one or specific element

e.g
  <div id="title"></div>
                       <!--CSS-->
  <style>                     
    #title{
        background-colour:red;
    }  
    </style>                 

# Grouping selector:
- best used when a group of elemnt have similar style declaration and u dont want repition
- you but a comma inbetween the selector inorder to group them
<style>
.read {
  color: white;
  background-color: black;
}

.unread {
  color: white;
  background-color: black;
}
</style>
                              <!--Grouping selector-->
<style>
     .read,
     .unread{
            colour: white;
            background-colour: black;
         }
</style>  

# Chaining selector:
- best used when you wnat to select elemnts that has  both classes at the same time
- they should be no space between them if not it becomes a descendant combinator
e.g
   <div class="subsection header"></div>
   <p class="subsection" id="preview"></div>
                 <!-- CSS -->
<style>
    .subsection.header.{
        colour:red;
    }
</style>    
<style>
    .subsection#preview{
        colour: blue;
    }
</style>

# Descendant combinator:
- best used when you want to select an elemnt nested within another element or basically telling the browser to look within the parent element and style the descendant elemnt or elemnt nested within it.
- a space must be put between it
e.g
   <!-- index.html -->

<div class="ancestor">
  <div class="contents">
    <div class="contents"></div>
  </div>
</div>

<div class="contents"></div>
                  <!--CSS-->
<style>
    .anscestor .contents{
                            height:750;
                       }
</style>                  

# Attribute selector:
- this best used when you wnat to selects all elemnts with that specifci attribute
e.g
<style>
    p[draggable]{
        colour: white;
    }
</style>
        <!--Index.html-->
<p draggable="true"></p>
<p draggable="false"></p>   
       <!--CSS-->
<style>
    p[draggable="true"]{
        background-colour:crimson;
    }
</style>       

-----------------------------------------------------------------------------------------

## CSS Properties
 colour
 background-colour
 font-family
 font-size
 font-weight
 text-align
 height
 width
-----------------------------------------------------------------------------------------

## colour:
- colour  (used to set an element text colour)
- bakground- colour (sets the background colour of an element) 
colour in CSS can be sepcified by this following methods:
-Hexadecimal colors e.g {background-color: #ff0000;}
-Hexadecimal colors with transparency e.g {background-color: #ff000080;} 
-RGB colors e.g {background-color: rgb(255, 0, 0);}
-RGBA colors e.g {background-color: rgba(255, 0, 0, 0.3);} 
-HSL colors e.g {background-color: hsl(120, 100%, 50%);} 
-HSLA colors e.g {background-color: hsla(120, 100%, 50%, 0.3);}
-Predefined/Cross-browser color names e.g {background-color: blue;}
-With the currentcolor keyword e.g color: blue; border: 10px solid currentcolor;

-----------------------------------------------------------------------------------------

## Font:
- font-family (used for chaing the font style f a text)
e.g font-family: "Times New Roman", serif;

- font-size (used for chaning size of text/font)
e.g font-size: 22px

- font-weight (used for changing boldness of a text)
- the value can be numerical or keyword
e.g font-weight: 700; / font-weight: bold;

- text-align (used to set the position of text)
e.g text-align: centre;

----------------------------------------------------------------------------------------

## Images:
- height (used to set height of image)
- width (used to set width of image)
e.g height= "auto"/ width="200px"