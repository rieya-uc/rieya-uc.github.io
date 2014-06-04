---
layout: post
title: "Roll The Dice"
date: 2014-06-03 14:22:18 +0100
comments: true
categories:
    - Javascript
    - Phaser
    - code
    - demo
---

Things to do:

-  Learn Javascript
-  Try out [Phaser](http://phaser.io/)
-  Get comfortable with putting stuff online

To that end, here's something short I wrote to try out Phaser. Click the dice to make them roll.

<!--more-->

<script type="text/javascript">
    var path = '../../../../../blog_demos/';
</script>

<div id="demo" class="centre">

    <script type="text/javascript" src= "../../../../../blog_demos/libs/phaser.min.js"></script>
    <script type="text/javascript" src= "../../../../../blog_demos/rolling_dice/Dice.js"></script>
    <script type="text/javascript" src= "../../../../../blog_demos/rolling_dice/rolling_dice.js"></script>
</div>
<pre><br></pre>

To get the roll effect I used a blur filter in combination with spritesheet animation and random rotation. The dice extend Phaser.Sprite so that they can manage their own values. With all the [examples](http://examples.phaser.io/) available on the Phaser website, it was fairly easy to work out what was needed (working out the intricacies of Javascript on the other hand...).

All the code is available on [github](https://github.com/rieya-uc/blog_demos), and in the rolling_dice folder specifically.

Where to now? A game of Yahtzee perhaps?
