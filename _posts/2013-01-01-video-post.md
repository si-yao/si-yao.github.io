---
layout: post
title: "A Post with my Video"
description: "Custom written post descriptions are the way to go... if you're not lazy."
tags: [sample]
comments: true
share: true
---
<iframe height="498" width="510" src="http://player.youku.com/embed/XNjczNDMwNTQw" frameborder="0" allowfullscreen></iframe>

## This is my first original video

This is my first orignial video in my life. I happened to play the multi-player version of Flappy Bird online, a very popular mobile game for a time. I saw the source code and found that this game is purely made by javascrip! How amazing! For the sake of respect, I hacked the code and gave the bird super power . I feel happy to see all of other birds fall down time after time, while my bird is free to across to wall. I uploaded the video to [bilibili](www.bilibili.tv/video/av967176/) and watched by thousands of people, and got nearly a hundred comments. That's fun!

##Descriptions about the function of embeded video

Video embeds are responsive and scale with the width of the main content block with the help of [FitVids](http://fitvidsjs.com/).

Not sure if this only effects Kramdown or if it's an issue with Markdown in general. But adding YouTube video embeds causes errors when building your Jekyll site. To fix add a space between the `<iframe>` tags and remove `allowfullscreen`. Example below:

{% highlight html %}
<iframe width="560" height="315" src="//www.youtube.com/embed/SU3kYxJmWuQ" frameborder="0"> </iframe>
{% endhighlight %}