---
layout: default
title: The future of RSS is microdata
---

Thanks to Google, the web is free again. Reader wasn't quite friendly towards web standards. It wasn't that Reader acted like a prison for RSS — it was the fact that it felt more like a hospice. It kept us sane every morning, but at the end of the day we worshiped a service that wasn't open. Now it is gone, and the web is free again. One day I want to say the same thing about social networks.

#### Promote your content, not an RSS feed

My preference for my own site is to remove any RSS links, but unfortunately I use Textpattern, which provides RSS as a core feature. So I'll keep it for the browsers and apps that can auto-detect the feed, with no prominent place in the site's layout design. I have to keep in mind that this site was designed for the year 2022. It may sound ridiculous at first, but when I posted it on [Dribbble](http://dribbble.com/shots/731291-Project-2022) I explained the design principles behind it.

Recently I added an access counter to the site, so each article stands on its own. The initial page view numbers were gathered from Google Analytics. I don't believe in social network counters (likes, tweets, +1s) because they don't change the way an article is consumed — actually, they make it worse.

#### Microdata saves the day

Microdata is an invisible interface added to the HTML code. It can provide basic feed functionality using descriptors for different parts of the content, and it can be extended with schemas. For example, the first paragraph of my "About" page contains my name and a small description of me. This "thing" is called a [Person](http://schema.org/Person). A Person can have multiple properties, defined within inline HTML elements like *span*, *b* or *i*.

Let's say I want my readers to know how many times an article was read. Can I pass this information to an RSS reader? No — not with a twenty-year-old format that can't be extended in any way. All I have to do with Microdata is define the access counter as [UserPageVisits](http://schema.org/UserPageVisits) and pass this information as [interactionCount](http://schema.org/UserInteraction). Now any robot that parses the page will interpret the data the same way a human would. Clever, isn't it?
