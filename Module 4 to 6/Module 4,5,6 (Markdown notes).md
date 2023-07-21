
## Module 4.1 

#### Q - Difference Between Absolute and Relative Paths.

<i>Absolute path </i> :- is the path that makes no assumptions about your current location in relation the the file u are describing.

<i>Relative path :-</i> is always relative to current folder.

2 imp character in relative paths :- 
- `./abc` means in current folder search for abc.
- `../abc` means in parent of the current folder we are in, search for abc.

![image](https://github.com/yashasviyadav1/Searching-Sorting/assets/124666305/177b135a-31a7-466f-817d-7e1f50abf8c0)


![img](https://i.postimg.cc/wMBxtSfm/download1.png)

## Module 4.2 

##### Q - link Webpages using paths and anchor tag.

![image](https://github.com/yashasviyadav1/Searching-Sorting/assets/124666305/99c8dbb5-ae09-42f3-a12f-45fd4668c04b)

Que - how to remove underline from anchor tag's font ? 
Ans - By setting its `text-decoration :none` 

Que -how to change the cursor style? 
Ans - By setting its `cursor : default/move/etc`

# Module 5 (Intro to CSS)

## Module 5.1
###### CSS - Cascading Style Sheets 
Cascade means a small water fall
the way a style is applied, based on their priorities and specificity
is why its called cascading style sheets.

###### 3 Different types of CSS :- 
- Inline CSS
- Internal CSS
- External CSS

Inline CSS : It is useful for cases where we want to style a specific section or line with a particular style 
![screenshot-www udemy com-2023 07 20-07_45_02](https://github.com/yashasviyadav1/Searching-Sorting/assets/124666305/ee2d2eb8-5da5-4298-b228-59fa118afa25)

Internal CSS : used when not much styling is required, also useful in single page websites.
![paths](https://github.com/yashasviyadav1/Searching-Sorting/assets/124666305/03bcf0d4-007f-49b6-a6e7-25f35c92b0d7)

External CSS : used when a lot of styling is required, so we separate the styling part from the html code, also useful for multipage websites.
![screenshot-www udemy com-2023 07 20-07_50_19](https://github.com/yashasviyadav1/Searching-Sorting/assets/124666305/41339e27-b787-41b9-b07d-8f3f111430a5)
link a stylesheet :- 
```html
<link rel="stylesheet" href="./styles.css"> 
```


## Module 5.2


#### CSS Selectors :- 

1. element selector - selects all occurrences of an element for styling
![screenshot-www udemy com-2023 07 20-08_44_38](https://github.com/yashasviyadav1/Searching-Sorting/assets/124666305/665fac3b-0cb7-4cea-a5b9-dc2ce312ddbf)

2. Id selector - selects elements with given id 
![screenshot-www udemy com-2023 07 20-08_47_26](https://github.com/yashasviyadav1/Searching-Sorting/assets/124666305/e0665ab4-bb69-4232-b340-8429739c9f28)

3. class selector - selects all elements with given class
![screenshot-www udemy com-2023 07 20-08_46_34](https://github.com/yashasviyadav1/Searching-Sorting/assets/124666305/aff5529c-031c-490f-b770-8d4d40d9fcf9)


4. Attribute selector - selects an element based on presence of given attribute or attribute with given value 
  - 4.1 using only attribute name
![screenshot-www udemy com-2023 07 20-08_49_10](https://github.com/yashasviyadav1/Searching-Sorting/assets/124666305/1d0589aa-bcd8-414c-843a-0ba54272ae6e)
   - 4.2 using attribute name with value
![screenshot-www udemy com-2023 07 20-08_50_43](https://github.com/yashasviyadav1/Searching-Sorting/assets/124666305/d4f59ce4-801c-4845-ae75-a734ba48dfa6)

1. Universal Selector - `*` selects all elements and apply style to them
```css
*{
	color:blue;
}
```

###### Difference between id and classes ? 

<b> Id </b> is unique identity of a element. For ex there is an element `<div id="me"></div>` in a single HTML doc, there should be only 1 element with id 'me' no other element should have that id, because it is technically wrong in programming.

<b> Class </b> whereas more then 1 element can have the same class

note : <i> ids are represented by # and classes by . </i>




# Module 6 (CSS Properties)

## Module 6.1 

Question - How to find the right color combinations or color palette for your website Or How to find the for your custom color?

![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/b7cd8112-5a7d-430b-bd95-0925b8a1e5e1)
source : [csfieldguide.org](https://www.csfieldguide.org.nz/en/interactives/rgb-mixer)

![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/7672296a-6b32-490b-ba7e-8b8bb087cc64)
source : [colorhunt.co](https://colorhunt.co/)

## Module 6.2

### Font Properties :- 
```html
color  (changes font's color)
font-weight  (changes font's weight i.e normal, bold, etc)
font-size  (changes size of font)
font-family (changes font)
text-align (position of text - left, right, center)
text-decoration ('none' will remove underline from the anchor's font)
```


Question - What are different  units for font size ? 

1. `pixel (px)`   is 1/96th of the inch 
2. `point (pt)` is 1/72nd of inch (used in MSword)
3. `em`  is basically relative to the parent 
	- eg. 1em means 100% of parent
	- eg. 2em means 200% of parent 
4. `rem` is basically relative to the root (`<html>` tag)
	- eg. 1rem means 100% of root
	- eg. 2rem means 200% of root

Question - How to find best fonts ? 

![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/7a4bef29-8543-45ea-b4d1-6aad6e8ef640)

Question - how to use a particular font family from google fonts in ur html?
Answer - By copying the code below, and pasting it into the `<head>` and by copying the CSS rules given below and pasting them into the text's styles we want to change for.
![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/a6ba24ba-d194-4e3d-9f58-6b4b633097a2)
![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/d4d49edd-2c84-41d7-a8cd-09de9ccd521b)



## Module 6.3 (CSS Inspection)

Que - How to set height and width of an element (eg. p or div)

height and width can be set in 2 units, `%` or `px` .
using px we define that how many pixels of height or width we want for our element, and by % we tell the how much % of the screen we want to our height and width.

note : when we increase height of an element, then it pushes the other element's on top and bottom (if any).
![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/a843fd86-927c-4ed8-968c-b85a2f47943e)

![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/bccebade-4dab-4c86-bf4d-2a0692b240ad)



Que - what happens when we change the border's thickness?

When we change the border thickness of a box, then only the thickness increases or decreases, it will not effect the height and width of the box whose border we are changing.

![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/4789fc03-6333-4031-a057-32f3a56f5cf4)


Que - How to set different border width for left, right, top, bottom ?

By using `border-width` property, which can have 4 different values for `top, right, bottom, left` (simply clockwise).


![screenshot-www udemy com-2023 07 21-19_58_15](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/b5097981-dbfc-4bb5-9024-e3ea2859e6a5)

Que - What happens if there are only 2 values for border-width ?
![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/7fd3c94e-5c27-47bb-a8e4-410ea88e06a9)


Que - What happens when there are only 3 values for `border-width` ?

![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/7f901da5-1c6e-4497-94cc-7b6fd1a72dd7)


###### What is `Padding & Margin` of an element?

Padding adds space between a box and its border (note that it doesn't change size of the box)

Margin adds space between the border of a box and its outer element.

![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/8298dae7-005e-4749-badc-96fcecb9231b)

![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/a6436413-5454-4327-9fed-7906bb0bec8b)

Que - How to see how invisible elements like div, para are grouped together ? 

Use chrome extension 'pesticides'.
![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/7e3238ce-19b7-4aea-ab5c-21566e3499e2)

Que - What is Box model in html and CSS ?

The CSS _box model_ is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding and height/width.

![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/15471757-2b60-4697-9337-e4319ba5308f)

Below is a good exercise for practicing the 'margin' and 'padding' :- 
[6.3+CSS+Box+Model (1).zip](https://github.com/yashasviyadav1/DSA-Questions/files/12130222/6.3%2BCSS%2BBox%2BModel.1.zip)



