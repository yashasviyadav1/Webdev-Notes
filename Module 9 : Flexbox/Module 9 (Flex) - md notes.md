
## Module 9.1 (Learning Tables and Flex)

###### Que - how to create tables in html ? 

Solution :
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/cc4b670a-f51a-4ba3-ae83-401ca22c4c8e)

```html
  <table id="my-table">

   <th>Main Table</th>

    <tr class="my-row">
      <td class="my-col">Name</td>
      <td class="my-col">Class</td>
      <td class="my-col">Roll</td>
      <td class="my-col">Grade</td>
    </tr>

    <tr class="my-row">
      <td class="my-col">Name</td>
      <td class="my-col">Class</td>
      <td class="my-col">Roll</td>
      <td class="my-col">Grade</td>
    </tr>

    <tr class="my-row">
      <td class="my-col">Name</td>
      <td class="my-col">Class</td>
      <td class="my-col">Roll</td>
      <td class="my-col">Grade</td>
    </tr>
    
  </table>
```

```css
#my-table{
      border : 1px solid black;
      font-size: 20px;
      width: 100%;
    }

    .my-row{
      border: 3px solid red;
    }

    .my-col{
      width: 25%;
      border: 1px solid red;
      text-align: center;
    }
```


#### Que- What is Flex or Flexbox system and why it is used ?

Flex Box is basically a box or a system in which whatever elements we add will become inline element (not block). 

initially we had some ways to make newspaper like structure of our website which were:- 
- `position: absolute ` and `left,right,top,bottom` for positioning
- `float: left/right` 
- `tables with rows and cols` 
but there is an issue as whenever a new element gets added in the webpage, it becomes a difficult task to place it at the right position, so to remove this stress we now use a new system `FLEX`

###### Imp Points about About `display: Flex`

- 1. Flex is set on the display property.
- 2. lets say we have 3 elements and we need to place them in same line, then what we can do is simply place all of them inside a container (div).
- 3. Now set containers `display: flex` and suddenly all 3 elements will be inside the container and in same line.
- 4. There is also a `gap: 10px (value)` property which can be used to give space between the elements
- 5. Whenever we set the container's display to flex, what happens is all elements inside that container will become `inline` elements (not block element).
- 6. (VIP) the width of each element inside this flex box container will depend on their contents inside them (more context, more width) (but yes we can change the width)
- 6.2 The height of the container will by default depend on the size of content inside them, for example if we set height of each paragraph tag equal to 200px inside the container, then the container will also increase (but we can change this height anytime ).

![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/94f72b7c-b109-4f0b-9ca2-23fe9778d2de)
breakdown:- 
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/7c43510c-11e2-408b-9d3f-76cf68f7c718)
```html
<style>
        .container-div{
            display: flex;
            gap: 10px;
        }
        .paras{
            margin:0;
            background-color: aquamarine;
        }
    </style>
</head>

<body>
    <h1>Learning Flex-Box</h1>
    
    <div class="container-div">

        <p class="paras">Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore tempore repellendus dicta non facilis alias distinctio quam enim autem cum?</p>
        <p class="paras">Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestias tenetur nobis quos porro unde quaerat? Suscipit vitae sint aperiam, quo alias tempora asperiores repellat perspiciatis illo iure maxime necessitatibus, deleniti cupiditate ipsam architecto sit labore, eum pariatur quam rerum esse ex! Cum modi consequatur fuga qui sed atque eveniet eum.</p>
        <p class="paras"> Lorem ipsum dolor sit, amet consectetur adipisicing elit. Iste, dignissimos? ipsum dolor sit amet consectetur adipisicing elit. Illum nostrum distinctio molestias assumenda odio ad, ipsa exercitationem quisquam labore ab alias atque neque aspernatur iure facere debitis! Fuga voluptatem ullam similique quae velit eveniet voluptate magnam alias, eius quia ex doloremque, in facilis expedita. Saepe</p>
         <p class="paras">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Cumque culpa fugiat, aut dolores, corporis provident at eum nostrum, explicabo similique officia rerum facere!</p>

    </div>
```

lets set width of each `p` to 25% (for 4 paras each)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/2dd45018-ee14-4dca-819d-efda111fe3b8)


