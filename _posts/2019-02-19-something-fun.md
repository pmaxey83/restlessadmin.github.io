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

Below is the code from the exercise:

_(Note: you can ignore the p styling, just there for consistency's sake.)_


**HTML**
```
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
```
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
First I set "variables" for each image.  The square brackets contain the variable name and are followed by image path and alt-text.

```
[image1]: /assets/ep1.jpg "Copyright Paul Maxey 2019"
[image2]: /assets/ep2.jpg "Copyright Paul Maxey 2019"
...

```
Then I set a style block that I will use with each image..

```
{:imageGrid:width="30%"}

```
and apply it to each variable.

```
[image1]: /assets/ep1.jpg "Copyright Paul Maxey 2019"
{: imageGrid}
[image2]: /assets/ep1.jpg "Copyright Paul Maxey 2019"
{: imageGrid}
```

Finally I laid out each image in a grid like fashion.

```
![image1] ![image4] ![image7]
![image2] ![image5] ![image8]
![image3] ![image6] ![image9]
```

<hr>

I gotta say, it's pretty close.

![image1] ![image4] ![image7]
![image2] ![image5] ![image8]
![image3] ![image6] ![image9]

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
