---
layout: post
title: Java upgrade
quote: Should i upgrade to the latest java version ?
image: false
video: false
---

# Why should i run the latest java version

In Scala community there have been talks about what java version the next scalac should target. That got me thinking, why should we run the latest version of java, and by latest i mean the latest major version.

It turned out it was easier to argument why you shouldn't run an old version, so here goes !


## Security

Nobody wants to be on the cover of some newspaper because your application has been compromised. That's why Oracle is using some many resource to keep java bug free. They actually are using so many resource to fix bugs, that the next java version has been pushed, due to lack of resources internally at Oracle.

Once a version is at it's end of life, Oracle won't be fixing bugs, unless you give them lots and lots of money.

So when did the java versions reach their EOL:

* 1.5 -> Oct 2009
* 1.6 -> Feb 2013

Source: http://www.oracle.com/technetwork/java/eol-135779.html


So if you are running 1.5 in production, your java version hasn't been update in 4 years. If you compare that with the number of security fixes that are put out, you __should__ be scared. Granted that most security issues are related to WebStart or Applets, some do target the server side code too.
A nice example can be found here http://blog.diniscruz.com/2013/08/using-xmldecoder-to-execute-server-side.html

## Developer attraction
Let's face it, we live in a dog eat dog world. You business will only survive if you got the best and the brightest. One why to attract them is to run a later version of java. I'm not saying that's the only parameter you are measured on, but it adds to the pile.

It can also be a leading factor in keeping the talent your got. We all know the ancient Chinese proverb "The bamboo is always greener, on the other side". So you should at least keep your bamboo somewhat green.


## Performance
We all need performance, right ?

You can have a secret army of code monkey slapping away on the keyboards, to get some performance gain. But just upgrading the JDK/JRE will give you huge benefits.

Java 6 is __18%__ faster than Java 5

Java 7 is __46%__ faster than Java 6

Source: http://geeknizer.com/java-7-whats-new-performance-benchmark-1-5-1-6-1-7/

There you have it, go upgrade :o)