- 7. By default this flexbox container will be a block element, but suppose our containers contects are already wrapped in 50% of the width, so we want to use the remaining empty space of the container for other new elements by setting `display: inline-flex` (by doing this now the container's width by default will be equal to the content provided inside it), any other new element can also adjust in the remaining space.
- So basically inline-flex is used when we want our container and all inner child elements to have width = content present inside them

example1:- 
container's 

`display: flex`
note: each one of them inside the container are div 

![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/b68007f6-ab4a-4579-9d96-2907ce7fc785)

container's display: inline-flex
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/c6d1ddca-9614-4349-a442-42a4f354c322)

example2:- 
container's `display: flex`:-
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/66ae44a3-02be-4c9e-850b-5e4119f48c10)

container's `display: inline-flex` :- 
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/86da1c0d-e49a-440b-ae46-e3c1f20b2fbc)

Code:- 
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/2b8665d8-9e38-4f17-9237-3e2e152e8ad5)


more examples:- 
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/8b4408bc-ad57-4d9c-b431-d6160c0bf062)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/9acc3444-6fe0-4439-81a6-4a977bd893c1)

note: 🔍now using this flex box we can very easily create nav bars, we will not have to use all those float, positioning and display:inline/block, etc. properties


###### Que - Create a navbar using only `display:flex` (do not use float, position, and other display values).

![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/0db6f885-7c07-40e2-a859-83db8a1aa0cb)

Breakdown :- 
![Untitled (5)](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/c8ed0558-20bb-4390-9176-00e47a81fc81)

code:- 
- By creating a div container, and inside that we have 4 anchor tags
- set display of container to flex
- after setting it to flex by default container will be block element.
- give all anchors width of (25%) each, now center their text using `text-align: center`
- give background-color of container, now increase the font size of the 3 anchors and the height of the flexbox will set itself accordingly.
![Untitled (6)](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/34f345bd-bba3-4d42-869a-460bab3e9a91)


--------

## Module 9.2 (Flex-direction, Flex-Basis, main axis, crossaxis)

##### Que - What is `flex-direction`?

- it is a property of 'flex-box', which specifies that in which direction the new elements inside the flexbox container will be added.

by default (flex-direction is = row)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/d64d9331-0b14-4d7a-868c-a14ebdf228c4)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/fc81ece4-b4b2-41ee-878a-5b708cdeb367)

when we set `flex-direction: column`
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/44bdca8a-0a32-4618-b850-4d1e999da9f1)

- It is set on the parent (.container) element
- it's values: `flex-direction: row` and `flex-direction: col`. 
- By default flex-direction is always set to row.
- There are 2 axis in flex box 1) main-axis 2) cross-axis.

When we set `flex-direction: row` all elements will be added in same row (untill its full)
i.e `main-axis` will move from left to right and `cross axis` will move from top to bottom.

When we set `flex-direction: co`l all elements will be added in same col (untill its full)
i.e `main-axis` will move from top to bottom and `cross axis` will move from left to right.

![Untitled (10)](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/e17ace57-733d-4ca8-9673-c590d3535abc)
![Untitled (8)](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/7b8d053d-a52c-49c9-827a-734a38084c86)



##### But Why are these main-axis & cross axis important ?

Because There is another property `flex-basis: size `  which we set on the containers child elements (or inner elements or items )

When we set containers (parent's) `flex-direction: row`  (i.e main axis from left to right) 
now when we set child's `flex-basis: 100px`  then the width of all inner elements will increase to 100px (width because main axis is now left to right)
![Untitled (12)](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/02a0046b-a551-4149-877c-841da124f0f5)


When we set containers (parent's) `flex-direction: co`l  (i.e main axis from top to bottom) 
now when we set child's `flex-basis: 100px`  then the height of all inner elements will increase to 100px (width because main axis is now top to bottom).

![Untitled (13)](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/0b395398-8268-4116-bec9-86acc16690b9)


Que - Also What if we use display: inline-flex here? 
Ans - then the element will take only that much width which is required for the content inside them
 
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/0ba8103c-9bd0-4906-90f9-658b20ae8e04)


Que - Explain all of the 'flex-directions' with example. 
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/8fd16080-49cb-437e-91fe-713cd7e27ae2)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/92cc0ab8-5b0f-49a7-8b56-551cd1ac129f)

## Chitkara University (Homepage) - Clone 
i created a clone of CU Website homepage (not exact but yes many changes)

