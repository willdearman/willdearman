---
layout: post
title: Instapaper versus Pocket
categories: [products I use]
tags: [productivity]
published: True
---

Several weeks ago Instapaper announced they had been acquired by Pinterest. A fair amount of negativity was expressed by the community, which the employees [attempted to temper](https://news.ycombinator.com/item?id=12346612). Now that the initial excitement has subsided, I want to review the two relative to my current workflow.

## My Objective
Like many people I read quite a bit of text content on the web, and have some desire to save what I read for future reference. What I want to save can range from specific facts, to how-to articles, to general background on subjects. Generally speaking, I'm looking for a futureproof [commonplace book](http://thoughtcatalog.com/ryan-holiday/2013/08/how-and-why-to-keep-a-commonplace-book/) that requires very little time to maintain [edit: yes, I realize the irony that a pen and paper commonplace book meet this requirement]. This is an actual use case as on a not infrequent basis I do find myself referring to my personal knowledgebase to find related ideas.

Beyond the practical uses, I also aspire to use my collected 'knowledge' to create something interesting I can interact with. I'm always curious about the ontology of knowledge (conceptual versus applied) and how it will be eventually integrate with AI, so the idea of shoveling this content into some sort of deep learning model is fascinating. While this is doable today, I don't see myself investing the time to actually do this any time in the near future.

## The Need
At the top, my need is similar to that of many others: 

1. I encounter an artcile or post ('content') I don't have time to read in the present, and I want to save it for later reading;
2. To find the content at some indefinite future point, I need a tag and folder system or something more;
3. When I read the content, I want to be able to highlight specific sections to retain indefinitely;
4. I need to combat byte-rot (information is taken offline with no redirect) because I may refer to it years later;
5. I need my solution to be relatively future-proof to avoid losing the processed information.

## Competing Workflows

### Instapaper
Instapaper and Pocket are very similar in functionality so I *should* need only one, not both. I've been using Instapaper for several years now, and my workflow evolved to this:

1. Safari Extension (OS X and iOS) to save page
2. Read in the Instapaper iOS app or on Instappaer.com
3. Highlight text segments
4. Favorite or Do Not Favorite
5. Archive in Instapaper
6. IFTT received highlights and appends them to a note in Evernote with the article title
7. IFTT receives favorited articles and saves the text to a note in Evernote
8. Tag highlights in Evernote
9. Search Evernote for information, if not found, search Instapaper.

One related workflow I tried was sending the posts either in a digest or individually to Kindle. This has the benefit of being easier on the eyes, and being usable on a more durable device. Interestingly, it is possible to retain highlight text on the Kindle, but unfortunately it is cumbersome (though not impossible) to get the highlights into Evernote.

#### This workflow has several drawbacks:
1. Instapaper does not work on sites requiring a login. Period. I save a number of articles from the WSJ and only get the first few lines. My workaround is to use the iOS share sheet to share the article in Evernote directly, but this eliminates my ability to store highlights in a separate note.
2. The search feature on Instapaper.com is just not very good. It is horribly slow most of the time, and the order of the results often puts irrelevant results first.
3. The future of Instapaper post-acquisition is uncertain. While the commitment was made to not shut down the product, that is different then keeping it up to date.
4. Exports do not contain article content.

#### The key benefits of this workflow are:
1. The highlighting feature works just as it should, and works the same across platforms (iOS, web). I end up with a separate note in Evernote with just the highlights I made.
2. The formatting simplification in Instapaper is stellar. Very, very rarely do I ever need to go to the non-simplified view.
3. The site and iOS apps are minimalist and free of distractions (though I wouldn't call the overall UX great).

### Pocket
While I had been using Instapaper, Pocket is clearly the incumbent in the read it later segment. I've tried it for the past month and my workflow evolved to this:

1. Safari extension (OS X and iOS) to save article
2. Tag the article at the time of save
3. Read via iOS or Mac OS apps, or on Pocket.com
4. Highlight text and share it via Recommended (highlights are not retained in the article)
5. IFTTT receives favorited articles and saves them to Evernote.
6. Search my Recommended Pocket items for information, if not found, search full Pocket archive, else search Evernote.

#### The workflow has several drawbacks:
1. I experiene a significantly lower success rate with converting pages to simplified text, and my undersanding is that only simplified text is retained in the permanent archive. [edit: untested assumption]
2. My method of turning highlights into shares is really just a workaround. I have not found a way to abstract the highlights into a useful format (e.g. a single Evernote note) without significant manual effort.
3. While search is faster with Pocket, I don't have an easy way just to search my highlights.
4. All my highlights have to be shared.
5. Saving from sites requiring credentials only works from mobile apps. ([see here](https://help.getpocket.com/article/1065-saving-from-subscription-based-sites))
6. The tags are not retained outside of Pocket.
7. Exports do not contain article content.

#### The key benefits are:
1. The iOS app (though **not** the web and Mac OS  versions) successfully saves from sites requiring credentials (wish this were true of those saved via Mac OS Safari).
2. Suggested tags and tagging at capture. This results in me actually using tags, rather than deterring this to some indefinite point the future. 
3. Pocket seems to have a more certain future, though it still does not appear to have a sustainable self-funding model.
4. The search on Pocket just works better.
5. The ['permanent archive' feature](http://www.theverge.com/2014/5/28/5755392/pocket-introduces-paid-version-to-become-your-permanent-digital) could could potentially replace my reliance on Evernote for archiving on a go-forward basis.

## Conclusion?
I'll admit the jury is still out on which product will be my long term companion. Instapaper has superior formatting simplification technology, but Pocket can save content from paywalled sites. Instapaper recently sold to a company (Pinterest) that is unlikely to invest in developing Instapaper further, but Pocket appears to have an unsustainable revenue model altogether. Instapaper allows me to highlight text and consolidate it separately, and Pocket simply does not. With either my workflow is to rely on Evernote as a consolidation point, which itself is a potential point of failure.

### Imagine a different future...
None of these options seems to be very good for retaining content in a simplified format indefinitely, and none appears to contemplate feeding the simplified content into a deep learning model. Unfortunately I doubt the market for such a product is very deep. Optimistically, however, there are some FOSS projects to replace Evernote that could be adapted to replace my workflow entirely.

Perhaps you can help](https://github.com/twostairs/paperwork/issues/62) bookmarklet or browser extension to scrape articles and associated graphics into self hosted instances of [Paperwork](http://paperwork.rocks) we could then use as a platform for managing our knowledge?
