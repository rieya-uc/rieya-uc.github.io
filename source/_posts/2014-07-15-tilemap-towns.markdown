---
layout: post
title: "Tilemap Towns"
date: 2014-07-15 17:17:28 +0100
comments: true
categories:
    - Phaser
    - Tilemaps
    - Collision
    - P2
    - Arcade
    - Sprite animation
    - Javascript
    - demo
---

Come in, have a look around. I've created an rpg-style town for you to explore. 

<!--more-->

Use the cursor keys to move, or use the on-screen arrows.

<script type="text/javascript">
    var path = '../../../../../blog_demos/';
</script>

<div id="demo" class="centre">

    <script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/phaser/2.0.6/phaser.min.js"></script>
    <script type="text/javascript" src="../../../../../blog_demos/explore_the_farm/Boot.js"></script>
    <script type="text/javascript" src="../../../../../blog_demos/explore_the_farm/Preloader.js"></script>
    <script type="text/javascript" src="../../../../../blog_demos/explore_the_farm/MainMenu.js"></script>
    <script type="text/javascript" src="../../../../../blog_demos/explore_the_farm/Game.js"></script>
    
    <script type="text/javascript" id="script">
      
      window.onload = function() {

      
      //	Create your Phaser game and inject it into the gameContainer div.
      //	We did it in a window.onload event, but you can do it anywhere 
      // (requireJS load, anonymous function, jQuery dom ready, - whatever floats your boat)
      var game = new Phaser.Game(800, 600, Phaser.AUTO, "demo");
      
      //	Add the States your game has.

      game.state.add('Boot', TilemapTowns.Boot);
      game.state.add('Preloader', TilemapTowns.Preloader);
      game.state.add('MainMenu', TilemapTowns.MainMenu);
      game.state.add('Game', TilemapTowns.Game);

      //	Now start the Boot state.
      game.state.start('Boot');
      
      };
      
    </script>
</div>
<pre><br></pre>

If you're using Firefox and notice it to be laggy, try it in a different browser (Chrome and IE work fine for me). The framerate drop doesn't seem to show up when I run the game locally, but only once I've pushed it to the blog. I'm not quite sure how to go about debugging something like that.

The version that's up now is using Phaser's Arcade physics to check for collisions. I also wrote a version using P2 physics, have a root around the [repo](https://github.com/rieya-uc/blog_demos/tree/master/explore_the_farm) if you'd like to compare the two. There's some changes coming to the P2 api, so depending on how far into the future you're reading this, the P2 physics town may or may not work.

There's also a third physics system, Ninja, which I haven't tried out yet. Don't know which one to use? Read the explanation [here](http://www.html5gamedevs.com/topic/4518-explaining-phaser-2s-multiple-physics-systems/).

Fancy making your own town? You'll need [Tiled](http://www.mapeditor.org/), and the wonderful lpc tilesets from [opengame.art](http://opengameart.org/lpc-art-entries).

Check out my [code](https://github.com/rieya-uc/blog_demos), it seems to be growing.

    
