---
layout: post
title: "Using Snap CI with golang"
description: ""
category: 
tags: [golang, ci, snapci]
---
{% include JB/setup %}

I'm finding myself writing more and more code in go, so i thought it were about time i got some CI up and running.
Pretty much when that idea popped into my head, i got a mail from snap-ci. So i thought i would give it a go.

Snap is a product developed by ThoughtWorks, and it seems like a nice take on the whole CI thing.

But it seems that golang isn't supported out of the box, however we can hack it a little bit to make it work :)

I went for the free on-line hosted version, since my projects are currently only small hobby projects.

You first need to go through a small snap ci guide, the first time you use it. This is kinda nice, takes 1 minute and explains what snap is about.

Once all that is done, you need to create or alter a stage, for the handling the go build / test. I took the DummyStage, and renamed it to GOTEST.
And now for the hacking of this stage, since go isn't a supported language in snap, we need to install the binaries ourself, luckily snap supports this.

The first thing we need to do in the stage, is this:

```sudo yum install --assumeyes golang```

This installs the golang binaries, don't worry you are allowed to do sudo commands in snap, according to the documentation.
We also need to setup the GOPATH, in order for go to work. On the stage configuration page there is a section called ___Environment Variables for this stage___ in there we need to set the name to GOPATH, and the value to /var/snap-ci/repo.

So the final list of commands to be executed in this stage should look something like this:

{% highlight bash %}
$ sudo yum install --assumeyes golang
$ go get github.com/spaolacci/murmur3
$ go test
{% endhighlight %}

All done, simple and nice.
