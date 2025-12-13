---
layout: post
title: "Devlog #7 – Second enemy and scaling enemies"
date: 2025-09-17
---
The goal since the last devlog was to add more depth to the gameplay, by adding another enemy to the game, with it's own unique
stats. The plan was to create a larger enemy by size, with a lot of hp and damage, that moves slower compared to other enemies.
Making it able to be kited easier. Other than that the enemies needs to be scaled by the time in the game, making the game get 
more difficult the longer the game has been running. I also have to create an enemy spawner, that can pick what enemy to spawn
and scale it with the clock in the game.

To do so I first had to find some suitable free assets, to use for the enemy and it's animations. Afterwards I had to allow the
enemy movement and health/damage scripts to be have public changeable values, that can be set when the enemies is spawned. I
created an enemy spawner and a clock for the game to allow for spawning enemies of different types and scaling based on time.

To allow for all these changes to how the enemy is spawned, I needed to change a lot of fundamental things about how the scripts
worked. Allowing for the spawner script to set the enemies damage and health values with paremeters, to allow them to scale with
the clock. I also created a list of enemies to spawn based on a given weight, making the spawner able to randomly spawn different
types of enemies, and make it so there are more common easy enemies than rare harder enemies. There were a lot of challenges
involved with this, and it was quite difficult to get all the scaling values correct, based on the time. I had to try a lot of
different ways to scale the enemies, to get it to work properly. Making the second enemy was quite easy, as I had experience 
creating the first enemy, and a lot of the scripts were made to be reusable for all enemies. Like the EnemyHealth, EnemyDamage
scripts and enemyMovement scripts, this allowed for a more streamlined process, where most of the work was in the enemy spawner
and scaling of the values for enemeies.
I am however a bit worried about the way the enemies are randomly selected for spawning and how it will function later on in the
game process. If there will be very rare enemies, you could potentially get very unlucky and spawn 2 very hard enemies at once.
However this also makes it so every game isn't the same, so I'm still reflecting upon if this is a problem or not and will wait 
and see if it becomes one later down the line.

![Enemy movement code](/github-portfolio/images/blog/EnemySpawner.PNG)

![Enemy movement code](/github-portfolio/images/blog/EnemyScaling.PNG)


