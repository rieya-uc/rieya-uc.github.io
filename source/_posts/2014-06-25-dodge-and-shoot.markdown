---
layout: post
title: "Dodge and Shoot"
date: 2014-06-25 13:55:45 +0100
comments: true
categories:
    - Phaser
    - Phaser templates
    - code
    - demo
    - Javascript
---

For this demo I decided I wanted to do something a little longer. See how many monsters you can kill before you succumb to the inevitable.

<!--more-->

Hold the left mouse button to strafe.

<script type="text/javascript">
    var path = '../../../../../blog_demos/';
</script>

<div id="demo" class="centre">
    <link rel="stylesheet" type="text/css" href="http://fonts.googleapis.com/css?family=Handlee">
    <script type="text/javascript" src="../../../../../blog_demos/libs/phaser.min.js"></script>
    <script type="text/javascript" src="../../../../../blog_demos/arena_shooter/Boot.js"></script>
    <script type="text/javascript" src="../../../../../blog_demos/arena_shooter/Preloader.js"></script>
    <script type="text/javascript" src="../../../../../blog_demos/arena_shooter/MonsterSpawner.js"></script>
    <script type="text/javascript" src="../../../../../blog_demos/arena_shooter/MainMenu.js"></script>
    <script type="text/javascript" src="../../../../../blog_demos/arena_shooter/Game.js"></script>
    
    <script type="text/javascript">
      
      window.onload = function() {

      
      //	Create your Phaser game and inject it into the gameContainer div.
      //	We did it in a window.onload event, but you can do it anywhere 
      // (requireJS load, anonymous function, jQuery dom ready, - whatever floats your boat)
      var game = new Phaser.Game(800, 600, Phaser.AUTO, "demo");
      
      //	Add the States your game has.

      game.state.add('Boot', ArenaShooter.Boot);
      game.state.add('Preloader', ArenaShooter.Preloader);
      game.state.add('MainMenu', ArenaShooter.MainMenu);
      game.state.add('Game', ArenaShooter.Game);

      //	Now start the Boot state.
      game.state.start('Boot');
      
      };
      
    </script>
</div>
<pre><br></pre>

It still needs a lot of polish, but it's a good starting point for developing something more complex. Later on, when I have the time, I'll have a go at fleshing it out.  Give the monsters more of a bite, they're too easy to dodge at the moment. Monster bullets, levels, bosses, collectibles, player upgrades, sound ... what else?

If you decide to take a peek at the [code](https://github.com/rieya-uc/blog_demos), you'll notice the sudden increase in .js files. I've moved on to using Phaser's [templates](https://github.com/photonstorm/phaser/tree/master/resources/Project%20Templates) as a way of organising my code. It sets everything up to load in stages, with space for a preloader bar and logo screen if needed. Useful for when my demos start getting bigger.

As an aside, here's the fun little game I shamelessly ripped my idea from, [Death Vs Monstars](http://www.kongregate.com/games/GameReclaim/death-vs-monstars). And of course, here's a link to my [code](https://github.com/rieya-uc/blog_demos).



