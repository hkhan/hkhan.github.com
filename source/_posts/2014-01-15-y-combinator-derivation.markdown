---
layout: post
title: "Y Combinator Derivation"
date: 2014-01-15 14:17:46 +0000
comments: true
keywords: computation, y combinator, y-combinator, y-combinator derivation
description: A detailed derivation of the Y combinator based on the Why of Y derivation by Matthias Felleisen
---

One of the benefits of going through The Little Schemer, which I've [reviewed]({% post_url 2014-01-14-review-little-schemer %}) recently is that it dedicates one of the later chapters solely to arriving at the [Y combinator](http://en.wikipedia.org/wiki/Fixed-point_combinator#Y_combinator). It starts with a constraint that a function definition is not allowed to refer to itself. Up till this point, recursion has been the key technique for computation but what if a language only contains anonymous functions. In this case, its not possible to refer to the function which is describing the computation. How can recursion be implemented in such a language? 

This is an interesting and challenging exercise. Of course, its of little practical value in every day programming as all languages allow named function definitions. Nonetheless, its a fascinating question to ask and the real value is in the journey towards understanding and working through a problem methodically. The book provides a great step-by-step treatment of the problem but there are lots of ways to arrive at the solution. I've found that each one gives new insights into functional programming techniques and ideas. 

Here is a detailed derivation inspired by [A Lecture on the Why of Y](http://www.ps.uni-sb.de/courses/sem-prog97/material/YYWorks.ps).

{% gist 8436742 %}
