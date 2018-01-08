# 100 Days Of Code - Log

### Day 1: January 1st, 2018.

**Today's Progress**: I've only recently started coding and have been taking a course on Unity and C# on Udemy. Today I worked on enemy and player behaviors in a 2D space shooter game, adding explosion effects on death. 

**Thoughts:** Things went really well today, with no issues or compiler errors on my first attempt to add effects on object destruction. Both player and enemy ships explode into small stardust when health is <=0. 

**Link to work:** [EnemyBehavior Script](https://github.com/fauletto/100-days-of-code/blob/master/Day001-EnemyBehaviorScript)

### Day 2: January 2nd, 2018.

**Today's Progress**: Continuing to work on my code for my Udemy course. I created a formation spawner for enemy ships that respawns enemies once they are killed. 

**Thoughts:** Mostly working as intended, but I need to figure out how to alter the time between enemy respawns. As of now, as soon as the formation is destroyed, enemies pop back in one at a time, in order. I would like to figure out a way to shuffle them around and also randomize the spawn timing a bit more.

**Link to work:** [EnemySpawner Script](https://github.com/fauletto/100-days-of-code/blob/master/Day002-EnemyFormationSpawner)

### Day 3: January 3rd, 2018.

**Today's Progress**: Today was a really good day for learning and practicing. I spent most of my lunch break reading the C# Yellow Book to expand my C# knowledge a bit. During my drives to work, the gym, and home, I listened to the CodeNewbie podcast to try to immerse myself in as much programmer talk as possible. Once I got home, I continued to progress through [Bob Tabor's C# Fundamentals for Absolute Beginners](https://mva.microsoft.com/en-us/training-courses/c-fundamentals-for-absolute-beginners-16169) course, which I'm really enjoying for learning the basics of C# and Visual Studio. 

*But wait*--I did actually still manage to find time to code today! I broke off of my Udemy coursework and decided to begin working on my own text-based RPG/adventure game in Unity. I only began by creating the very basics of the game, but I have working game states and keyboard commands that transition between scenes. 

I plan to take this code and expand it dramatically; I would eventually like to flesh out the story, add items, enemies, and a few combat scenes in the game. The story that is in place now is simply a placeholder to test the game systems and get them working. Eventually--when I'm more comfortable with both C# and Unity--I would like to add a graphical interface and turn this into a 2D RPG/adventure game. But, I'm pleased with the progress of simply getting things to work for now.

Whew...long entry today. Without further ado, the code for my basic placeholder story-based RPG/adventure game can be found below!

**Thoughts:** Really pleased with my productivity today. I didn't create/code anything mind-blowing, but it *worked*, which is a huge step in the right direction for a newbie such as myself. I am really starting to immerse myself into as many coding resources as possible, including books, podcasts, and communities. I'm really loving where this is going!

**Link to work:** [TextAdventureTest Script](https://github.com/fauletto/100-days-of-code/blob/master/Day003-TextAdventureTest)

### Day 4: January 4th, 2018.

**Today's Progress**: Today was a snow day, so no work! That means more time to code! I started the day reading a bit more of [Rob Miles' C# Yellow Book](http://www.csharpcourse.com/) and finishing up [Bob Tabor's awesome C# Fundamentals for Absolute Beginners](https://mva.microsoft.com/en-us/training-courses/c-fundamentals-for-absolute-beginners-16169) course. After that work, I went on to coding by myself.

So, I decided to start taking the training wheels off and be a bit more ambitious today. I have really enjoyed the Udemy Unity coursework I've done so far, but I'm taking a brief break from it to take what I've learned and try to apply it to my own projects outside of the course. Since I decided yesterday that I'd like to expand my very basic text/story-based RPG, I made an effort to create a class template for two character classes. Nothing much to show in terms of display within the game, but this is more of the background stuff that will be running in Unity to power the characters. 

**Thoughts:** Another productive day today! I don't have much to show for my work, but I do have a few scripts I'm happy with. Tomorrow I will plug away at this a little more, and maybe come up with a way to display this in the start screen (e.g., selecting your class and displaying their starting attributes/skills).

**Link to work:** [Character Script](https://github.com/fauletto/100-days-of-code/blob/master/Day004-CharacterScript),
[Engineer Script](https://github.com/fauletto/100-days-of-code/blob/master/Day004-EngineerScript),
[Marine Script](https://github.com/fauletto/100-days-of-code/blob/master/Day004-MarineScript)

### Day 5: January 5th, 2018.

**Today's Progress**: Another snow day, another code day! I decided to jump back into my Udemy C#/Unity coursework and continue to work on my space shooter, Star Swarm. I did a lot of the work without the assistance of the videos/instructors and updated/cleaned up some of my older scripts. I added a music player that starts up when you load the game, loops, and destroys any additional music players that are spawned when the player is taken back to the start screen. I also added sound effects to my player and enemy ships, both for firing lasers and for when they are destroyed. Additionally, I added a UI score overlay, and created a function to increase the player's score by 150 points for each enemy destroyed.

**Thoughts:** All in all, another pretty productive day. I didn't create or code a lot of new products, but I updated, cleaned up, and improved some of my older scripts, all on my own! I think that was the biggest achievement for me today: not needing the videos or instructions to improve the scripts. I know I can still improve a *ton* from here, but I feel like I'm making baby steps each day.

**Link to work:** [ScoreKeeper Script](https://github.com/fauletto/100-days-of-code/blob/master/Day005-ScoreKeeperScript),
[MusicPlayer Script](https://github.com/fauletto/100-days-of-code/blob/master/Day005-MusicPlayerScript),
[Updated Enemy Script](https://github.com/fauletto/100-days-of-code/blob/master/Day005-UpdatedEnemyScript),
[Updated Player Script](https://github.com/fauletto/100-days-of-code/blob/master/Day005-UpdatedPlayerScript)

### Day 6: January 6th, 2018.

**Today's Progress**: Another productive day today! I continued to work on my space shooter game, Star Swarm with minimal assistance from the Udemy videos. I used a lot of resources on Google to answer some of the questions I had. Today I created two new systems within my game: a working Leaderboard, which keeps track of the top 10 scores in the game; and an updated music player, which plays a different audio track for each loaded level. 

I did encounter a problem while coding today, but I didn't give up and actually came up with a solution! Here was my issue: I was attempting to create a method that caused the player's space ship to explode when its health reached 0 points. Easy enough. I then wanted the ship sprite to disappear, play a sound, and load the "Game Over" scene. Not so easy. I realized (after more time than I would like to admit), that because the object with the sound file (the space ship) was being destroyed, so too was the audio clip. I eventually created a method and attached it to another game object that constantly checks to see if the player's health is <=0. If that is detected, this separate game object would play the death sound and load the next level, allowing the ship sprite to disappear without affecting the sound or level load.

I definitely was battling some frustrating during that experience, but finding the solution *with no help at all* was really satisfying. 

**Thoughts:** Similar to the progress I made yesterday, I am very pleased that I was able to do some of the (minor) things I did with minimal assistance. I hit a bit of a snag while working on some systems and got a bit frustrated. I didn't give up, however, and managed to find a solution, which felt awesome. 

**Link to work:** [Leaderboard Script](https://github.com/fauletto/100-days-of-code/blob/master/Day006-LeaderboardScript),
[Music Script](https://github.com/fauletto/100-days-of-code/blob/master/Day006-MusicScript)

### Day 7: January 7th, 2018.

**Today's Progress**: I encountered a few issues today, but overall made some good progress and learned a few new things along the way.

I started my morning with a delivery from Amazon; it was the copy of [C# in Depth by Jon Skeet](https://www.manning.com/books/c-sharp-in-depth-third-edition) I ordered! So, I started my morning by reading some of that with a cup of coffee. I feel like I'm going to get a lot out of this book!

When it came time to code, I decided I was going to put the finishing touches on my Unity space shooter, Star Swarm. Last night, I was having some issues getting the leaderboard to display the player's name after putting it in the input field in the game. After a few hours (yes, it took hours), I managed to figure out the solution. I completely scrapped my old leaderboard system, and wrote a brand new one today.

Then, more frustration hit. I was repeatedly getting the following error when I attempted to load scores: **"NullReferenceException: Object reference not set to an instance of an object."** Uh-oh. I had no idea how to fix this, I Googled and searched the Unity docs, but still came up with nothing. Then, it dawned on me: the text box for the score was not referencing the score from the ScoreKeeper script I wrote. Once I declared a public score GameObject from my ScoreKeeper script, everything worked!

So, while it may seem like I made minimal progress today, I actually felt like those bits of progress were huge. Tomorrow I will continue to read my new book (so excited) and work on my personal RPG.

**Thoughts:** I definitely made some small steps today, but they felt like giant leaps. I solved *two* major problems in my scripts and completely re-wrote my leaderboard script to ensure everything was working as intended. Today was a frustrating day for sure; I spent a few hours to fix these errors, but it was worth it in the end, as my short little game is complete!

**Link to work:** [New Leaderboard Script](https://github.com/fauletto/100-days-of-code/blob/master/R1-Daily-Repos/Day007-NewLeaderboardScript),
[Updated ScoreDisplay Script](https://github.com/fauletto/100-days-of-code/blob/master/R1-Daily-Repos/Day007-UpdatedScoreDisplayScript),
[Updated ScoreKeeper Script](https://github.com/fauletto/100-days-of-code/blob/master/R1-Daily-Repos/Day007-UpdatedScoreKeeperScript),
[Star Swarm Game!](https://gamebucket.io/game/ef3e1222-2d86-4c6a-89e3-4db5b18d0bab)
