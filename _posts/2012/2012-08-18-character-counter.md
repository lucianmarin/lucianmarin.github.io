---
layout:     post
date:       2012-08-18 03:14:15
edit:       2013-03-19 20:58:17
title:      "Textpattern Character Counter"
category:   meaningful-labor
slug:       character-counter
syntax:     true
---

The recent [announcement](http://dev.twitter.com/blog/changes-coming-to-twitter-api) by Twitter made me sad. I talked about the issues with social networks in *A Dash in Space-Time Continuum* and *Disconnected*, so I’m not gonna discuss it again.

Anyway, two days before the announcement I launched my own private column featuring links and news that I find interesting. It’s a twitterrific-delicous-pinboarding kind of thing. Of course, it even comes with a RSS feed and character counter. How did I do it? The main ingredients were: Textpattern, FeedBurner, jQuery and charCount.js plugin.

I used FeedBurner to enhance the feed provided by Textpattern. The links page was set to be the default admin tab. The character counter was added because I need to keep myself limited, not to pollute the air traffic on the interwebs. For everything else, I can always write an article.

#### Back on the subject

It’s pretty easy to add charCount.js from [CSS Globe](http://cssglobe.com/jquery-plugin-simplest-twitterlike-dynamic-character-count-for-textareas/) since TextPattern comes by default with jQuery. All you have to do is to edit *txplib_head.php* from */textpattern/lib/*. The you have to add the code below after jQuery declaration:

{% highlight html linenos %}
<script type="text/javascript" src="charCount.js">
</script>
<script type="text/javascript">
    $(document).ready(function(){
        $("#link-description").charCount();
    });
</script>
<style type="text/css">
    .counter { position: absolute; }
    .counter.warning { color: #e40; }
</style>
{% endhighlight %}

Make sure you backup the original *txplib_head.php* before you do this and upload charCount.js where jquery.js file is located. The same thing can be applied to the textarea for article editing, all you have to do is to add the right ID in the code above.
