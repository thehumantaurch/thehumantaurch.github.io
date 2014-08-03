---
layout: post
title:  "Week 4 Technical Blog"
date:   2014-06-29
categories: technical
---


Week 4
======

Array It That Way
-----------------
Arrays are useful little things in Ruby because they allow us to make groups of information that we can then manipulate. An array can store numbers or strings or both. They are mapped by a number system. Each item in the array corresponds to its order in the array, but starting with position 0 (not 1!). You can retrieve a value in the array by calling its position.

Hashes and Values and Keys, Oh My!
----------------------------------
Hashes are like arrays in that they allow us to group information as an array would do, only they allow you to be more specific in how the information is grouped. While an array is mapped by the numbers, starting at position 0 and all the way to the end of the array, a hash is mapped by pairs of keys and values. Within a hash, they key/value pair is sort of like algebra-- you can make "x" correspond to 100-- but you can also make "x" correspond to any value, string or otherwise. In a hash, you can retrieve a value by calling its key. 

Where do we go from here?
-------------------------
When should you array and when should you hash? Well, they both have their uses. If you need to store a group of items and order doesn't necessarily matter, an array should do the trick. If you want an array that tells you the months of the year, you can make one:

months = \["January", "February", "March", "April"... etc...\]
						
However, what if you get confused by calling months(1) and expecting January, but instead you get February? You need to call months(0) to get January, but your mind keeps defaulting to January being the first month of the year. In this case, a hash may be more suited to your needs. You can assign the key "1" to "January".

To decide between the two, most often you'll know. If you need to take two things and make them correspond to each other within your group, you need a hash. If not, an array will work just fine. Unless you've got some weird numbering things going on, in which case a hash might make things more clear.