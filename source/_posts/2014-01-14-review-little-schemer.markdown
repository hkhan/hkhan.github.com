---
layout: post
title: "Review: Little Schemer, Fourth Edition"
date: 2014-01-14 11:34:48 +0000
comments: true
categories: [Book Reviews, computation, Lisp] 
---

[The Little Schemer](http://mitpress.mit.edu/books/little-schemer) is very different from the usual books on programming. It can probably be considered the first 'koan-style' book - it presents a dialogue between a student and a teacher which is used to further the student's progress and understanding.

The book starts off with the very basics and gradually builds more and more complex ideas namely [recursion][1], [Y combinator][2] and the [metacirular evaluator][3]. The code translates seamlessly to Racket which is a modern descendent of Scheme and working in DrRacket is a very enjoyable experience. I adopted a TDD approach using RackUnit as the testing framework to give a red-green-refactor style workflow. Gradually, the idea of recursion begins to sink in, the fog begins to clear and the choice of Lisp for expressing these ideas becomes clear. Its a very liberating feeling to be able to express solutions using the very minimal set of constructs whilst taking a peek at what's so special about Lisp.

In short, this is a wonderful book which has something for everyone. For those new to Lisp and previously used to imperative style, its an eye-opener. It exposes the reader to elegant and beautiful ideas of computation through its learn-by-doing and learn-by-reflection approach. For curious minds, these are fascinating avenues for further exploration. I've thoroughly enjoyed going through the exercises, grasping the ideas presented and learning some Lisp along the way. Its definitely on my recommendation list.

Arguably, you can get all this with SICP which gives a much more rigorous and formal treatment of these topics (and more) but this is so much more fun and that's what its about, isn't it?

[1]: http://en.wikipedia.org/wiki/Recursion_(computer_science)
[2]: http://en.wikipedia.org/wiki/Fixed-point_combinator#Y_combinator
[3]: http://en.wikipedia.org/wiki/Meta-circular_evaluator
