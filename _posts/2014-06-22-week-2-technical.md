---
layout: post
title:  "Week 2 Technical Blog"
date:   2014-06-22
categories: technical
---


Week 2
======

Let's be honest: at first glance "class"es and "id"s seem to be pretty much the same thing. But if we're being honest (and we are) there is no way that programmers who live for ease and efficiency would interchangeably use two completely different tags. So... what is the difference? 

In general, IDs are going to be more specific. IDs will outrank other HTML elements and classes. There are many analogies I've come across. Each student can only have his or her own ID, but a bunch of them can be in the same class. Or the difference between a barcode and a serial number-- all White 32GB iPhone 5s for Verizon will have the same barcode. That's all the store needs to know when you're purchasing it so it knows how much to charge you. But each of those iPhones also has its own unique serial number, which indicates which iPhone belongs to you and only you.

So what? They still do the same things, right? While this isn't necessarily going to affect your coding between CSS and HTML, the difference is more important when it comes to interacting with the DOM or other languages such as JavaScript. An ID acts like a "you are here" sticker for JavaScript. You don't want to have more than one "you are here". You can't be in more than one place at once. A class won't interact the same way, so you can have them wherever.

An important (nay, one might even say crucial) thing to remember is when naming classes is that they should be named specifically but not descriptively. For example, if you name a class "red_text" and then have to change your color scheme, you would have to go into your HTML and change every instance of the class-- well, you wouldn't HAVE to. You could just change the colors in the CSS, but it could get confusing to anyone else looking at your code. Try to name classes according to their function. Instead of "red_text", you could say "warning_text". 

So really, there are two things to as yourself when it comes to IDs and classes:

1. Is what I'm about to create completely unique? Will it always be unique in the future? If yes, it should be an ID. If not, a class.

And then: 

2. How do I name this according to function as opposed to description?

For more information:

+ [Reading 1](http://www.iraqtimeline.com/maxdesign/basicdesign/principles/princlass.html).
+ [Reading 2](http://webdesignfromscratch.com/html-css/using-classname-class-and-id-in-html/).
+ [Reading 3](http://stackoverflow.com/questions/298607/css-best-practice-about-id-and-class).

