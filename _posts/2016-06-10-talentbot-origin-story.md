---
layout: post
title: Talentbot - The Origin story
categories: [product management]
tags: [product management], [professional development]
published: False
---

A few days ago I was driving and listening to my four year old daughter in the back seat. She was using her LeapReader to have ["Leap and the Lost Dinosaur"](https://www.amazon.com/LeapFrog-LeapReader-Book-Dinosaur-works/dp/B00AOHDC4A?ie=UTF8&*Version*=1&*entries*=0) read to her. In the story a professor travels through time in an attempt to return a baby Hypacrosaurus to the Cretaceous period where it belongs. After jumping to the wrong period the professor says "But we're only off by 70 million years" to which my daughter says "that's not a lot".

I immediately wanted to object because 70 million is a large number, but in the history of the universe it is not that long. But how do I explain that to a four year old? What is the difference between the 70 million that is a lot, and the 70 million that is not a lot?

The answer is *context*. Context is the way we know the different between big and small, short and long, easy and hard, and even good and evil. Without context, a number is just a value without metadata; you don't know where it fits in the big picture. In the government spying discussions of the past few years, many argue that the metadata of a phone call is as important as the content of the call itself. As a practical matter, is this because it gives the event context?

I then realized, the reason most digital applications are not more useful is that they are lacking context. If go to almost any financial application and ask how the business is doing, I will get a report full of numbers, balance sheets, income statement, cash flow statements, and similar. None of these directly answer my question: how is the business doing. Similarly, I can ask Siri, Google Now, Cortana, or the other digital agents almost any question and they will deliver a factual answer at best. They have no context to provide you anything better. Further you can't even extract the additional information you need to synthesize your own context. Clearly context is a problem across the board worth solving.

So, how do you address the problem of context? Peter Rojas says bots beat apps ["when context and convenience matters most"](https://chatbotsmagazine.com/when-do-bots-beat-apps-when-context-and-convenience-matter-most-443c9191bb2b#.rr4q3ymwe). If that is true, why are Siri and her competitors so bad at context when they have the potential to obtain so much contextual data from our lives? Ryan Block seems to have figured it out: ["For everybody else, the narrower the domain, the better"](https://medium.com/@ryan/conversational-interaction-design-constructing-context-b21e2341334f).

At this point, a strategy begins to congeal: a bot with a narrow domain. But, the realist in me says that if this were the optimal strategy, the smart people already working on the [near infinite number of bots out there already](https://www.producthunt.com/topics/bots) would have solved the problem before now and we would be better off than we are. So, what is missing?

What is missing is that deep down we all want something more complete than a toolkit of a 101 domain specific bots operating in silos. Jumping from bot to bot to obtain discrete parts of the context isn't any better that jumping between a few Excel files to find what I need. Slack is approaching the problem by aspiring to be ["a Control Panel for Your Job"](http://bits.blogs.nytimes.com/2015/12/15/slack-aims-to-become-a-control-panel-for-your-job/), but even in a control panel you are still jumping between discrete components.

If a control panel is not the right approach, who is doing something different? Amazon Alexa came to mind. Developers build 'skills' for Alexa that add capabilities. While I don't own an Alexa-enabled device yet, the demonstration I saw had someone saying "Alexa, ask Capital One what my credit card balance is". Interesting. With Alexa, Amazon is training users to provide a component of their own context (who to ask), but allowing many more contexts to exist than Siri (because of the open nature of the platform).

Alexa is clearly an advancement as you have the beginnings of context, but you are still limited to asking a pre-defined query. What's missing is the ability to maintain your engagement with the context until you have accomplished your objective. For instance, conceptually Alexa could tell you that sales are up 50%, and in the future maybe even that an increase in sales is generally a good thing, but Alexa still couldn't tell you why.

At this point, it sounds like our best bet is to work on a chat bot in a limited domain, that also has the ability to gain abilities via add-ins. But what would we have accomplished? Re-creating Alexa as a Slack bot? How do we truly master that last aspect of context that everyone is missing?

The answer seems obvious now: why wouldn't we just have a conversation?

Bingo. I'll make a bot platform like Alexa, with domain specific add-ins (as opposed to vendor specific), that you will work with in a conversation, with context provided both by what you are working on as well as what you said previously.

Awesome. Now how do I build that?