![chitkara clone - first look](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/a8629ae3-3777-4698-a240-3b7bb8d9cb8b)

```html
<!-- H T M L  Code -->

<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CU Clone</title>
    <link rel="icon" href="./assets/pictures/chitkara-logo.png">
    <link rel="stylesheet" href="./style.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">

    <!-- fonts from google -->
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
	<link href="https://fonts.googleapis.com/css2?family=Varela&display=swap" rel="stylesheet">
	<link rel="preconnect" href="https://fonts.googleapis.com">
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
	<link href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400&family=Varela&display=swap" rel="stylesheet">
</head>

<body>

    <div class="navbar-container">
        <a href="#" class="navbar-anchor">Admissions</a>
        <a href="#" class="navbar-anchor">Courses</a>
        <a href="#" class="navbar-anchor">Fees</a>
        <a href="#" class="navbar-anchor">Reviews</a>
        <a href="#" class="navbar-anchor">Placements</a>
        <a href="#" class="navbar-anchor" id="contact-us-anchor">Contact Us</a>
    </div>

    <!-- chitkara logo -->
    <div class="main-logo-container">
        <img class="chitkara-logo-img" src="./assets/pictures/chitkara-logo.png" alt="chitkara logo">
    </div>

    <!-- chitkara campus img -->
    <div class="campus-pic-container">
        <img class="chitkara-campus-img" src="./assets/pictures/campus-img.webp" alt="">
    </div>

    <!-- courses cards  -->
    <div class="courses-cards-outter-container">

        <div class="courses-cards-inner-container">

            <div class="course-card">
                <h2>BTECH</h2>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates, repellat.Lorem ipsum dolor sit amet consectetur adipisicing elit. Nesciunt, nihil! Perspiciatis similique, quis inventore officia magnam soluta blanditiis recusandae dolores suscipit, veniam dolorem quam Culpa molestiae id maiores accusantium laudantium.</p>
            </div>
            
            <div class="course-card">
                <h2 class="course-card-heading">BBA</h2>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Animi blanditiis explicabo eos libero minus officia deleniti assumenda laboriosam impedit vero sed vel cumque officiis quisquam facere sunt atque dolore eius dolorem soluta ipsum maxime, temporibus possimus. Adipisci, iure. Quos, incidunt?</p>
            </div>
            
            <div  class="course-card">
                <h2>MBA</h2>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Corrupti, sapiente labore vel inventore architecto asperiores molestias iste incidunt aperiam, optio voluptatum voluptatem ut totam iure suscipit autem aspernatur. Accusantium nisi eveniet quo magnam sequi optio nulla odio nobis itaque est.</p>
            </div>
            
        </div>
        
    </div>

    <!-- footer -->
    <footer class="footer-container">
        <iframe class="chitkara-gmap" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d184821.4673014666!2d76.60220702728469!3d30.599150057419063!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x390fc32344a6e2d7%3A0x81b346dee91799ca!2sChitkara%20University!5e0!3m2!1sen!2sin!4v1690727333097!5m2!1sen!2sin" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        <p class="footer-para">
            © 2023 CU Clone by Yashasvi
        </p>
    </footer>

</body>

</html>
```

