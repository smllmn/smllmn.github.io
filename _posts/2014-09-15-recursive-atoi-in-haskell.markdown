---
layout: post
title: Recursive atoi in Haskell
---
A friend of mine suggested, during a conversation, that it would be difficult to write a recursive implementation of atoi which could handle all real numbers (i.e. not just non-negative integers). Well, I decided I had to do it anyway. I will freely admit that most of my time was spent remembering how Haskell works.

{% highlight haskell %}
import Data.Char
import Data.List.Split
myatoi :: [Char] -> Float
myatoi ""       = fromIntegral 0
myatoi ('-':xs) = - myatoi xs
myatoi ('.':xs) = (myatoi xs) / 10^(fromIntegral$length(xs))
myatoi (x:xs)   = fromIntegral((ord(x)-ord('0'))*10^length(head(splitOn "." xs))) + (myatoi xs)
{% endhighlight %}

It will fail amusingly if you feed it anything other than a number as a string, but otherwise it works pretty well. That is, of course, despite it being ugly and mildly indecipherable.
