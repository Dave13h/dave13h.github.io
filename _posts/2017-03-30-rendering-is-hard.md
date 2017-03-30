---
layout: post
title: "_Rendering is hard_"
date: 2017-03-30
---

Another great quote is _"learn to laugh at yourself"_, which is why I decided actually do something with my github pages repo. In the laziest possible way, I am going to post stupid videos of my crazy attempts at doing something cool with OpenGL.

I've already managed to build a fairly usable deferred rendering engine and even cobbled together something resembling Physically Based Rendering, or at least the lighting works on some of the common aspects of PBR but one thing that has alluded me for far too long is how the Assimp library imports models with bones and animations.

The first step is only a tiny step of taking the ENTIRE data structure apart and hoping that when you put it into GL that it all lines up the way you hope *spoiler* it doesn't *spoiler*

[![Please put me out of my misery!](https://img.youtube.com/vi/4h3poEeNnow/0.jpg)](http://www.youtube.com/watch?v=4h3poEeNnow)

But there is definately some real bits of model in there right? I mean you can see a head and things are kind of animating? After jiggling around the matrices a little and making sure that the multiple meshes in the data line up with the bone weights it looks like we're getting somewhere!

[![There can be only one!](https://img.youtube.com/vi/XQLjo3vqJcQ/0.jpg)](http://www.youtube.com/watch?v=XQLjo3vqJcQ)

What the hell? If you look carefully you can see his finger tips are traveling across dimensions and ripping apart time and space! Also his hood is clearly not of this world either. Oh yeah, ASSIMP forgot to metion that some nodes have ```_$AssimpFbx$_``` in the name if it can't match them or they are actually just identity or something, not entirely sure. But for a laugh I thought I could just detect those and strip that bit out leaving the original bone name in there. Oh look at that, it works. Don't really want to question if that is right :P

Sprinkle some interpolation between animation frames and BLAM! We have some animation!

[![Double the cinematic framerate!](https://img.youtube.com/vi/6obodEmGO3c/0.jpg)](http://www.youtube.com/watch?v=6obodEmGO3c)

Oh, did you want to blend between multiple animations, yeah that works too :)

[![Oh hai](https://img.youtube.com/vi/JTI-N7MZga0/0.jpg)](http://www.youtube.com/watch?v=JTI-N7MZga0)

Let's see what is next on the things I want to implement but don't understand list.
