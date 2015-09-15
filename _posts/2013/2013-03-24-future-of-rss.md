---
layout:     post
date:       2013-03-24 15:51:31
edit:       2013-03-29 16:22:20
title:      "The Future of RSS is Microdata"
category:   hope-for-the-future
slug:       future-of-rss
---

Thanks to Google the web is free again. Reader wasn’t quite friendly towards web standards. It wasn’t that the Reader acted like a prison for RSS, it was the fact that it felt more like an hospice. It kept us sane every morning, but at the end of the day we worshiped a service that wasn’t open. Now it is gone and web is free again. One day I want to say the same thing about social networks.

#### Promote your content, not a RSS feed

The preference for my own site is to remove any links for RSS, but unfortunately I use Textpattern which provides RSS as a core asset. So, I’ll keep it for browsers and apps that can auto-detect the feed with no relevant place in the design of site’s layout. I have to keep in mind that this site was designed for the year 2022. It may sound ridiculous at first, but when I posted it on [Dribbble](http://dribbble.com/shots/731291-Project-2022) I explained the design principles behind it.

Recently I added an access count to the site, this way it’s making each article standing on its own. The initial page views numbers where gathered from Google Analytics. I don’t believe in social networks counters (likes, tweets, plus ones) because they don’t change the way an article is consumed, actually they make it worst.

#### Microdata saves the day

Microdata is an invisible interface added to the HTML code. It can provide the basic feed functionality using descriptors for different parts of content and can be extended using schemas. For example, the first paragraph from my “About” page contains the name and a small description of me. This “thing” is called a [Person](http://schema.org/Person). The Person can have multiple properties which can be defined within inline HTML elements like *span*, *b* or *i*.

Let’s say I want my readers to know how many times an article was read. Can I past this information to a RSS reader? No, not with a twenty years old format that can’t be extended in any way. All I have to do with Microdata is to define the access counter as [UserPageVisits](http://schema.org/UserPageVisits) and past this information as [interactionCount](http://schema.org/UserInteraction). Now any robot that will parse the page will interpret the data as any human will do. Clever, isn’t it?
