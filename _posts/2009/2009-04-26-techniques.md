---
layout: default
title: Web techniques
---

There are techniques that, from what I know, aren't used by today's web designers, and I want to address them here. I think sometimes we are so eager to come up with something better that we end up trying to reinvent the wheel when we already have the wheel.

#### 960px width wasn't that smart

Why [960](http://960.gs/)? Because it is a number with lots of divisors. That's it? Yes — plus a supposed grid system behind it. Hmm, that's not enough, since complex grid systems can be applied to any surface. What if we designed the way we used to for print? Let's say we chose a paper format — A4, for example — and a DPI, 96 in this case. What's the width in pixels of that paper format in portrait orientation? 794 pixels. What do we do with this number? Well, you can fit articles to this size and then design everything around it: sidebars, menus, and so on. I used this technique when I designed The Journalist last year, one of the popular WordPress themes out there. Basically, every article formatted in The Journalist can be printed right away, without reformatting a single line. That's the theory; in practice, things can change.

Cameron Moll asks what's [beyond 960px](http://cameronmoll.com/archives/2009/04/is_it_time_to_move_beyond_960/). I suggest using the same A4 format but at a different DPI, maybe 150, so the resulting width would be 1240px. We can also increase the paper size to A3, keeping the same 96 DPI and getting a width of 1124px. Keep in mind that A3 is more suitable for newspapers, while A4 is used for magazines.

#### Golden ratio isn't that perfect

The golden ratio's value is almost 1.61803399. When I first heard about it, I thought: "Well, if I use this, then everything I do can hold water." This happens to be true in some cases, but when it comes to designing an interface, things change. There are some [aspect ratios](http://en.wikipedia.org/wiki/Aspect_ratio) currently used for framing: 16:9 (derived from 4×4 and 3×3) for TV screens, 16:10 for computer displays, and the traditional 4:3. All of these ratios are bad because they don't use prime numbers as their base. Prime numbers lead to better multiplication, since 3 has more multiples than 4 or 9 in a defined numeric range. There is an exception — the 3:2 used in photography — but it can't be cropped easily for widescreen, which defeats the purpose of a golden ratio.

After thinking like I did above, I came up with a 5:3 aspect ratio — primarily because its value is close to the golden ratio, and secondly because both 5 and 3 are prime integers. On Nostalgia — the name of my site's current design — I used the 5:3 ratio to adjust menu, sub-menu and title line heights, and not only for sizing images at 500×300 pixels. I suggest using this ratio to adjust the dimensions between article bodies and sidebars, between headers and menus, or other things (between good and evil, if you want to).

I was surprised to see that Google used the golden ratio for the tab bar in Chrome when it first appeared in September 2008 — just like I did one month earlier.

#### Interaction outside the chrome

For years we have been used to drawing a sandbox of any convenient size, called layout, and playing inside it without thinking about anything other than a computer monitor. Things have changed. We have to bring the same content — which should look, feel and interact in the same manner — from mobile devices to laptop displays, netbooks, televisions, game consoles, even paper, and God knows what other devices we will invent in the future. We have to use ratios and formats that can accommodate all of these. So why not use the international paper formats like A3, A4, A5, B5, and so on?

*After all that being said, he recognizes that he (likes) loves math.*