```css
/* CSS CODE */

body{
    margin:0;
}


/* ------NavBar Styling-------- */

.navbar-container{
    /* border: 1px solid black; */
    background-color: #d00000;
    display: flex;
    flex-direction: row;
    /* gap: 10px; */
}

.navbar-anchor{
    text-align: center;
    color: white;
    text-decoration: none;
    font-size: 18px;
    width: 16%;
    margin-top: 10px;
    margin-bottom: 10px;
    font-family: 'Varela', sans-serif;
    /* border: 1px solid pink; */
}

#contact-us-anchor{
    margin: 0;
    /* border: 1px solid white; */
    background-color: rgb(247, 247, 79);
    color: black;
    padding-top: 8px; /*just to center the anchor*/
}


.navbar-anchor:hover{
    color: rgb(0, 255, 234);  
}

#contact-us-anchor:hover{
    background-color: rgb(43, 100, 93);
    color: rgb(241, 241, 241);
}

/* --------Chitkara center main logo-------- */

.chitkara-logo-img{
    height: 200px;
    /* border: 1px solid black; */
    width: 70%;
    margin-left: 15%;
    margin-right: 15%;
    object-fit: contain;
}

/*--------- chitkara campus img ---------*/

.campus-pic-container{
}

.chitkara-campus-img{
    width: 90%;
    margin-left: 5%;
    margin-right: 5%;
    border-radius: 40px;
}

/* ----------courses cards------------ */
/* note i created 2 containers because, it is difficult to center 3 divs inside a single container,but using 2 containers, what i did is i centered the inner container (width:80% leftpush:10% rightpush:10%) and inside this inner container are my 3 divs (Cards), then i applied flex-row on the inner container

 */

.courses-cards-outter-container{
    padding-top: 40px;
    padding-bottom: 40px;
    width: 100%;
    /* border: 1px solid black; */
    background-color: #f5f5f5;
    margin-top: 20px;
    margin-bottom: 20px;
    gap: 20px;
}

.courses-cards-inner-container{
    width: 80%;
    margin-left: 10%;
    margin-right: 10%;  /*to center this inner container(which is inside outer container)*/
    /* border: 3px solid rgb(211, 25, 25); */
    display: flex;
    flex-direction: row; /* so that we can fit the 3 cards equally inside the inner-container*/
    gap: 20px;
}

.course-card{
    flex-basis: 33%;
    /* border: 1px solid black; */
    background-color: white;
    border-radius: 20px;
    padding: 10px;    
    text-align: center;
     font-family: 'Open Sans', sans-serif;
}

/*------------- footer maps--------------- */

.footer-container{
    background-color: black;
    height: 300px;
    width: 100%;
}

.chitkara-gmap{
    width: 60%;
    margin-left: 20%;
    margin-right: 20%;
    margin-top:40px;
    height: 150px;
    border-radius: 20px;
}

.footer-para{
    text-align: center;
    color:white;
    font-family: 'Open Sans', sans-serif;
    font-size: 13px;
}
```

------------------------------------------



## Module 9.3 (Flex-Layout)

There are a lot of properties to set the different layouts for a flexbox items
```css
- order : value;
- flex-wrap : nowrap | wrap | wrap-reverse;
- justify-content: flex-start | flex-end | center | space-between | space-evenly |space-around
	/*used on main-axis */
- align-items : (works on nowrap)
- align-self: 
    /* used on cross-axis*/
- align-content : (works on wrap) 
```

##### 1. `order: ` of flex 

- this property is set on the child element always (whose order we want to change).

By default the order of items inside flexbox container is 0, so that is the reason that when we add new elements in the container, they add on from the end of the flex (if flex-direction is row, then flex-end will be right most), and element will keep on adding in this order . Once the line is full, then elements will add in new lines.

now what if we do not want this default behavior rather we want some item/items to be in different order then we can use this `order: ` property to set order of that item  
![Untitled (15)](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/c64328ce-5898-4bd0-aeba-9273e976b1af)

##### 2. `flex-wrap: wrap | nowrap | wrap-reverse`

- It is basically used to make sure that whether the child's inside parent container should  wrap or not when the screen size hits their width;
- this property is set on the parent container always.

###### flex-wrap: nowrap
by default every flex-box container has `flex-wrap: nowrap` set.
here when the screen size hits width of the child element in the corner, then all the child elements inside the flexbox container will start to shrink.
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/6f826c7a-b006-4469-b72b-61ac12e0ad9e)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/54fb32ff-7114-4456-95ba-3ffe703230b3)

###### flex-wrap: wrap;
if we set `flex-wrap: wrap` then whenever the screen end hits the last child element's width ,then it will go on to the next line of the container, and if we continue to shorten the screen then each element will go on to the next line untill we stop decreasing.
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/e155838c-f985-420d-ab54-29afc1fe0b2d)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/5687762b-f72a-4d04-b21d-d3443bac9fb7)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/e1c684c0-b149-4868-b9da-79a08f47aa99)

###### flex-wrap: wrap-reverse
this will do the same thing but in order bottom to top, i.e when the screen shrinks the item (child) will go a new upper line.
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/244465c9-dd96-476b-9141-b4b07e6be90f)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/a86b8907-eb44-4c65-923a-107bc2c1061c)

