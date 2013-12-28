---
title: philosophy behind the technical aspect of my site
created_at: 2011-11-08 22:00
kind: article
tags: [myblog, learning]
tldr: Optimize for the right use-cases and keep it KISS.
---

### Makin it static[^1]

I always wonder about those simple, sometimes beautiful, but slow sites. I once stumbled upon "[Solving the Wrong Problem][]", which is an article about CMS solutions that "address issues of blog maintainers, not readers". Also Arjan shares his thoughts in his hello world post: "I can tell you now that it makes managing my site a hell of a lot easier: there a far fewer moving parts."

While busy with the first step of setting up my blog I heard another quote I like from [Nicholas Zakas]: 
	
	So if it's possible to do something in HTML, then you should just do it in 
	HTML without anything else. And then, if it's possible to do it in CSS, 
	you should do it in CSS before you try doing it in anything else. And if,
	it's possible to do on the server, you should do it on the server unless you 
	really can't. Then, once you've exhausted all of those options, then you
	go to JavaScript. That is the thing that comes at the end of your journey 
	rather than where you start it.
	
### use-cases

#### The reader
For me, and who knows some people that might take interest in my endeavors, it must be fast, robust and searchable.

#### The content maintainer
As maintainer it must be easy, from a native flow[^2] point of view, to add blog posts and also maintain some custom pages.

#### Technical 
Let the tools and application do their jobs. In other words in this context I try to stick with [Standing on the shoulders of giants] and avoid the [Not_invented_here] mantra of rolling my own.

Although during the initial setup I will use this also as a learning project, the goal is to have a website which works and does not take much looking after.

### Grand scheme

So basically I shamelessly copied this blog setup from [Arjan de Graag][], but I will explain why it fits my use-cases and philosophy.

1. Fast and Robust: It's just some HTML5[^3], bit of CSS and minimal Javascript. So what can go wrong ;-)
2. Adding blog post and custom pages is a matter of writing some [Mark down] press Compile and Upload, e.g.:
    
	write markdown
	nanoc
	nanoc view (host local to review post)
	nanoc deploy
	Time for tea

3. It is searchable with Google custom Search
4. No Hazardus "Comments" section, using Twitter for that.
5. And as far as "nice to have" go:
    * RSS feed: if people want to keep posted.
    * Google analytics: for page view analysis

As the whole technical side of the setup just read [Why I like nanoc] from Arjan.


[^1] In the past, in a time when mentioning AJAX would be 99% of the time assosiated with the cleaning fluids, I generated a static photo website. I choose PHP as learning object, but used it as shell script, rather then dynamic content language.
[^2] As text files are very natural to my flow. Complying a bit more to the md/kramdown format is a small tweak.
[^3] No I will not do any older browser support.

[Solving the Wrong Problem]           : http://prog21.dadgum.com/130.html
[Arjan van der Gaag]                  : http://arjanvandergaag.nl/
[Nicholas Zakas]                      : http://hanselminutes.com/383/enough-with-the-javascript-already-with-nicholas-zakas
[Why I like nanoc]                    : http://arjanvandergaag.nl/blog/why-i-like-nanoc.html
[Standing on the shoulders of giants] : http://en.wikipedia.org/wiki/Standing_on_the_shoulders_of_giants
[Not_invented_here]                   : http://en.wikipedia.org/wiki/Not_invented_here
[Mark down]                           : http://daringfireball.net/projects/markdown/syntax

*[CMS] = Content Management System
