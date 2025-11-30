---
layout: post
title: "Devlog #11 – UI - Game over screen"
date: 2025-11-14
---

Created a Game over screen for when the player dies, this screen pauses the game and pops up once the players health reaches 0.
This is a vital part of creating the game loop, since it will allow the player to actually lose the game and start over again.
This game over screen has 2 buttons, with one being a "Play again" button that restarts the game from the start again. The other 
button is a "Main menu" button, that takes the player back to the main menu screen. This completes the game loop, of being able to
Start the game, play till you die, and then start the game over again, trying to get further.

There was a lot of issues with restarting the game using the "Play again" button, where a lot of references was getting lost and not
properly assigned to the necessary objects, this made the game unplayable and caused a lot of issues like enemies not spawning,
the player keeping their upgrades from their previous runs and other issues. This turned out to be an issue with using the method
"DontDestroyOnLoad" for some of the objects in the scene, and the way some scripts were structured, where they tried creating a new
gameobject on loading in and if there already was an instance, it would delete the new instance and keep the one already in play.
This caused issues because we also used a few scripts that auto assign their references, this turned out to be causing the references 
to auto assign the new instance that then gets deleted because there already was another instance of the object, causing the reference
to go missing, which caused the scripts to get errors and not run.

To fix this we simply removed the use of "DontDestroyOnLoad" for now, since we're not using the benefits that this functionality gives,
since we currently only have a single level/scene and don't need to keep the same instance of the player when loading a new scene.
This could cause issues in the future, if we decided to create more levels, however this is currently not the plan for this project,
since we do not have the time to implement this.

Once this was fixed the game loop worked as it should and the UI is working as intended.
