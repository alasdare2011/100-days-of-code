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

### Day 8: January 8th, 2018.

**Today's Progress**: Back to work today, so I didn't have 8+ hours to code today. Boo! I still was able to spend a little over two hours reading, learning, doing tutorials, and working on my own RPG in Unity. 

During my lunch break at work today, I continued reading [C# in Depth by Jon Skeet.](https://www.manning.com/books/c-sharp-in-depth-third-edition) What a phenomenal and in-depth (ugh, sorry) look at the C# language! Jon Skeet is a fantastic teacher and clearly loves the C# language.

When I finally settled in at home tonight (during a pretty awful ice storm outside), I started the C# training path on [Pluralsight.](https://app.pluralsight.com/paths/skill/csharp) Some of it has been a retread of what I learned in Bob Tabor's course on the Microsoft Virtual Academy, but I figure there's no such thing as too much information. 

After a few videos, I hopped back into Unity and Visual Studio to work on my as of now untitled sci-fi RPG. I created a script for items, inventory, and item slots within the inventory. Nothing too groundbreaking or exciting, but the scripts work within my Unity editor and some of the basic foundation work is coming together for the game. I am really trying to start building a lot of the underlying systems of the game before I start worrying about art and such. We'll see how it goes!

**Thoughts:** Overall happy with today's work. I didn't run into any issues, but I believe that is solely because I am working with some fairly simple scripts for now. Regardless, I'm always happy to make progress!

**Link to work:** [Inventory Script](https://github.com/fauletto/100-days-of-code/blob/master/R1-Daily-Repos/Day008-InventoryScript),
[Item Script](https://github.com/fauletto/100-days-of-code/blob/master/R1-Daily-Repos/Day008-ItemScript),
[ItemSlot Script](https://github.com/fauletto/100-days-of-code/blob/master/R1-Daily-Repos/Day008-ItemSlotScript)

### Day 9: January 9th, 2018.

**Today's Progress**: Another busy day today! I had a staff meeting after work, which cut down on my coding time this evening, but I still managed to get another two hours or so in! 

I continued reading [C# in Depth by Jon Skeet](https://www.manning.com/books/c-sharp-in-depth-third-edition) when I had breaks at work. I really am loving how detailed each section of this book is so far. 

Oh! I forgot to mention: to further immerse myself in all things code, I've been listening to coding podcasts during my commute each day. I started digging into the [CodeNewbie podcast](https://www.codenewbie.org/) and absolutely love the different perspectives I've heard so far. It's just another opportunity to learn more!

At home, I continued working through the C# learning path on [Pluralsight.](https://app.pluralsight.com/paths/skill/csharp) I decided to start with the fundamentals, just to cement that stuff into my brain. I really appreciate the attention to detail in each of these lessons. 

I jumped back into Unity and Visual Studio to continue working on some stuff for my RPG. It isn't much, but I took some old code and Google research to create a more succinct and tidy Music Manager for my game. I like this version over the one I used in my previous game, as it requires a lot less work from me, and it helps keep things from getting over complicated. Simplicity is a beautiful thing!

**Thoughts:** I didn't write a ton of scripts, but the one I did write will help to simplify music management in my game. I'm looking forward to adding some more systems to my game tomorrow. 

**Link to work:** [MusicManager Script](https://github.com/fauletto/100-days-of-code/commit/d847399edee6a89fc1c31be8ab3591b2b485c3cf)

### Day 10: January 10th, 2018.

**Today's Progress**: Hey, I hit the double-digit mark for days! I managed to squeeze in another few hours to work on code when I got home from work today! It feels like I'm starting to develop a pretty consistent schedule for coding/learning.  

To give a quick update on the "learning" portion of my day, I bounced back and forth between reading [C# in Depth by Jon Skeet](https://www.manning.com/books/c-sharp-in-depth-third-edition) and [Rob Miles' C# Yellow Book](http://www.csharpcourse.com/) when I became a bit overwhelmed by Skeet's explanations (which are fantastic, but still a bit over my head in some places). I managed to finish another module of the the C# learning path on [Pluralsight.](https://app.pluralsight.com/paths/skill/csharp), and listened to more of the [CodeNewbie podcast](https://www.codenewbie.org/) during both my commute and gym session today!

I began making a generic Player Prefs script for Unity that I can use across multiple games. For those unaware, Player Prefs in Unity literally just saves different preferences, such as volume, difficulty, etc. We'll see how it works when I finish it and actually use it in the future. I also improved a fade in script from a tutorial I did, cleaning up the code and simplifying it a bit!

**Thoughts:** More small progress today, but still progress. Looking forward to seeing how this Player Prefs script works when I have more time to work tomorrow and Friday. 

**Link to work:** [PlayerPrefsManager Script](https://github.com/fauletto/100-days-of-code/blob/master/R1-Daily-Repos/Day010-PlayerPrefsManagerScript), [FadeIn Script](https://github.com/fauletto/100-days-of-code/blob/master/R1-Daily-Repos/Day010-FadeInScript)

### Day 11: January 11th, 2018.

**Today's Progress**: Super busy day today, but I was able to get in an hour to update a script I wrote yesterday and create an options menu with a script in my game!

I am still taking some time to read both [C# in Depth by Jon Skeet](https://www.manning.com/books/c-sharp-in-depth-third-edition) and [Rob Miles' C# Yellow Book](http://www.csharpcourse.com/) each day. I also spent some more time listening to the [CodeNewbie podcast](https://www.codenewbie.org/).

Since I didn't have much time to code today, I made sure to dive right in and update the PlayerPrefsManager script I worked on yesterday. The script is now wired to accept and save volume, difficulty, and any unlocked levels! 

I also finished up an options menu, creating working volume and difficulty sliders, and a "defaults" button that is wired to return those values to their default settings. Not a lot of time to work today, but pretty productive nonetheless! 

**Thoughts:** I am pretty excited to get a few of these backbone systems in place in my game. I will hopefully have more time tomorrow to work on some things, because I really wanted to dig deeper and start developing a script that will control player movement. 

**Link to work:** [UpdatedPlayerPrefsManager Script](https://github.com/fauletto/100-days-of-code/blob/master/R1-Daily-Repos/Day011-UpdatedPlayerPrefsManagerScript), [OptionsController Script](https://github.com/fauletto/100-days-of-code/blob/master/R1-Daily-Repos/Day011-OptionsControllerScript)

### Day 12: January 12th, 2018.

**Today's Progress**: Another busy day today; I wasn't home much, but I still set aside my hour to code. 

A quick reminder that I'm still reading [C# in Depth by Jon Skeet](https://www.manning.com/books/c-sharp-in-depth-third-edition) and [Rob Miles' C# Yellow Book](http://www.csharpcourse.com/) each day. I also listened to an episode of [CodeNewbie podcast](https://www.codenewbie.org/) with Quincy Larson, which was pretty awesome to hear.

Today I simply made a third class for my untitled RPG project, then made a scene controller script to control the level flow in Unity. Not much to show for the day, but I got my coding in!

**Thoughts:** I didn't do anything "new" per se, but I did something and got some more practice in. Hopefully tomorrow I will have time to really tinker and try out some new things. 

**Link to work:** [Medic Script](https://github.com/fauletto/100-days-of-code/blob/master/R1-Daily-Repos/Day012-MedicScript), [SceneController Script](https://github.com/fauletto/100-days-of-code/blob/master/R1-Daily-Repos/Day012-SceneControllerScript)

### Day 13: January 13th, 2018.

**Today's Progress**: So, today I did something new and a little different: I started my first MOOC (massive open online course) through [edX](https://www.edx.org/). I specifically decided to begin [Harvard's CS50x course](https://www.edx.org/course/introduction-computer-science-harvardx-cs50x) to get a better understanding of computer science in general. I think this understanding will translate to better programming/coding overall. After just one lecture, I am absolutely in love with the way David J. Malan teaches; he's engaging, intelligent, and funny. Definitely recommend this for anyone who wants to get a better understanding of computer science or even just problem solving in general.  

I spent an hour watching the lecture, then went on to work this week's assignment for the course, which was to create either an animation, piece of art, or game in [Scratch](https://scratch.mit.edu/). I spent a few hours working, but I managed to come up with something pretty awful; however, it works! [Mario's Mushroom Madness](https://scratch.mit.edu/projects/197770621/)

**Thoughts:** Yikes, coding in Scratch was a little more difficult than I thought. I felt a little more restricted than I would in C#, so I couldn't quite do what I wanted. Tomorrow will be a busy day, but I hope to spend some time working in C# again. 

**Link to work:** [Mario's Mushroom Madness](https://scratch.mit.edu/projects/197770621/) 

### Day 14: January 14th, 2018.

**Today's Progress**: It was nice to get back into coding in C# today, rather than using Scratch...that was a nightmare yesterday! I went back to work on my untitled RPG today, but I've decided to make some changes to my plan (which I think is okay).

The biggest change to my plan is the overall flow of gameplay. I orignally intended to make a very standard turn-based RPG, with a standard overworld map. I have actually decided to change that to more of a tactical turn-based strategy/RPG, similar to the gameplay of Fire Emblem or Advance Wars. This will allow me to contain the gameplay a bit more, which I think will make it a little easier for me to complete.

With that said, I decided to start working on the enemies in the game. I read up a lot on using Scriptable Objects in Unity, and have decided that will be the most efficient way to handle enemies in the game. I created a very basic template for the information and elements that will be needed to create each enemy. I will eventually edit this, but I think it's a good start for now. 

**Thoughts:** Felt good to get back into using C# today. I have a lot of work to do if I want to make this game work, but fortunately I have all the time in the world to get it done. I am starting to feel a little overwhelmed with some things, so I think I need to get back to the basics and do more tutorials/lessons online. 

**Link to work:** [EnemyData Script](https://github.com/fauletto/100-days-of-code/blob/master/R1-Daily-Repos/Day014-EnemyDataScript) 

### Day 14: January 14th, 2018.

**Today's Progress**: I decided to continue to expand my knowledge of C# today, and worked through some coursework for one of the MOOCs I am taking. I ran through a few tutorial and videos, then did my first homework assignment. I had to simply create a console application that would accept and print student data. It isn't anything special, but it was nice to step back and work through some of the C# basics I need to solidify. 

After that, I worked through a few of the exercises on [freeCodeCamp](https://www.freecodecamp.org) to further my programming/coding knowledge. I really like this site and how it presents information, so I think I will spend a lot more time here. Maybe it isn't a great idea to combine this with all the C# I'm learning, but as I mentioned recently, I have been feeling like I hit a brick wall and really need to solidify my coding foundation. 

**Thoughts:** It was nice to work on something a little simpler to build my confidence today. My next assignment--which I plan to work through tomorrow--looks a little trickier, so we'll see how that goes!

**Link to work:** [Module1HW Script](https://github.com/fauletto/100-days-of-code/blob/master/R1-Daily-Repos/Day015-Module1HW) 
