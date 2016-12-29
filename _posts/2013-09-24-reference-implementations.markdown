---
layout: post
title: Reference Implementations
categories: programming
tags: [python, programming]
---
Recently I’ve been playing around with a Lisp dialect called Scheme. It’s an absolutely tiny language designed to be very easy to implement. The very first problem I had with Scheme is that it’s very easy to implement; consequently, there are a lot of implementations. This is great when you have a good grasp of the language – you know which features of different implementations will suit you best, and you can choose the right implementation for you and your projects. When you’re just starting out, however, it can be a tricky – and daunting – task to choose from a list of so many different implementations with differences you don’t grasp.

Contrast this approach with, say, Python. Python has a canonical reference implementation called CPython (yes, it is written in C). I’m certain that most beginning Python programmers aren’t even aware that there are other implementations; if they are it’s in a fuzzy ‘I don’t need to care about that’ kind of way. When you Google Python, you find python.org which hosts the CPython implementation as well as the Python documentation and more. After you become more familiar with the Python language, you might want to branch out and use a different Python implementation because it offers something you need – that’s fine. But CPython’s prevalence makes it easy for beginners to jump in. They don’t have to make decisions they don’t understand.

That’s not to say that Scheme’s way of doing things is necessarily wrong. But it does mean that people without an amount of programming experience behind them need a little more hand-holding when getting started with Scheme. Because seriously, there are a [lot](http://community.schemewiki.org/?scheme-faq-standards#implementations) of implementations to choose from. For what it’s worth: I went with Mit-Scheme because I’m working through _Structure and Interpretation of Computer Programs_.
