---
layout: post
title: "UI - Makeshift Scrolling"
date: 2014-09-01 16:03:58 +0100
comments: true
categories:
    - Phaser
    - UI
    - Javascript
---

I've been writing various UI bits and bobs for a different project I've been working on, including this rather colourful scrollpane. There's not much to look at, everything works as expected, and I've added a few extra buttons to show it off.

<!--more-->

<script type="text/javascript">
    var path = '../../../../../blog_demos/';
</script>

<div id="demo" class="centre">
    <style>
        canvas {border : 1px solid black;}
    </style>

    <script type="text/javascript" src="../../../../../blog_demos/libs/phaser.min_2.07.js"></script>
    <script type="text/javascript" src="../../../../../blog_demos/makeshift_scrolling/Pane.js"></script>
    <script type="text/javascript" src="../../../../../blog_demos/makeshift_scrolling/Scrollpane.js"></script>
    <script type="text/javascript" src="../../../../../blog_demos/makeshift_scrolling/makeshift_scrolling.js"></script>

</div>
<pre><br></pre>

A guide on [scrollbar mechanics](http://csdgn.org/inform/scrollbar-mechanics) helped immensely with the not-so-obvious issues that arose. Just bear in mind that in Phaser the position (0,0) is top-left of the screen rather than bottom-left, so scrolling downwards runs in the opposite direction to that outlined in the guide.

Other than that, the fiddly bit was having to account for borders in the background image and scrollbar which the pane content shouldn't move over. Small, pixel-sized errors compound to window-sized errors as the pane content grows! I think I've accounted for every border offset now though.

Check out the scrollpane code [here](https://github.com/rieya-uc/blog_demos/tree/master/makeshift_scrolling), and if you wish, peruse the other [demo code](https://github.com/rieya-uc/blog_demos).
