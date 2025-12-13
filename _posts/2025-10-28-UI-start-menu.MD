---
layout: post
title: "Devlog #10 – UI - Start Menu"
date: 2025-10-28
---

Created a start menu for the game, with the buttons "Play", "Options", "Leaderboards" and "Quit", to start working on putting
together the game play loop. For now the Options and leaderboards options are not functional, since the Leaderboards button is for
another collaborator on the project to use, while the Options functionality is not a high priority at the current time.

This time i used the option "Strecth to screen" for the canvas, allowing it to automaticly deal with aspect issues, since this was 
an issue on the canvas used in the main game. Where the UI isn't at the correct location for all resolutions and aspect ratios.

I also worked with AI to generate images to use for the buttons and the main menu background, to make it more visually pleasing.
This however turned out a lot more challenging than expected, especially with issues of generating the buttons by themselves and
not together with the background. The main issue here was the size and formating of the files, where I had difficulties getting the
AI to generate a file with only the buttons needed in them. After spending a lot of time working on this, I decided to simply have 
it create the buttons as part of the background image and then making the UI buttons transparent and laying them on top of the 
button images. While I would have liked to create the buttons by themselves and adding the image to the button object in the scene,
I decided that this was not worth the amount of time it was taking and moved on, since it would make a minimal difference.

I realized that image/asset generation using AI, was a lot more challenging than expected, especially when trying to go for more 
specific generations. Since the AI was not great at following directions, with what to generate or change on the generated images.


![Enemy movement code](/github-portfolio/images/blog/MainMenu.PNG)

