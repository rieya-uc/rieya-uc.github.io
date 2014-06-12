---
layout: post
title: "Drag The Square"
date: 2014-06-11 16:01:37 +0100
comments: true
categories:
    - Phaser
    - Phaser.Group
    - Phaser.Sprite
    - Javascript
    - code
    - demo
---

This one took somewhat longer than I expected. I wanted to create a collection of sprites that could be dragged around the screen as one.

Click the button to make a random rectangle appear somewhere on screen. Drag it around, then add a few more.
<!--more-->
<script type="text/javascript">
    var path = '../../../../../blog_demos/';
</script>

<div id="demo" class="centre">

    <script type="text/javascript" src= "../../../../../blog_demos/libs/phaser.min.js"></script>
    <script type="text/javascript" src= "../../../../../blog_demos/drag_square/Square.js"></script>
    <script type="text/javascript" src= "../../../../../blog_demos/drag_square/drag_square.js"></script>
</div>
<pre><br></pre>

The rectangle (Square.js), is made up of several sprites; its body and four borders. They are contained in an extended Phaser.Group (see [example](http://examples.phaser.io/_site/view_full.html?d=groups&f=extending+a+group.js&t=extending%20a%20group)). Groups have no dimensions, which means no click area, and no drag event. Therefore to get the rectangle to move as one, I enabled drag on the body and kept the borders aligned during `update()`.

Everything inside a Group is moved relative to the Group's position. Don't do what I did and move the Group after the body's been dragged as an alternative to aligning the sprites individually, because you'll find the body has moved twice as far and your rectangle will be rectangular in name only. I found it simpler to keep all Groups at position (0,0), and position the sprites relative to that. The downside to doing it this way is that moving the Group via `(group.x, group.y) = some position` screws up the drag.

I think that if I were to redo this, I would forego drag altogether and use mousedown events instead, so that I could move the Group as a whole, and not the individual sprites.

Code? All available on [github](https://github.com/rieya-uc/blog_demos), and in the drag_square folder specifically.
