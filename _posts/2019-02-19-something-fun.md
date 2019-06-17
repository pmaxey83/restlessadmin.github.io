---

layout: post
title:  "static content says #1"
date:   2019-02-19 16:18:00 -0700
categories: [personal,tutorial]
tags: [markdown,html,css]


---

![photoGallery](/assets/screenshot-2019-2-19photogallery.png "Photo Gallery")
##### **While taking Colt Steele's Udemy course, ["The Wev Developer Bootcamp"](https://www.udemy.com/the-web-developer-bootcamp), I realized Colt's image gallery exercise would be an ideal project to translate to Markdown, and better yet allow me to start a new blog series "static content says".**

---
The "static content says" series will focus on fun content that can be produced using Markdown on a static webpage.  So let's start this one off right and get right into the code.  


Below is the code from the exercise:

_(Note: you can ignore the p styling, just there for consistency's sake.)_


**HTML**
```html
  8 <body>
  9 <p>Paul/Maxey</p>
 10 <img src="..\Pictures\ep1.jpg">
 11 <img src="..\Pictures\ep2.jpg">
 12 <img src="..\Pictures\ep3.jpg">
 13 <img src="..\Pictures\ep4.jpg">
 14 <img src="..\Pictures\ep5.jpg">
 15 <img src="..\Pictures\ep6.jpg">
 16 <img src="..\Pictures\ep7.jpg">
 17 <img src="..\Pictures\ep8.jpg">
 18 <img src="..\Pictures\ep9.jpg">
 19 </body>
```


**CSS**
```css
  1 img {
  2     width: 30%;
  3     float: left;
  4     margin: 1.66%;
  5 }
  6 p {
  7     font-family: raleway;
  8     margin-left: 1.66%;
  9     font-size: 23px;
 10     font-weight: 800;
 11     text-transform: uppercase;
 12     border-bottom: 2px solid #f1f1f1;
 13     padding-bottom: 20px;
 14     width: 30%
 15 
 16 }
```
<hr>
First I set reference links for each image.  The square brackets contain the reference link name and are followed by image path and alt-text.

```md
[image1]: /assets/ep1.jpg "Copyright Paul Maxey 2019"
[image2]: /assets/ep2.jpg "Copyright Paul Maxey 2019"
...

```
Then I set a style block that I will use with each image..

```md
{:imageGrid:width="30%"}

```
and apply it to each reference link.

```md
[image1]: /assets/ep1.jpg "Copyright Paul Maxey 2019"
{: imageGrid}
[image2]: /assets/ep1.jpg "Copyright Paul Maxey 2019"
{: imageGrid}
```

 and then finally, I referenced the images.

```md
![image1]
![image2]  
![image3]  
![image4] 
![image5]
![image6]
![image7]
![image8]
![image9]
```

<hr>

I gotta say, it's pretty close.


<span><a href="#img1" rel="modal:open">![image1]</a></span>
<span><a href="#img2" rel="modal:open">![image2]</a></span>
<span><a href="#img3" rel="modal:open">![image3]</a></span>
<span><a href="#img4" rel="modal:open">![image4]</a></span>
<span><a href="#img5" rel="modal:open">![image5]</a></span>
<span><a href="#img6" rel="modal:open">![image6]</a></span>
<span><a href="#img7" rel="modal:open">![image7]</a></span>
<span><a href="#img8" rel="modal:open">![image8]</a></span>
<span><a href="#img9" rel="modal:open">![image9]</a></span>

{:imageGrid:width="30%"}

[image1]: /assets/ep1.jpg "Copyright Paul Maxey 2019"
{: imageGrid}
[image2]: /assets/ep2.jpg "Copyright Paul Maxey 2019"
{: imageGrid}
[image3]: /assets/ep3.jpg "Copyright Paul Maxey 2019"
{: imageGrid}
[image4]: /assets/ep4.jpg "Copyright Paul Maxey 2019"
{: imageGrid}
[image5]: /assets/ep5.jpg "Copyright Paul Maxey 2019"
{: imageGrid}
[image6]: /assets/ep6.jpg "Copyright Paul Maxey 2019"
{: imageGrid}
[image7]: /assets/ep7.jpg "Copyright Paul Maxey 2019"
{: imageGrid}
[image8]: /assets/ep8.jpg "Copyright Paul Maxey 2019"
{: imageGrid}
[image9]: /assets/ep9.jpg "Copyright Paul Maxey 2019"
{: imageGrid}

It's nothing exciting, but it's a fun way to incorporate images in your Jekyll post.

<div id="img1" class="modal">
  <img src="/assets/ep1.jpg"  class="modal_img">
  <a href="#" rel="modal:close">Close</a>
</div>
<div id="img2" class="modal" style="text-align: center;">
  <img src="/assets/ep2.jpg" class="modal_img">
  <br>
  <a href="#" rel="modal:close">Close</a>
</div>
<div id="img3" class="modal" style="text-align: center;">
  <img src="/assets/ep3.jpg" class="modal_img">
  <br>
  <a href="#" rel="modal:close">Close</a>
</div>
<div id="img4" class="modal" style="text-align: center;">
  <img src="/assets/ep4.jpg" class="modal_img">
  <br>
  <a href="#" rel="modal:close">Close</a>
</div>
<div id="img5" class="modal" style="text-align: center;">
  <img src="/assets/ep5.jpg" class="modal_img">
  <br>
  <a href="#" rel="modal:close">Close</a>
</div>
<div id="img6" class="modal" style="text-align: center;">
  <img src="/assets/ep6.jpg" class="modal_img">
  <br>
  <a href="#" rel="modal:close">Close</a>
</div>
<div id="img7" class="modal" style="text-align: center;">
  <img src="/assets/ep7.jpg" class="modal_img">
  <br>
  <a href="#" rel="modal:close">Close</a>
</div>
<div id="img8" class="modal" style="text-align: center;">
  <img src="/assets/ep8.jpg" class="modal_img">
  <br>
  <a href="#" rel="modal:close">Close</a>
</div>
<div id="img9" class="modal" style="text-align: center;">
  <img src="/assets/ep9.jpg" class="modal_img">
  <br>
  <a href="#" rel="modal:close">Close</a>
</div>

<script
			  src="https://code.jquery.com/jquery-3.4.1.min.js"
			  integrity="sha256-CSXorXvZcTkaix6Yvo6HppcZGetbYMGWSFlBw8HfCJo="
			  crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery-modal/0.9.1/jquery.modal.min.js"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/jquery-modal/0.9.1/jquery.modal.min.css" />

