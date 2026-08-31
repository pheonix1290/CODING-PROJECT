# CSS Notes

## What is CSS?

Cascading Style Sheets

Used for:
- Styling webpage
- Formating
- Styling content of ur webpage

---------------------------------------------------------------------------------------------------

## Cascading Rules
- it involves hierachy which decided which is applied and ignored over the after
- They are categories that dictate the level of a css decleration:
  - position    |  least 
  - specificity |
  - Type        |
  - Importance  | most

# Position
  - in position css chooses the highest position which is the last style decleration written
   e.g 
<style>
  li{
    color: red;
    color: blue;
  }
  li{
    color:green;    /*this is owuld be priotised first due to the lower down the rule the more    important*/
  }
</style>  

# Specificity
  - the more specific the selector the more imoprtant it is
  - order of specificity goes
   element            | least
   class selector     |
   attribute selector |
   id selector        |more

  - id selector is more specific becuase ideally you only ment to have only one particular id name to that one element on that webpage

# Type
<link rel="stylesheet" href= "./style.css"> External    | least
<style></style>                             Internal    |
<h1 style= "">Hello</h1>                    Inline      | most

# Important 
  - the (!) most important keyword this ensure this is the most important rule to that element
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
# colour
 colour
 background-colour
# font
 font-family
 font-size
 font-weight
 text-align
 text-transform
# box model
 height
 width
 border
 border-width
 margin
 padding
 box-sizing: border-box;
 inine
 block
 display
 transform
 overflow
# position
 relative
 fixed
 absolute
 static 
 top
 left/right

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
e.g font-size: 1px/1pt/1em/1rem

- font-weight (used for changing boldness of a text)
- the value can be numerical or keyword
e.g font-weight: 700; / font-weight: bold;

- text-align (used to set the position of text)
e.g text-align: centre;

- font-style (used to set the style of the text)

----------------------------------------------------------------------------------------

## Images:
- height (used to set height of image)
- width (used to set width of image)
e.g height= "auto"/ width="200px"

----------------------------------------------------------------------------------------

## Margin:
-  increases the space between the borders of a box and the borders of adjacent boxes.
- the space between border and the content beside or around it
- other margin elemnt include:
e.g 
  <style>
    p{
        margin: 20px;
        margin: 10%;
    }
  </style>
margin-top
margin-bottom
margin-left
margin-right

-----------------------------------------------------------------------------------------

## Border:
- adds space (even if it’s only a pixel or two) between the margin and the padding.
- the dimension of a container which is nirmally madw with the <div> element
- it used determine size of different sides of the container
- the other border include:
   border-top
   border-bottom
   border-left
   border-right
   border-width
   border-stlye
   border-radius
- you use border radius when you wnat make the corner round
- you use border style to change the tytpe of line the border uses   
- border element can also be used to set both top & bottom position seprately form right & left position
- this can be applied using 
<style>
    .term {
        border-width: 10px 20px}  
</style>  
- the first slot which is (10px) reresent both the top and bottom
- the second slot which is (20px) represent both the left and right 

-----------------------------------------------------------------------------------------

## Padding:
-  increases the space between the border of a box and the content of the box.
- this is the space between the content and the border
- it is used to expand or push out the border 
  e.g 
<style>
.term{
    padding: 10px;
}  
</style>

------------------------------------------------------------------------------------------

## Text-transform:
- used to changed all text from upperclass or lower class
- the different values involve:
text-transform: none;
text-transform: capitalize;
text-transform: uppercase;
text-transform: lowercase;
text-transform: full-width;
text-transform: full-size-kana;
text-transform: math-auto;

--------------------------------------------------------------------------------------

## box-sizing:
- used to modify the box calculation
## box-model:
- two types of boxes
they determinehow html element interact
  - inline (these is diaplayed in line wth the eleemnt they our placed beside)
  - block (these is default display seen when prievewing of ur webpage, as  element our stack untop eachother)
  - inline-block (serves as the middle ground, as it behaves like an inine ement where it inline with the element it placed beside but it has the padding and margin of a block-style)

 - display (use to detremine how html element appear on the webpage) 

- <div> and <span> our the boxes used in containg content for styling
- <div> used as a block- container which behves like a rectangle,containg element which have similar content etc
  - it uses class/id as a hook for CSS styling
e.g
<div class="introduction">
   <h2>Introduction</h2>
</div>  

- <span> it an inline container that sit inside a line of text,it doesn't start on a new line unlike <div> that starts on a new line
 - you only use it when you wnat style or target just part of a sentence or a specific word
 - ypou use the class/id as a hook for css styling  
 - takes up as musch space as needed
e.g
<p>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
  eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
  minim veniam, <span class="highlight">quis nostrud <a href="https://www.dictionary.com/browse/exercitation">exercitation</a>
  ullamco laboris</span> nisi ut aliquip ex ea commodo consequat.   
</p> 

--------------------------------------------------------------------------------------------

## Position
- used to determine the position of a box in a webpage
- position consist of 5 different type of positions:
  - static (this is the default position of a box in a webpage adn it stays stacked untop of eachother)
  e.g 
<style>
{
position: static;
top:10px;
right:10px
}
</style> 

  - relative (it a position that is relatove to the default position which cango side ways,top or bottom)
  e.g
<style>
  {
    position: relative;
    top:10px;
    right: 10px
  }  
</style> 

  - absolute ( it position at the top-left corner of a webpage by default if it has no parent box but it normal at the top-left corner of a parent box) 
  e.g
<style>
    {
        position: absolute;
        top: 10px;
        right: 10px;
    }
</style>  
  # Z index
  - it used to determine which elements go untop of eachother on the y-axis
  - it is normally the element whith the highest z-inde that goes untop

  - fixed (is a block that act like a sticker and position is stick to the screen and follow as you scroll down or up)

  -------------------------------------------------------------------------------------------------

  ## Overflow
  - used to determine what happened to a content inside a box if it too big
  - different values include:
    - visible(usually the default in a browser)
    - hidden (chops of the extra content spilling out of the box)
    - scroll(forces scrollbars unto the box, so users can scroll to see it)
    - auto( it add a scrollbar on only one condition, that is if  the content actually spills out of the box)

---------------------------------------------------------------------------------------------------
  ## Transformation  
  - different tyoes of transformerd:

  # translate(Move)
  - used to move elements from its original position along X(horizontal) and Y (Vertical)
    - translate (x,y): moves along both axes
    - translateX(x): moves horizontally
    - translateY(y): vertically only

  e.g
<style>
  .move-me{
    transform:translate(80px, 50px);
  }
</style>  
  # Rotate(Turn)
  - used to rotate element cloackwise(+value) or anticlockwise(-value)
  - the measurement for values can be (deg)/(turn)
  e.g
 <style>
  .rotate-me{
    transform: rotate(45 deg);
  }
 </style> 
 # scale(resize)
 - changes the size of the element
 - value (1) it orignal size
 - value (2) doubles it
 - value (0.5) halves it
 e.g
<style>
  .scale-me{
    trtansform: scale(1.5)
  }
</style> 
 # skew(Tilt)
 - tilt an element along the x/y by a specific degree
 e.g 
<style>
transform: skewY(20deg)    
</style>