##### 3. justify-content : 
- This property is used to define the position of the items (child) in the center
- (I M P) works both on `wrap` and `nowrap`  
- It is applied on the parent (container) element always 
- It works always as per the main axis.
- (I M P) If the main axis is from left to right then the `flex-start` is left corner, `flex-end` is right corner. and if the main axis is from top to  bottom, then `flex-start` is top and `flex-end` is bottom.

values -> flex start, flex-end, center, space-between, space-around, space-evenly.
center:
```
flex-start: (by default 'left' for flex-direction: row) and ('top' for flex-direction: column) 

flex-end: vice verca of flex-start 

center : it is one of the best ways and easiest to center items inside a flex-box container

space-between: all items will have equal space only between them 

space-around: all items will have its on margin (space) on their left and right corners, and                also at the start and end  

space-evenly: equal spaces between elements and start and end as well.
```

![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/b60be14b-549f-4a05-a8fe-079a0a78cd78)

Que - What if items is not only in 1 line, then how will this 'justify-content' work?
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/b82ea483-b56b-4150-959b-c6508ab47a09)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/4323ca30-20b9-48bb-a9d5-05a90bbc3bf8)

##### 4. align-items : 

- This defines the default behavior for how flex items are laid out along the `CROSS Axis`
- Think of it as the `justify-content` version for the cross-axis (perpendicular to the main-axis).
- works only in `flex-wrap: nowrap`.  (of flex-wrap property) because if we wrap then items will go to next line.
- if `flex-direction: row` that means main axis from left to right and cross axis from top to bottom , so in that case `flex-start` is the top and `flex-end` is bottom end of the container.

![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/fb608470-51a4-41ab-804b-e6a5adb0cb33)

![screeeen](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/c2286a50-64b2-426e-936d-82b4604d592b)

###### What is `vh` and how it is used as a unit for height ?
`vh` means viewport height, viewport means height of screen so if we write `height: 70vh` then height of our element will set to 70% of the total screen's height.


##### 5. align-content 
- works in cross axis
- works on `flex-wrap: wrap` 
- works even with multiple lines of items.

![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/da58a0f1-ae51-425f-8c31-0b495ec4a2e8)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/b78ffe70-cd40-44b5-be03-2ab9ca6f1666)



Que - How to reverse the order of the items inside flexbox container ? 
Ans - using `flex-direction: row-reverse;` or `flex-direction: column-reverse`;
```css
.container { flex-direction: row | row-reverse | column | column-reverse; }
```
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/a343b700-3771-4412-9884-f578b8755379)
Notice : that when you set the direction to a reversed row or column, start and end are also reversed.




## Module 9.4 (Flex Sizing)

By default when we create lets say 4 div then they will be block elements, as soon as we put them into a flexbox container, then the div items will become inline element, now when we reduce the width size of this container, the div items will also start to shrink (as soon as the with of container hits the last element of the div items)

In most cases this is what we want, i.e we want out items to shrink, but sometimes we want a different type of sizing, so for that we can customize the sizing which will be based on the priority basis :- 

```md
 content-width < width < flex-basis < min-width/max-width
```

###### 1. content-width 
when we compress the container, then the min width of div item will be equal to the width of longest word of that div items, and max width will be equal to the width of all content combined inside that div item

![asdf, smdf s](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/a5f90650-5a8f-45db-b02f-6e18f9456306)

###### 2. width  
when we set width of items to lets say 100px, then all inner div will have width of 100px initially but if we shrink the container div to an extent that it hits the last item div then, the items will start on shrinking again.

###### 3. Flex-basis
- applied on container

We already learned flex basis earlier that it works on the (main-axis) always. 
flex basis has more priority then the normal `width` and `content-width`. 
so if we set the `fkex-direction=row` and  `flex-basis` to 100px then  by default the width will be 100px. now if we shrink the view port width, and if it hits the last div, then it will start to shrink again and this shrinking will stop ones the width of each item div reaches the `content-width`. 

###### 4. min-width/max-width

- (IMP) these properties are applied on the child items (not the flexbox container)

note: if we apply these properties on the `container{}` div then it will not work for the items, it will work for container only, so use these properties on the child elements

`Max width` property is maximum possible width of div items, now 
if max-width: 100px and flex-basis: 50px then div items will have width of 100px 
if max-width: 50px and flex-basis: 100px then div items will have width of 100px 

similarly if min-width is larger then the flex-basis then `min-width` will be respected

