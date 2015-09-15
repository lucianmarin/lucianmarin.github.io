---
layout:     post
date:       2009-04-26 20:42:50
edit:       2013-03-19 20:47:23
title:      "Web Techniques"
category:   meaningful-labor
slug:       web-techniques
---

There are techniques that aren’t used, from what I know, by today web designers and I want to address them here if it’s possible. I think sometimes we are so eager to come up with something better that we are ending up trying reinventing the wheel when we already have the wheel.

#### 960px width wasn’t that smart

Why [960](http://960.gs/)? Because is a number that has lots of divisors. That’s it? Yes, and a supposable grid system behind it. Hmm, that’s not enough, since complex grid systems can be applied to any surface. What if we design like we have done it for print? Let’s say we chose a paper format, A4 for example, then a DPI, 96 in this case. What’s the width in pixels for this paper format in portrait orientation? 794 pixels. What we gonna do with this number? Well, you can accommodate this size to articles then design everything around it, sidebars, menus, etc. I used this technique when I designed The Journalist last year, one of the popular WordPress themes out there. So, basically every article that was formatted in The Journalist can be printed right away, without needing to reformat every single line. That’s in theory, in practice things can change.

Cameron Moll asks what’s [beyond 960px](http://cameronmoll.com/archives/2009/04/is_it_time_to_move_beyond_960/). I suggest using the same A4 format but at a different DPI, maybe 150, so the resulting width will be 1240px. Also, we can increase the paper size to A3, keeping the same 96 DPI and getting a width of 1124px. We should keep in mind that A3 is more suitable for newspapers, where A4 is used for magazines.

#### Golden ratio isn’t that perfect

Golden ratio value is almost 1.61803399. When I first heard about it I thought that: “Well, if I use this, then everything I do can hold water.” This happens to be true in some cases, but when comes to design an interface things change. There are some [aspect ratios](http://en.wikipedia.org/wiki/Aspect_ratio) currently used for framing: 16:9 (derived from 4×4 and 3×3) for TV screen, 16:10 for computer displays and the traditional 4:3. All of these ratios are bad because they don’t use prime numbers as their base. Prime numbers can lead to better multiplication, since 3 can have more multiples than 4 or 9 in a defined numeric range. There is an exception for 3:2 used in photography but it can’t cropped easily for wide screen and it loses the purpose of a golden ratio.

After thinking like I did above I came up with 5:3 aspect ratio, primarily because the value was close to golden ratio and secondly because both, 5 and 3, are prime integers. On Nostalgia — name of the current design of my site — I used 5:3 ratio for adjusting menu, sub-menu and title line heights, not only for sizing images at 500×300 pixels. I suggest using this ratio for adjusting dimensions between article bodies and sidebars, between headers and menus, or other things (between good and evil if you want to).

I was surprised to see that Google used golden ratio for tab bar in Chrome when it first appeared in September, 2008 like I did one month earlier.

#### Interaction outside the chrome

We are used for years to draw a sandbox at any convenient size called layout and play inside it without thinking about nothing else except a computer monitor. Things have changed, we have to bring the same content — that should look, feel and interact in same manner — from mobile devices to laptop displays, netbooks, televisions, game consoles, even paper, and God knows what other devices will we invent in the future. We have to use ratios and formats that can accommodated all of these. So, why not use the international paper formats like A3, A4, A5, B5, etc.?

*After all that being said, he recognize that he (likes) loves math.*
