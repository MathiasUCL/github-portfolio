---
layout: post
title: "Devlog #9 – Third enemy and enemy drops"
date: 2025-10-03
---
The goal since the last devlog has been to create more depth in the game by creating a ranged enemy and also adding
drops and scaling these drops and xp drops from enemies. To allow for a better functioning gameplay, the enemies
need to drop different amount of experience based on the enemy type and how far into the game the player is. Making
harder and higher scaled enemies drop higher amounts of experience aswell. The idea with the ranged enemy is to add more
depth to the way the player plays the game, so the player isn't just running away from enemies, but also has to dodge the
ranged enemies attack.

For the third enemy I decided to go for a ranged enemy that charges a magic attack, that then shoots a magic ball after the
player. So I first have to find assets that suit these requirements, afterwards I have to create a new movement script for 
ranged enemies, that is also flexible so it works with enemies that do not need to charge before shooting.
To allow enemies to drop a different amount of experience, I have to change the way experience is dropped in our game,
creating a new script to handle drops, that then also handles the experience drops, which is then changed based on the game time.

Creating an enemy that charges their attack, before then shooting it was a lot more complicated than I imagined, creating a ton of
different issues I hadn't expected to occur. There was especially a lot of issues with the way animations was played, however it was 
a great learning experience as I learned to make use of pivot points. Using pivot points I could fix the issues with animations of
different sized sprites making the character jump around all over the place when charging their attack. There was also a lot of 
difficulties with making the animator trigger the correct animations at correct times, stopping the characters movement and animation
while charging. To not allow the charging and charging animation to occur while walking and to properly time the instanced projectiles,
with the timing of the attack. This took a very long time to figure out, since I was very unfamiliar with attacking animations and animations
outside of walking in general.
Creating the drop script was a lot simpler and straight forward, reusing a lot of earlier functionality, I was able to quite easily scale
the experience dropped with the time and changing experience dropped based on the enemy prefab. The drops outside of experience still needs 
more work, however the primary functionality is there and just needs to be changed to fit the type of drops, we decide to use for our game.

![Enemy movement code](/github-portfolio/images/blog/RangedEnemyUpdate.PNG)


![Enemy movement code](/github-portfolio/images/blog/RangedEnemyMovement.PNG)


![Enemy movement code](/github-portfolio/images/blog/RangedAttack.PNG)


![Enemy movement code](/github-portfolio/images/blog/DropScript.PNG)