---
layout: post
title:  "Week 7 Technical Blog"
date:   2014-07-15
categories: technical
---


Week 7: Squealing about SQL
===========================

Injecting Fear into the Hearts of Devs
--------------------------------------

What is a database for? To store data. What is SQL for? To access and request data. SQL Injection is a nasty technique that hackers use to steal that information from your database. And, unfortunately, it's pretty easy. SQL is (thankfully) pretty easy to use, but that's also what makes it so easy to hack.

In a somewhat simplistic example, let's say you have a website with entry fields that a user can input info by which to gain access to the database, such as a username and password. However, that input field can become a double-edged sword. While a user with the appropriate intentions can insert their login credentials and access the information in their part of the database, a user with less than benign intentions could (instead of credentials) input an SQL query in itself, which could concievably retrieve way more information from the database than you would want them to. Think: passwords, credit card numbers, social security numbers, etc. You'd just have to guess the name of the column they were under.

If nothing else, remember this: OWASP, the Open Web Application Security Project, lists Injection as the number one critical web app security risk.

For example, if you add a simple "OR" statement to a request, as in: OR "1=1" the request is for a specific piece of data or where 1=1 is true. WHICH IS EVERYTHING. See now why SQL injection is scary???

So... how do we prevent it? Well, it's hard, but there are a few things you can do. For us at DBC, who are using SQLite, we can use sqlite3_prepare() to create a statement object, in other words, a prepared statement. A prepared statement won't let an attacker change the original intention of a query-- think of it as an unsafe query reading "username" OR "1=1", but with a prepared statement the input would instead read "username OR 1=1" which is much more specific. There are ways to create a prepared statement in most languages, which you can read more on at this [OWASP cheat sheet](https://www.owasp.org/index.php/Query_Parameterization_Cheat_Sheet).

There are other methods as well, such as using Stored Procedures, which are similar to prepared statements but are stored in the database itself (whereas a prepared statement is a query, sometimes known as a paramatized query). There are also ways to "escape" the user input, in other words, to help differentiate the user input from the original query.

For further reading:

1. [A Clear Explanation of Injection for the Uninitiated](https://www.acunetix.com/websitesecurity/sql-injection/)
2. [OWASP Injection Prevention](https://www.owasp.org/index.php/SQL_Injection_Prevention_Cheat_Sheet)