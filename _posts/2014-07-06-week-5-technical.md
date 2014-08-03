---
layout: post
title:  "Week 5 Technical Blog"
date:   2014-07-06
categories: technical
---


Week 5
======

About Classes
-------------

Let's start simple: <b>classes</b> are merely a <b>means of organization</b>. We're still dealing with objects, variables, and methods, but we're just grouping them as convenient. Within a class, you can define <b>methods</b> and <b>variables</b> that are <b>instances of the class</b>.

<i>Don't worry too much about the syntax in the following. I'm going for the concepts here.</i>

To create an example: let's say we want to organize our library. If we create a class about books, there's a lot of information we will want to be able to easily access about books.

	class Book

We would create a new book (or a book object) by calling Book.new.

We would then set up the different kinds of information we want to be able to access about each new book we create. We might want to store information about title, author, number of pages, and genre. To do that we use instance variables. In this new book we've called, this is the information we may want to use. All books we create will have the same four types of information, but for each new Book, each separate Book, the information will be different.

We would then use instance variables to organize that information. Instance variables (with the little @ in front) define the same type of information for <b>this particular instance</b> of a Book. In other words, all Books have @titles, @authors, @pages, and @genre, but they won't be the same things.

	@title = title
	@author = author
	@pages = num_of_pages
	@genre = genre

In other words:
				
	Book.new("American Gods") // <= instance of Book
				
would have an author of Neil Gaiman:
				
	@author = Neil Gaiman // <= variable in this instance of Book
				
but
	
	Book.new("The Golden Compass") // <= instance of Book
				
would have an author of Philip Pullman:
				
	@author = Philip Pullman // <= variable in this instance of Book

You could also have:
				
	Book.new("Neverwhere")
	@author = Neil Gaiman

It doesn't matter. Both objects are books, but separate books, even if information pertaining to the books is the same. For the instance of the class Book that is "American Gods", it will have a title and author set to American Gods and Neil Gaiman. For the instance of the class Book that is "The Golden Compass", it will have a title and author set to The Golden Compass and Philip Pullman.

Now in a class we can also manipulate the data we've organized. We can define a method that will return a book's name and author. For any instance of the Book class that we've defined with the appropriate instance variables, if we define a method <b>info</b> that:

	puts @title + " is by " + @author

we can retrieve the title and author of any Book we create. In other words, for the Neverwhere instance of Book:

	Book.new("Neverwhere") =  book1

if we provided the appropriate information that all Books have:

	@author = "Neil Gaiman"

and we called

	book1.info

as we can on all Books, we would get

	Neverwhere is by Neil Gaiman

But for American Gods instance of Book, we'd see

	American Gods is by Neil Gaiman.

Now, if we wanted to have a class Play, we would want to store some different information. We might want act number and scene numbers and line numbers. We might stil want to have the title, author, and number of pages, but we'd probably be storing and manipulating the data in a different way. Thus, we would use a new class.