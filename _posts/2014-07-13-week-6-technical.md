---
layout: post
title:  "Week 6 Technical Blog"
date:   2014-07-13
categories: technical
---


Week 6
======

The difference between OO and non-OO programming
------------------------------------------------

I'm going to try to keep this very simple (and from an English major's perspective). 

In programming, you have variables and methods. They're the nouns and verbs of your code. They're the building blocks, just like the building blocks of a sentence.

You can have any number of nouns: a cat, a dog, a monkey, etc...

That do any number of verbs: nap, eat, chase, etc...

If we define a cat variable, a dog variable, and a monkey variable, we can call methods (napping, eating, and chasing) on all those different variables. We can have a cat napping or a dog napping. We can have a monkey eating and a dog eating. We can go through all the permutations we want! However, in this story we're trying to tell with our code, it gets more complicated to say that the dog ate (past tense). 

Object-oriented programming helps us group these nouns and verbs together into objects. In our parts of speech analogy, it'd be like defining simple sentences. Instead of the nouns as variables and verbs as methods, we can simply ensure that we don't have a verb without a subject or a noun without an action-- in other words, a complete sentence (which would be the object). 

Procedural programming would make us call the methods on the variables. With object oriented programming we can create a class Sentence that requires both a noun and verb.:

	class Sentence
	def initialize(noun,verb)
	@noun = noun
	@verb = verb
	end

You don't have to worry about calling: cat.chase or dog.nap. All you have to do is:

	Sentence.new(cat, chase)
	Sentence.new(dog, nap)

Whereas cat.chase is running a method (chase) on a variable (cat), which is two different things, we can use object-oriented programming to just create a sentence in which the cat chases. The first is procedural. It's telling the computer to call chase (step 1) on cat (step 2). The second, object-oriented, is creating an instance where the cat chases (only one step).

This inherent connection between the nouns and verbs of your program can make your life much easier (especially as things get more complicated)! You can group things by connection instead of simply by individual nouns and verbs. When things get more complicated, you can have classes for tenses that would still both take a noun and verb as their inputs, but the verb would have different methods(tenses) applied to it.