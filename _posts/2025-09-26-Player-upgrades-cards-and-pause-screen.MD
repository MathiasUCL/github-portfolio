---
layout: post
title: "Devlog #8 – Player upgrades cards and pause screen"
date: 2025-09-26
---
The goal since the last devlog has been to make a screen pop up with selectable upgrades for the player, when they level up.
The idea here is to show 3 different upgrade cards with different upgrades on them, which you can then select one of that
adds that upgrade to your character. To do so there is also a need for a way to pause the game, when the player levels up
so that they do not die when chosing upgrades.

To make this possible the first step is to create the pause function, using the esc key to pause the game. After that is done
the pause function can be reused and triggered when the player levels up, and then untriggered when the player has chosen their
upgrade of choice. There is a need to create an UI element that spawns in which is triggered by the player level up, that then 
randomly chooses from a list of available upgrade cards, and shows 3 different upgrade cards with a random rarity. To make this
possible there is a need for a list of available cards and rarities, to then be rolled on with different weights for the items, 
so that legendary cards are more rare than common cards, with the more rare cards giving better upgrades. There is also a need
for a way to create these cards in a easy way, to allow for more cards in the future.

This functionality has been very difficult to create, since it required a lot of different scripts to work together. I started with
creating the pause function, which was the easy part. I then moved onto trying to get an UI element to pop up when the player leveled
up as a trigger, I started with using hard coded cards to test things out. But later on I moved over to having a container for the
cards, that then creates 3 instances of these randomly selected cards on the screen once triggered. There are some difficulties here
with the text on the cards getting streched, that needs to be fixed in the future. Then I started working on creating different
cards and adding them to the list of possible cards to draw, where I ended up making the cards as scriptable objects, to allow 
for easier creating of new cards. After this was done I had to create a way for these upgrades to be able to apply the selected
upgrade to the player character, using the players current stats and adding the upgrades ontop of those. I also created a new stat
called luck, that gives the player better odds of drawing rarer cards and created cards for this stat aswell.

All in all this was a huge new functionality that was very difficult to create, since I ran into a lot of issues both with the scripts
and the UI elements of this task. And the end result is not very satisfactory yet, especially the UI part, since there are a lot of
issues with streching the cards, which then streches the text, making it hard to read. This function needs to be looked at and improved 
upon again later on in the process, if the timeframe allows for this.