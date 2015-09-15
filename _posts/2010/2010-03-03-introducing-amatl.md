---
layout:     post
date:       2010-03-03 15:33:33
edit:       2013-03-19 20:50:20
title:      "Introducing Amatl"
category:   meaningful-labor
slug:       introducing-amatl
syntax:     true
---

In today’s world where millions of documents are electronic we need a format that is easy recognizable by most devices and operating systems that we use: Mac OS X, Windows, laptop, desktop, Linux, iPhone, eReaders, etc.

> From the start, I want to say that the idea, concept, examples and eventually writing the specification, are all mine. So, go ahead, read the lines below and blame me for things that aren’t the way they should be.

The name, Amatl, comes from a form of paper that was manufactured in pre-Columbian Mesoamerica. There are [more details about it](http://en.wikipedia.org/wiki/Amatl) on Wikipedia, of course. My Amatl is based on HTML5 and CSS (2.1 now and 3.0 in the future), two standards that raised the bar with what we can do in terms of layout, embedding fonts, typography, grid and images or blocks positioning. Basically, Amatl is actually a file format that wants to display paper documents inside browsers without any additional tools or software. The format isn’t intended at replacing Adobe’s PDF format or Microsoft’s XPS; it should be used as a complementary format, open and supported by the entire industry. The closest resembles to it can be [EPUB format](http://en.wikipedia.org/wiki/EPUB) but they are two completely different concepts.

#### Compatibility

The good part about this format is that it can be recognizable by old browsers too, I name Firefox 2 and IE7 here. It’s just HTML after all, right?

#### Differences

There will be no differences when it comes to HTML5 syntax, maintaining the current specification is very important. Still, I recommend not using *meta* attributes because they will be present in a CSS metadata header.

The most important differences to CSS is introduction of a DPI value and a CSS metadata header. It will be used to write documents at a higher DPI than 96, which is the standard to all web pages on Internet today.

#### Structure

The Amatl document files should be packed in a ZIP container, having .am extension (like Document1.am) for offline usage and not only. Browser support will be needed for reading HTML files packed inside a ZIP. It can also be served directly from a server with the following structure:

{% highlight css linenos %}
index.html
page-2.html
page-3.html
|-- styles
   |-- screen.css
   |-- print.css
|-- fonts         /* embeddable fonts should be placed here */ 
|-- languages     /* support for multi languages documents */
   |-- index-en-us.html
   |-- index-en-gb.html
   |-- index-ro-ro.html
|-- images
|-- videos
|-- audios
{% endhighlight %}

#### Writing, printing and scaling the documents

It should be very easy to write an Amatl document, like writing a blog post with basic HTML tags: *p*, *a*, *strong*, etc. This is because the HTML5 structure of the format is very easy. You can view the source of this example: [Document 1](http://lucianmarin.com/amatl/examples/doc2/). Printing documents can use a *print.css* file or the browser should interpret the *screen.css* (remove styles for body and article tags) and print the pages exactly like they are displayed on the screen.

As I said before, Amatl will supports writing HTML5 with custom DPI through CSS. You can understand how this works by viewing the [Warp](http://lucianmarin.com/amatl/examples/warp/) example from Firefox (or any other browser that supports zooming) at minimum zoom. If browsers will adopt this format, you can view higher quality web documents right in your browser, including higher DPI images and graphics and you can print them right away without needing any other software.

Amatl can also use a single HTML file, that embeds CSS, fonts and images and separates pages accordingly. You can see this in the [Document 2](http://lucianmarin.com/amatl/examples/doc2/) example. This can be dropped from the specifications since I prefer a more standard structure for the format.

#### License

The format should and will be open since it’s based on open technologies, but it will require a commercial license for software products or web applications for writing, managing or printing the documents. More about this in the future and don’t forget there is [an Amatl page](http://lucianmarin.com/amatl/) dedicated for this very project.
