---
layout: post
title: Primality Testing
tags: [mathematics, primality, python]
categories: mathematics
---
I spent the past week working on implementing the Baillie-PSW probable prime test, and it’s been a lot of fun. It’s pushed my abilities in interesting ways, and I’ve had a lot of fun working on the code. I’ve learnt about profiling code in Python, as well as fast modular exponentiation.

On that last one: finding out that Python has a three argument form of pow() where the third argument is an integer to perform the exponentiation modulo to – that sped my code up ~10,000 times. Yep, ten thousand.

The interesting thing about the Baillie-PSW test is that it’s not deterministic. It can only tell you that a number is probably prime. There are a fair few probabilistic tests, and they all share the same flaw: pseudoprimes. A pseudoprime is a composite (non-prime) number which a probabilistic test reports as being prime. This is obviously quite a problem with probabilistic tests – you can be sure that any number reported as composite is composite, but you can’t be sure that any number reported as prime is prime.

This area is where the Baillie-PSW test is very good though. It combines two simpler probabilistic tests (Miller-Rabin and a strong Lucas test). There are no known numbers which are pseudoprimes to both tests. There may be some out there, but there are definitely none below 2^64, and no-one has found any higher than that, either. This means that, for many purposes, the Baillie-PSW test can be regarded as deterministic. It certainly is below 2^64.

If you need to check numbers above 2^64, Baillie-PSW can still be useful. It can weed out definitely composite numbers, leaving you with a smaller list of probable primes with which to check with a slower, deterministic method.

If you’re interested in the code I wrote, it’s available on [GitHub](https://github.com/smllmn/baillie-psw).
