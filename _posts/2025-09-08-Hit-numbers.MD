---
layout: post
title: "Devlog #6 – Hit numbers"
date: 2025-09-08
---
The goal since the last devlog has been to allow the player to see hit numbers, for both when he takes damage
and deals damage. Which is supposed to be done by making numbers pop up, in different colours based on what
type of damage the player dealt.

To do so I first had to set up a damage type system that, which worked hand in hand with the effect system.
This made it possible to differentiate the damage type that affects the enemy, and made it possible to create
hit numbers based on what type of damage was done to the enemy. An example would be White damage from the sword
swing as physical damage, which then applied a bleed and burn that showed up respectively as red for the bleed
and orange for the fire.

I ran into quite a lot of difficulties creating the hit numbers, since most of the different scripts had to 
interact in some way to pass along the needed information. This made it more of an advanced task than first
expected. There was also a lot of different Unity features used that I had never used before, which added to
the complexity of the task. However in the end I managed to make it work and have the damage numbers pop up
on the target that takes damage, based on the type of damage done.
There are still improvements to be made on this feature, both visually and code wise. The idea is to make DoTs
not spam your screen like they're doing now, but have them add up and increase the already existing damage pop
up for that instance of damage. Which is what I'll be working on till the next devlog. Improve the visual
clarity of the hit numbers both for player and enemy damage.


![DamageNumbers code](/github-portfolio/images/blog/DamageNumbers.PNG)