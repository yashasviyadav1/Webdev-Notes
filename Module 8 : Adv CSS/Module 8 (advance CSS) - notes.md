
## Module 8.1 (CSS Display)

The `display` property specifies the display behavior (the type of rendering box) of an element.

There are 4 display property values :- 
 1. Block
 2. Inline
 3. Inline-block
 4. none 

###### Display: Block 
displays element as a block element (like p tag) it starts on new line and takes up the whole width of the screen
note : <i> Height and width of that element are changeable here. </i>
note : <i>no matter how much we change the width, the block element will never come to the next line.</i>

![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/9f0d035c-0f5f-4b10-808d-f5560bc44e3d)

![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/6c7bab47-0e0a-4a89-89dc-ad448cec847a)

###### Display: Inline 
displays element as inline element (like span), and goes in line with the previous element.
note : <i> any height and width property will have no effect on the element. </i>
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/37413251-c029-427d-b89c-689278c0fe8f)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/9b24942b-babe-40be-9d98-6c19dedd645a)

###### Display: Inline-block 
Displays an element as an inline-level block container. The element itself is formatted as an inline element, but you can apply height and width values

note : suppose 3 div's have a display property set to `inline-block`, then they will go straight in a horizontal line, but if we reduce the size of screen then the divs will go into vertical order 
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/117205ec-4193-451c-afc2-5564e257fb72)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/732270c5-d029-4979-aa2a-abf30f6f8a08)

note : <i> When we apply height and width to the element, then it will be changed, and suppose width is set to be more then the screen size, then in that case the element's on right of the `inline-block` element will go to the next line</i>
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/ef1903ef-3dc4-4d87-9f39-2afb10e8267d)

![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/1973dd01-78ef-46bd-875b-744dd9e3df46)

![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/4e965efa-6a9a-4109-a81e-58d39a63b04e)

note : if width of inline-block element is more then the screen then this element will come to the next line 

![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/f468cdbc-d879-46e8-b675-53f38e1e2cd9)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/546e2fae-66ba-4b8e-ae6f-6c5841fa4dd2)

###### Display: None
In this case the element will hide and not be visible.


#### Que - Suppose we have a para inside div, now how can we place it in absolute center of the div ? 

```html
<div> 
	<p> Some Text </p>
<div>
```
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/60705c98-c405-4b13-b943-d6316df3e6b4)

Solution :- 

Way-1:  using `margin` & `width ` (not the best way)

set p's width to any percent eg. 70% of div
and now the left space is 30%, so if we give p's `margin-left and margin-right`  to 15%(of div), then p will be at center of div.

```css
/* method-1 (using margin)*/
div{

}
p{
    width:70%;
    margin-left: 15%;
    margin-right: 15%;
}
/*
to center the text set p's text-align: center
*/ 

```
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/d39a660b-0956-4466-a930-c3ceee5162d6)

⭐Way-2): using `position: absolute` (left, right, top, bottom) properties

similarly instead of padding, we could also use position: absolute (for p) and position: relative (for div) then push the p a 15%(of div) from the left and right.
this is the right way.

```css
div{
    position: relative;
}
p{
    width: 70%; /*rest : 30% of div*/
    position: absolute;
    left: 15%;
    right: 15%;
}
```
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/d39a660b-0956-4466-a930-c3ceee5162d6)

------------
## Module 8.2 (CSS Float & Clear property)

###### Que - How to make text wrap around our image ? 

lets say we have a `img` and a `p` tag so we want out text to wrap around out img, then if we use `display: inline` on both of them then the text will just go at the right end of the img, and will not wrap around, so we can use the `float: left` here to let the image float on the left of its parent element (html body in this case). 

values of float : `float: left, right`

eg. if we used the display: inline then :- 
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/21367083-af6a-427b-9dab-480de7919e64)

if we used the float : left property.
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/dc810c05-22fe-4137-bbe0-213b71c84eb0)

more examples : 
![screenshot-www udemy com-2023 07 26-19_49_28](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/f9e6dbbc-3d9a-4735-9ba7-64cd7c605b7b)

Another scenario :- let say we have 3 elements, `img, p, footer` now here we have our image float : left, now our result will look like this :- 
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/6fc2cdc6-8a3d-441b-b44a-a7e668b09549)

because the float left is applied to img, now every other element will wrap around it, but we do not want out footer to wrap, because footer always comes at the end (capturing all the width of screen) so in this case we can use the `clear: left, right, both`  property which will allow the 'footer' to escape the mentioned float and will not wrap around.
like this :- 
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/61b1ce8f-499f-4545-99a8-635575b3a57e)

![screenshot-www udemy com-2023 07 26-19_52_32](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/172855f5-9e4b-4f6e-95f8-7fb88ce4c921)

###### Que - Difference between `float` & `display:inline` on multiple divs ?

When we set all 3 div's to float left then they will come in line with each other, but note that they have no margin by default.
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/e10b2699-421f-4b6d-bf7b-ba647a56a987)

But instead of the float, if we used the `display: inline` then all 3 became inline element but with some default margin :- 
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/942a5394-c141-4e1b-aac8-74bea0774ac8)


-------


## Module 8.3 (How to make Website Responsive)

Responsiveness of a website means, that on different devices of different screen sizes our website should also adapt. 
There are 4 ways to do that :- 
  1. Media Queries 
  2. CSS Grid 
  3. CSS Flexbox
  4. External Framework (eg. bootstrap)


###### Media Queries 
In this we specify different CSS for different screen sizes 
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/8c035ce2-041c-435e-89f9-7eef2a876ad8)