**by default** for a `<div> This is an item of Flexbox</div>`
- min-width will be equal to the width of longest word in the item i.e. `Flexbox` .
- max-width will be equal to the width of complete content inside that item

![Untitled (17)](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/210c6573-b1a1-4003-9b6f-27d132755c5e)

###### What is `flex-grow` & `flex-shrink` ?
- applied on the `items` 
Flexbox mainly works on its flex-grow and flex-shrink property, lets understand it better:- 

1. lets set `flex-grow: 0` and `flex-shrink: 0` then the width of each item will be equal to the `flex-basis` value always, and items will neither grow nor shrink, i.e even if we reduce the width of view port then items will not shrink.
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/95d30e48-2a04-4576-a38f-d42e363416b9)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/59765ddf-63b2-4757-b6d9-e64b85642665)


2. lets set `flex-grow: 1` and `flex-shrink: 0` then in this case the width of each item will first adjust according to the flex-basis, but because it is allowed to grow then it will grow and each item will have equal width with no space left out in the container div, but as we shrink the view port width, then it will only shrink till `flex-basis` set items
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/8e733c3d-cfd8-4b40-87b0-fbb4d92ce24f)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/12013cd4-014f-47c7-960c-35cbdaa03c4f)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/a9afdea4-fa68-4d30-a773-e90b0ff75a9f)

3. lets set `flex-grow: 0` and `flex-shrink: 1` then in that case again the width of each item will start with flex basis i.e 100px here, then since it is not allowed to grow so the width will stop at 100px but it is allowed to shrink that means if we reduce the viewport width then items will shrink till the `min-width` which is by default equal to the longest word's width inside each item 
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/87541016-bfe0-4d18-a18d-89fe1b7082e2)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/efeff584-6f58-4b83-82e4-37789ddeba16)

eg.2
notice below that the width of each item will first be 100px (flex-basis) but as the min-width by default is equal to the width of longest word in each div item then the 2nd div will grow till its min-width (min-width is the width from which the div item stops to shrink)

![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/179cc681-f33e-4f66-8d64-43886f6d617c)

![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/3fa658d3-b299-4be6-aca8-961a0419fda5)

4. Lets set `flex-grow: 1` and `flex-shrink: 1` then in that case first the width of each item will start with 100px (in our case) but for 2nd div it will be more (as discussed in previous example) and because it is allowed to grow, then each item will fill up the remaining space in the container equally, and also when we reduce the viewport width, then since it is allowed to shrink, then each div item will shrink till it reaches their min-width (not after that).
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/e6c3ca82-816a-434f-a652-dc4239506840)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/d459b953-06a6-4257-9162-cb73271e53d9)

note: in case we have not set the flex-basis property, then by default the width will shrink till `min-width` and grow till max-width
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/9528927d-8d6c-4bc0-aafd-c6dfc06e398b)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/f5e56349-f8aa-45a1-b77d-2069d3df7933)


###### what is `flex-basis: auto`?

By default flex basis is always `auto` and what it does is that inside the flex-box the width of each item will be given according to the amount of content provided inside them.

(IMP) if we do not want that then, and want all our items to have equal width then set `flex-basis: 0`; `

![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/411a9042-4646-4e82-8922-2ad2293a9955)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/3edd26bc-5b1e-4a64-b7d7-3f6c3e319cc9)

###### Que - What is short hand way to write these flex properties?

```css
.items{
	flex: 1 1 0;   /* grow:1 shrink:1 flex-basis:0 */
}
```

```css
.items{
  flex: 1 0 100px; /* grow:1 shrink:0 flex-basis:100px */
}
```

```css
.items{
	flex: 1;    /*grow,shrink,flex-basis all with value 1*/
}
```

###### How to give with of each item, relative to the other items using `flex`?
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/e93a9f2f-fbef-4a7c-bc6b-eba334886f9b)
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/edf07628-f8ad-4eac-ae0f-763cad9c85d3)
This will divide entire width into 1+5+10 => 16 columns and allot 1st col to 1st div item, next 5 to 2nd div and remaining 10 columns space to last div item.
note: it is responsive.
![image](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/c057c630-0c92-4f85-bb1e-67b4a78d824a)

Exercise to practice flex-sizing : [https://appbrewery.github.io/flexbox-sizing-exercise](https://appbrewery.github.io/flexbox-sizing-exercise/) 

---------
