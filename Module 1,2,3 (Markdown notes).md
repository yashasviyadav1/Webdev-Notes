
## Module 1.1

### What is Internet and how it works?
A vast network that connects a system to all over the world, through which systems can communicate with each other.

A computer which accesses the internet is a client.
A computer which helps client to access resources and data from the internet are called servers.


### What happens when we search a website.
When we type a website name from the client computer, then the req is sent to our Internet service provides (ex. Jio, Airtel)  and then ISP sends the req to DNS (Domain name system) which is just like a phone book, which keeps track of all the website and their IP addresses and then DNS finds the right IP of the website we req and sends back to ISP, then ISP searches for that IP over the internet and thats how we access a website.

![img](https://i.postimg.cc/x1Jm2Y2V/Pasted-image-20230717194737.png)
Check Out [nslookup](https://www.nslookup.io/) to find IP of any website 

### How all countries are connected to internet ?
via under sea cables (massive fiber optic cables)

![img](https://i.postimg.cc/L5J919vH/Pasted-image-20230717195713.png)
source : [submarinecablemap](htps://www.submarinecablemap.com)


## Module 1.2

### How a website is rendered ?
When we type lets say `www.google.com` what really happens after the ISP, DNS. thing is that the website that we types will send us all data of its webpage, i.e. 3 types of files `html, css, js`
and then using a browser, all of the 3 files gets loaded 1 by one and at last we see the complete website.




# Module 2 (Notes)

## Module 2.1

### HTML
Hyper Text Markup Language, where Hyper Text means a text which links to some other part or text, where as Markup is used to tell user/ reader that something is imp or highlighted (which we do using html tags).
<b>Some of most imp html tags :- </b>
![img](https://i.postimg.cc/m2bngXXr/Screenshot-2023-07-17-203503.png)



## Module 2.2

### Difference between HTML tags, elements, attributes, values ?

- Tag is basically what's inside the angle braces `<>`
- Element is the complete part starting from opening tag till closing tag. `<> abc </>`
- Attribute is the property of a tag `eg. value="10" color="yellow"`
- value is the value of that property

![img](https://i.postimg.cc/bNSjhFs2/screenshot-www-udemy-com-2023-07-17-20-41-02.png)
`<>` are called angle brackets
![img2](https://i.postimg.cc/FF2S4pKp/attribute.png)



### Heading Tag 
Heading's go from 1 to 6 where 1 is the max font size and 6 is the least font size.
```html
<h1> Heading </h1> <!-- largest-->
<h2> Heading </h2>
<h3> Heading </h3>
```


### Paragraph Tag 
a paragraph is a distinct section of a piece of writing, usually dealing with similar theme.
a new paragraph always starts in a new line.
![img](https://i.postimg.cc/ncy3J7MB/yesssssss.png)


## Module 2.3 

###### Void Elements ?
Void Elements are also called self ending elements ex.
`<br />` break tag ends a line 
`<hr />` horizontal row tag creates a row horizontally 
`<img /> `insert images 
<i>note :  it works even with and without /</i>
![img](https://i.postimg.cc/kG50R7Xd/yesssssss.png)

## Module 2.4

##### Creating a collection of best movies 
![img](https://i.postimg.cc/JzzjYqRx/yesssssss.png)

## Module 2.3 

### What is a List tag ?
there are 2 types of lists 
- ordered list 
- unordered list 

Ordered list items is in order (ranking starts from 1 by default)
Unordered list items are represented by bullets (default is a circular filled bullet)

![img](https://i.postimg.cc/MZghJqtM/yesssssss.png)

##### How to change the default bullets styles of list items ?
there are 2 ways to do this for ordered lists :- 
- 1. by setting `value` attribute to an int .
- 2. by setting `start` attribute to an int.
![image](https://github.com/yashasviyadav1/DSA-Questions/assets/124666305/3bbe081f-785d-4e3b-9724-8396afc6ca66)

and for unordered list :- 
- 1. set `list-start-type = any style` (in styling)
![img](https://i.postimg.cc/vBj1YcS6/yesssssss.png)

##### Nested List 
![img](https://i.postimg.cc/PqyGw593/yesssssss.png)

## Module 2.4

### What is an Anchor Tag and its attributes?

This tag defines a hyper link which is used to link pages with each other
its attributes are `href="www.google.com"`  (used to link website or other webpages) and `target="_blank"` which is used to open a new tab ones the link is clicked

attributes :- 
```html
href=""
target="_blank" 
download   (makes the link downloadable, usefull for pic and pdfs)
```

![Downloadable](https://i.postimg.cc/Zqmfb3TB/download1.png)
<i> note : When this above link is clicked the .txt file mentioned is downloaded</i>

![img1](https://i.postimg.cc/YSvvthPB/yesss-2.png)

![img2](https://i.postimg.cc/cJPrCdqg/yesssssss.png)
##### Que - How to jump to a specific section on the same page using anchor tags? 
Ans - all we need to do is instead of inserting link, just put the `<a href="#id">` where this id is the id of the specific `<p>` or maybe the `<div>` tag that we are targeting 
<i> example :- </i>
![img](https://i.postimg.cc/65S7v2pM/download1.png)


## Module 2.5

### What is an Image `<img>` Element ? 

image element is used to insert images into webpage. It is a void Element (self ending).

Here is a a Lorem Epsum type website for images :- [picsum.photos](https://picsum.photos/)
Just write picsum.photos/`size or seq in pixels`
eg. 

![200 px pic](https://picsum.photos/300)
source = https://picsum.photos/300

##### Que - How to embed google maps into webpage ?
Ans :- 
step1 : search for that location in google maps
step 2 : click on share
step 3 : go to embed link and copy the code, then paste this into `html`
![img](https://i.postimg.cc/NFQfrnLc/download1.png)