###### CSS Grid 
It is used for 2d designs in a webpage
![Untitled (5)](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/ccb370fe-7d81-412d-a619-0d51ce1d2cdf)

###### CSS Flexbox 
It is used for 1d design (either horizontal or vertical)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/9bcc533b-a9df-45d0-b496-6999253167d2)

###### Bootstrap
it is called framework because it is external, not present in html or css itself.
Bootstrap has a 12 division flexbox system i.e entire screen is divided into 12 coloumns of equal size.
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/b98f3e8f-3423-46f8-acf9-8b2084f9a1cc)



--------

## Module 8.4 (Media Queries)

  
The `@media` rule, introduced in CSS2, made it possible to define different style rules for different media types.

To target screens from 0px to 100px width  (inclusive)
```css
@media (max-width: 100px){
	body{
		color: seablue;
	}
}
```

To target screens from 100px to 300px width  (inclusive)
```css
@media (min-width: 100px) and (max-width: 300px){
	body{
		color: seablue;
	}
}
```


To target screens from 0 to 300px  and 400px to max width  (inclusive)
```css
@media (max-width: 300px) and (min-width: 400px){
	body{
		color: seablue;
	}
}
```

------
###### Que - How to create a card like a newspaper?
Solution :- 



----------
###### Que - How to create a attractive navigation bar, and center its anchor and division tags ?
Solution :- 

example1 :- 
![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/dad043e9-bfd6-4f80-98e1-a1827420fb43)

breakdown: 
![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/1838cdfb-7616-4724-97c4-b16f38fd6484)

example 2:- 
![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/5facbca0-7fcc-4c88-8f99-97d20d348b37)

Breakdown :- 
![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/d4860397-ed69-4305-8172-d386ab213511)
note : the red box is the anchor tags and blue one is div container.

To start this first, choose a dark background for body, and a lighter color for the navbar

- step1: now create a `div` (the `class="navbar-outermost-div"`) 
- step2 : inside this create another `div`  (the `class="navbar-container-div"`) (this will contain smaller divs and will help to center the links)
- step3 : create 3-4 `divs` (as per the number of links) inside the container-div give these same (`class="icon-divs"`)
- inside these divs create anchor tags `<a>` and give them same `class="icon-anchor-links"`.

html :- 
```html
<div class="navbar-main-div">
        <div class="navbar-icon-container">

            <div class="navbar-icon-div">
	            <a href="#" class="icon-anchor-link">Home</a>
            </div>

            <div class="navbar-icon-div">
	            <a href="#" class="icon-anchor-link">About</a>
            </div>

            <div class="navbar-icon-div">
	            <a href="#" class="icon-anchor-link">Pricing</a>
            </div>

        </div>
    </div>
```

now lets set them at their right positions (using css):- 

- step1 : 1st set the width of the div `(navbar-main-div)` to 100%.
![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/6c42d200-dd00-4872-bbb8-37430f71073a)

- step2 : now center the inner div `(navbar-icon-container)` inside the outer main div, 
   by setting its width to lets say any number eg. 50%. now set its `position: absolute` 
   and set outter main div's `position: relative`, now we know the remaining space is 50%, so now for the `navbar-icon-container` div push `left: 25%` and `right: 25%`. 
   and here out navbar-icon-container div is in center.
![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/3e70b3ce-7209-4b8a-9114-33193bee238d)

step3: now to set these smaller 3 div's `icon-divs` into horizontal line set their `float: left` .
![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/980cfc1d-997c-47c5-8ec9-fbe61ce1a53f)


- step 4 : now out `navbar-icon-container` is in center from left and right but is not in center from top and bottom of the `navbar-main-div`, for that we will give it a height of lets say `height: 70%` now remaining is 30% so we push this container div 30% downwards from the outter div i.e `top: 30%`, this way we canter our anchor tags.
![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/d8efcf2a-4ca6-4734-a8ab-5ead5fc661a3)


- step 5: now we need to resize the 3 `<div>`  `navbar-icon-divs`, so lets set their ` width: 33%;`
  so that all 3 will capture the `navbar-container-div` equally because 33+33+33 -> 99%, and all 3s `height: 100%;` of its parent container div, then by using `text-align :center` on the  3 divs the anchor tags will be placed at center of the 3 div's.
  ![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/1ee6b8f8-513e-4275-bed0-7dc5b1ae332c)

Output : 
  ![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/9cef70d4-3035-4fa5-bb5e-1042ea8e85c1)

```css
body,html{
    margin:0;
}

body{
    background-color: #322653;
}
  
.navbar-main-div{
    background-color: #9288F8;
    height: 65px;
    position: relative;
}
  
.navbar-icon-container{
    position: absolute;
    /* border: 1px solid red; */    
    height: 70%;
    width: 50%;
    left: 25%;
   right: 25%;   /* i set the ht to 70% then pushed the container 30% so that to center the icons*/
    top:30% ;
}

.navbar-icon-div{
    float: left;
    /* border: 1px solid black; */
    height: 100%;
    width: 33%;  /*note: their is little space on right end of the navbar-container-div because 33+33+33-> 99, remaining=1*/
    text-align: center;
}

.icon-anchor-link{
    font-size: 20px;
    color: #17151c;
    font-family: 'Poppins', sans-serif;
    text-decoration: none;
}

.icon-anchor-link:hover{
    font-size: 20px;
    color: #d21f1f;
    font-family: 'Poppins', sans-serif;
    text-decoration: none;
}
```
  

---------------
