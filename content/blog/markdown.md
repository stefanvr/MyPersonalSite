---
title: Markdown
created_at: 2014-01-08 23:00
kind: article
tags: [flow]
tldr: Shell live writing Markdown using Mou - clone github wiki, write some mark down, save, commit, push, WOOT!

---

# Living in a Shell 

[Markdown] is very popular these days for various reasons. One of those is the ability to write wiki pages, which can be rendered a bit more pleasant for the reader eyes. As text only gives an easy diff[^1] and wikis proof that rendering it can be nice too. Some times even fancy things like embedding [Websequencediagrams] is possible.

So what about living inside a shell?

# Flow

## Access with Git hub

Git repos have a wiki and and even [Websequencediagrams] work. Now as everything at git hub is about git, you can checkout the wiki with <git url>.wiki.git. How nice is this, having the markdown files on disk.

## Editing with MOU

[MOU] is a the tool for the job:

* **Split view**: markdown (with syntax highlighting) VS rendered view
* **Spelling checker** (Although I really need a proof reader)
* Hey I do not need more :-)

But wait, that is no shell....

## Putting it all together

Open a shell on a nice spot on your file system

    $git clone <repo>.wiki.git  
    $touch new article.md  
    $open article.md  

    write some nice markdown and hit save

    $git commit -m "Useful message here please :-)"  
    $git push
   

WOOT! Documentation all nice and updated for the readers.

## Loving it 

Markdown is also the weapon of choice for my site/blog, more on that soon. But for now the flow of writing notes in markdown from a shell and getting it out in the world has become a breeze.

[^1]: Yeah, yeah, I know, I know MS-Word can diff and with proper track changes it can work..... but some how (unintentional )style changes in larger documents alway seem to mess up easy comparison .... and really styling is not my thing, but I want it to look nice.

[Markdown]:            http://daringfireball.net/projects/markdown/
[Websequencediagrams]: https://www.websequencediagrams.com/
[MOU]:                 http://mouapp.com/
