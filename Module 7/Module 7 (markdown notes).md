
## Module 7.1 (Specificity & Inheritance )

### Specificity & Inheritance 
Suppose there is an element `<div>` and style `background-color` is applied to this div
at different places (in inline css, external, internal, and at different positions), now which one all will be applied to this div? 
the answer to this question will be it will be decided by the specificity and inheritance rules... 
![specificity](https://github.com/yashasviyadav1/Webdev-Notes/assets/124666305/b0afa7b7-ee55-427b-abb3-05e4884f7eb9)

here the lower one will be applied at the end.

<i>Here is a activity to practice what we learned till now (padding,margin,color,selectors,specificity, etc) :-  </i> [try-me.zip](https://github.com/yashasviyadav1/Webdev-Notes/files/12159901/7.0%2BCSS%2BCascade.1.zip)




## Module 7.2 (Combining Selectors)

#### Ways to combine selectors :-

###### 1. Grouping Selectors  
In this all selectors are separated with commas, and style is applied to all selectors mentioned below 
It is mainly used when multiple elements have same styling.
```css
selector1,selector2,selector3...{
	color: blue;
}
```

###### 2. Child Selectors
This is used to select 1st occurrence of mentioned child element with help of parent element and this is applied only 1 level deep (i.e. only to child, not grand child)
```css
selector1 > selector2{ /* selector1 is parent, selector 2 is child */
	color: blue;
}
```

###### 3. Descendent selectors 
```html
<ancestor>
	<descendent>
```
This can used to select a child, grandchild or any level deeper element for a parent. 
```css
selector1 selector2{ /*selector1 is parent, selector 2 can be child,grandchild or any element present any level deeper to parent*/
	color: blue;
}
```

###### 4. Chaining Selector 
This is used to select `very specific` element. here $1^st$ the element's name goes then the id or class, etc.
useful in cases when more then 1 element have same class or name
for eg.
```html
<div class="box" id="yes"> Hellow </div>
<div class="box"> Hellow</div>
```

```css
div.box#yes{
	color: blue;
}
```

###### 5. Combination of Combiners (all 4 mentioned above)
These are any combination of all 4 types talked above 
ex.
```html
<ul>
    <p class="done">Other items</p>
</ul>
```

```css
ul p.done{ /*go inside ul, if any level deeper a 'p' is found with class .done, then grab it*/
    font-size: 0.5rem;
}
```

--------


## Module 7.3 (CSS Positioning)

In CSS, there are 4 ways to position an element :- 
1. Static
2. Relative 
3. Absolute
4. Fixed

###### 1. Static Positioning
This is the by default position of each element in the html, if we do not give a position to an element then it is always static, in this the element is always placed underneath the previous element 

In static positioning even if we give a push of `top: 10px ` or maybe `bottom:20px` then also it doesn't move
![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/a07d2c75-2fe2-41f3-a20b-b2e33d60158f)


###### 2. Relative Positioning
In this the new position of an element is relative its current position.
![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/a7047756-12e2-4955-8eaa-8c83a1fd594c)

###### 3. Absolute Positioning 
In this the new position of an element is relative to the nearest ancestor. (immediate parent)
note : <i> for an element to be relative to its nearest ancestor element, make sure to set nearest ancestor elements position to `relative` or `absolute` .</i>
![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/45f463ce-e281-4a2b-b017-9a49437e7c81)

note : <i> If that element do not have a nearest ancestor or maybe its ancestors position is not relative/absolute then in that case the new position will be relative to the top left corner of the web page.</i>

 Z Axis :- <i> Every element has by default value of z axis set to 0, but in case of element with pos : absolute, the element will be shown above all other elements (when its z-axis value is 0)</i>

###### Fixed Positioning 
In this the element's new position is always relative to the top-left corner of the browser (not webpage) so it will always be sticked to the same position even if we move the cursor.
![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/cf77cc7a-b825-4758-b1b6-646ee83d99c7)

Practice positioning :- [7.2+CSS+Positioning.zip](https://github.com/yashasviyadav1/Web-Dev/files/12162612/7.2%2BCSS%2BPositioning.zip)

-------


## Module 7.4 (Flag of Laos)

Here I created Flag of Laos using html + CSS.

Try this activity : [FlagActivity.zip](https://github.com/yashasviyadav1/Web-Dev/files/12163008/7.3%2BFlag%2BProject.1.zip)

My Solution :-

![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/9fdfd006-82b5-47b8-a1a2-90d368dc6657)

![image](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/6796bb1e-869d-4317-8302-8501fbf20587)

![Webdev](https://github.com/yashasviyadav1/Web-Dev/assets/124666305/ccd24070-232b-4a1f-a1ce-949132545185)


  ---------
  