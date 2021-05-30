# Atari Platform Study- Adventure

## Ruby Ostrow
## Games Systems
## Spring 2021

  *Adventure* is an Atari 2600 video game released in 1980 and created by Warren Robinett. It was the first action-adventure game, most games up until this point having been confined to a single screen and lacking *Adventure*’s quality of explorations (“Adventure (1980 Video Game),” 2021). This game was a massive step for the Atari console, as it greatly stretched the expectations of what the device was capable of given its minimal memory capacity. It was considered such a leap that, when Robinett initially presented his idea for *Adventure*, he was told that it wasn’t possible and there was no point in even attempting it, leading him to begin the project in secret (Robinett 2015). *Adventure* was also a great step forward just in the conception of what video games could be: it showed how a video game could create a whole world and be centered around exploring it (Robinett 2015). While there is an objective in *Adventure,* it is not simply about defeating enemies as they come into your vicinity.  Rather, as one goes through the game and aims for one’s goal, the focus is on encountering and overcoming obstacles. In this way, it helped establish the foundation that has launched many of today’s classic video games with their expansive worlds and the total simulation the player can find within them—the experience of entering a kind of self-contained universe.
  
   Let us take a step back and look at the basic story of *Adventure.* The player plays as the hero on a quest to recover the Enchanted Chalice which has been stolen by an evil magician (“Adventure (1980 Video Game),” 2021). The kingdom in which the chalice has been hidden within is guarded by three fearsome dragons- Yorgle, Grundle, and Rhindle- which all seek to eat the hero and end his journey. There is also a bat that appears in higher levels of the game that flies throughout the rooms and can pick up objects and move them about. It is uninterested in the hero but can cause trouble by stealing necessary objects from the player. In addition to the chalice and these obstacles, there are a few other objects in the game- keys to open the castles, a magic bridge to get across walls, a magnet to pull objects towards the player, and a sword that can be used to kill the dragons- which will help the hero on his quest. The game is completed when the player returns the Enchanted Chalice to the yellow castle. You may also play the game at three different levels, increasing in difficulty. 
   
   With the basis of the game established, let us return to what led to its creation. The creator, Warren Robinett, was a young game developer at Atari, having just created his first game, Slot Racers. In pursuit of an idea for his next game, he discovered the text-based adventure game Colossal Cave Adventure, which was created by Willie Crowther and Don Woods between 1975-1977 for the PDP-10 mainframe (“Colossal Cave Adventure,” 2021). This game laid out a journey through a series of caves through which the player could traverse, exploring and picking up objects as she went. Everything was described with text and the player could pick their actions by one to two word text commands. Robinett was very interested in the concept and wanted to build on it through the transformation into the visual setting of video games. From the start, though, space was a massive issue: *Colossal Cave* used hundreds of kilobytes of ROM and the Atari 2600 only had 4K (Baker 2015). For this reason, Robinett was told to not even begin the project, as his boss thought this an insurmountable feat that simply would not be possible with this console. Robinett was not convinced, though, and, believing he had a way to make it work, began to work on a prototype in secret. He accomplished his task in one month, getting past the space issue (and even having 15KB left over!) with “a good data structure” and “efficient coding” (Robinett 2015). Still, this primarily gave proof that the game was possible rather than being much fun in and of itself. When presented with his prototype, his bosses, while being convinced of the feasibility of the project, still weren’t on board with his main idea and attempted to push him into making it a tie-in with the latest Superman movie. He was undeterred though, saying later on in an interview, “Sometimes you have to fight for your ideas” (Baker 2015). 
   
   When Robinett created this game, he seems to have had a sense that he was creating something special and rather groundbreaking, both with this new type of game and of course with all the obstacles he overcame in getting it created. He thus understandably wanted credit for this work and to have people know that this was a game created by Warren Robinett. And yet as a game developer at Atari at this time, that wasn’t allowed. The company had a policy of anonymity for the creators, fearing if they grew too confident that they would begin asking for more (higher pay, royalties, fair working conditions, etc.). Instead, Atari decided to treat its workers as “replaceable cogs in a machine” essentially, giving them no credit for their work and continually reinforcing the idea that every worker was replaceable (Robinett, interviewed by Seth Porges, 2017). Robinett cites this lack of recognition and fair treatment as a big factor in Atari’s downfall in the 1980s, given that it led to all the game designers quitting and their replacements proving that the talents of these people were indeed unique and not easily replicated (Robinett, interviewed by Seth Porges, 2017). But Robinett was not ready to allow himself to go unrecognized for *Adventure*. So he proceeded to utilize the same secretive tactics with which he managed to get the game created in the first place: he created a secret room with the words “CREATED BY WARREN ROBINETT” in it and didn’t tell anyone what he had done until the game was in stores around the world. He had to make it very difficult to access so that the game testers wouldn’t find it but not so difficult that it would never be found, though he had a backup plan to start the rumor of its existence and how to get to it himself if no kid found it naturally (which they in fact did). In this way, he created the first Easter Egg in a video game, spawning many, many more in games as the years went by-- so much so that it’s now basically an expectation that video games will have these secrets somewhere within if you’re clever enough to find them. Interestingly, though, he notes that, in creating this secret room, he didn’t think this was something that would catch on as a general idea. Rather, he says, “I just thought, ‘I'm going to trick these bastards and sneak my name into the game and I'm not going to tell anybody and they're going to manufacture 100,000 units of Adventure and they're going to ship them all over the world and kids are going to get them out of the boxes and there will be no way that Warner Communications can undo that maneuver’” (Robinett, interviewed by Seth Porges, 2017). In this way, Warren Robinett influenced the future of the video game world all with a square dot that moves through rooms of different colors and “Duck Dragons” (Baker 2015). 
   
   Delving into the code itself of *Adventure*, even with the crude graphics and general simplicity (at least considering what we now associate with a world-exploration video game), I still found myself rather daunted due to the tightness of what Robinett created. The game has a very clear idea and it was rather difficult to consider how precisely it would be interesting to tweak the code. So I began by simply adjusting some of the graphics I found most displeasing, beginning with the opening screen which shows a purple outline of a square with a small, green number in the middle denoting which level you had the game set to (1, 2, or 3). I began by adjusting the graphics of the shape of the room, lowering some of the byte values so that, rather than a solid edge of color, there were various holes in it which added more visual interest.
        

    ;Number Room Definition
    NumberRoom:
           .byte $F0,$00,$FF          ;XXXX        XXXXXXXXRRRRRRRR        RRRR
           .byte $00,$00,$00          ;
           .byte $30,$00,$00          ;XX                                    RR
           .byte $00,$00,$00          ;
           .byte $30,$00,$00          ;XX                                    RR
           .byte $00,$00,$00          ;
           .byte $F0,$00,$0F          ;XXXX        XXXX        RRRR        RRRR

I changed the first and last line to have a byte value of $00 in the middle rather than $FF. On lines 4, 5, and 8 I changed the first value from $30 to $00.

After this change, I proceeded to change the color of the room from purple to blue ($86) and the color of the number from green to flashing ($CB) in the Room Data Table and Object Data Table respectively. 

    LFE1B: .byte <NumberRoom,>NumberRoom,                $86,$0A,$21,$00,$00,$00,$00  
    ;00 'Number Room.       


    LFF71: .byte <NumberInfo,>NumberInfo, $DD,$00, <NumberStates,>NumberStates,$CB,$00,$00 ;#5 Number  

After this change, when playing through the game again, I noted a detail that I had forgotten to take into account with what I thought would be a very simple change: the Number Room definition is used to define more than just the opening screen. With the addition of the new passages through the walls, rooms that were previously enclosed now could be traveled through to get to their adjacent rooms (as defined in the data table by the links held in offsets 5 through 8). This led to some interesting looping, where I could exit out the right side of the room and enter back in from the left side (if the links referred back to the current room) or appear in a whole different part of the kingdom altogether. I quite enjoyed the disorienting and frustrating situation this created where you could either stumble across a shortcut that would bring you much closer to the chalice and bypass various obstacles but also could lead to you accidentally ending up back where you started when you were nearly at the goal. The game already has some mazes created by rooms throughout it but this seemed to be an interesting way to make the whole game feel labyrinthian, making it difficult to grasp which path to take at each turn until you memorized the pattern. 

So with the intent to continue with this objective, I proceeded to alter the graphics of the Castle Definition and the Top Entry Room (the changed values are designated by highlights). 


    ;Top Entry Room
    TopEntryRoom:
           .byte $F0,$FF,$0F          ;XXXXXXXXXXXXXXXX        RRRRRRRRRRRRRRRR
           .byte $30,$00,$00          ;XX                                    RR
           .byte $30,$00,$00          ;XX                                    RR
           .byte $30,$00,$00          ;XX                                    RR
           .byte $30,$00,$00          ;XX                                    RR
           .byte $30,$00,$00          ;XX                                    RR
           .byte $F0,$F0,$0F          ;XXXXXXXX    XXXX        RRRR    RRRRRRRR
    


    ;Castle Definition
    CastleDef:
           .byte $F0,$FE,$15          ;XXXXXXXXXXX X X X      R R R RRRRRRRRRRR
           .byte $30,$03,$1F          ;XX        XXXXXXX      RRRRRRR        RR
           .byte $30,$03,$FF          ;XX        XXXXXXXXXXRRRRRRRRRR        RR
           .byte $00,$00,$FF          ;            XXXXXXXXRRRRRRRR          
           .byte $30,$00,$3F          ;XX          XXXXXX    RRRRRR          RR
           .byte $30,$00,$00          ;XX                                    RR
           .byte $F0,$FF,$0F          ;XXXXXXXXXXXXXX            RRRRRRRRRRRRRR

I made similar changes to these rooms as I did to the Number Room, lowering byte values where I wanted to create new passages.  

Once I had made these graphics changes, I focused on changing links between the rooms, resulting in changing the geography of the game. Utilizing the new passages (and some pre-existing ones), I changed how you travel through the game, creating a more disorienting environment.  I will now go through where these new links lead you (again highlights designate which values have been changed).


    LFE3F: .byte <BlueMazeTop,>BlueMazeTop,              $AC,$0A,$21,$10,$05,$07,$12      ;04; Top of Blue Maze

If you exit on the left of the top of the blue maze, you now end up in the yellow castle entry (offset 8, $12).
 

     LFEAB: .byte <CastleDef,>CastleDef,                  $00,$02,$21,$01,$0C,$04,$01      ;10; Black Castle

If you exit right,  you will be trapped in the side corridor ($0C), unable to move on. If you exit left, you will find yourself in a room previously inaccesible in level 1 ($01), right near the chalice.


    LFEB4: .byte <CastleDef,>CastleDef,                  $1A,$0A,$21,$06,$02,$06,$10      ;11; Yellow Castle

If you exit left, you will end up in the black castle ($10). If you exit right, you will end up in the corridor previously below the yellow castle (and still above it as the yellow castle is accessible up from the corridor). If you exit downwards, you will appear in the bottom of the blue maze.


    LFEBD: .byte <NumberRoom,>NumberRoom,                $1A,$0A,$21,$1D,$07,$12,$11      ;12; Yellow Castle Entry 

If you exit right, you will end up in the middle of the blue maze ($07). If you exit left, you will arrive in the black castle. If you exit upwards, you will come into the top entry room ($1D) and be faced with the green dragon. 


    LFF20: .byte <TopEntryRoom,>TopEntryRoom,            $36,$0A,$21,$8F,$01,$11,$03      ;1D; (Top Entry Room) 

If you exit downwards, you will be trapped above the yellow castle.

I focused on these rooms in particular because they appeared to be many of the main rooms and I thought it more interesting to change those than rooms that only appeared in one level. Secondly, rooms such as the invisible maze (and the levels that contain those rooms) already seemed to have that element of disorientation present. I feel that I accomplished my goal of hacking the game to have more a sense of disorientation and a general, labyrinthian quality. If I were to continue with this hack, though, I would likely be interested in delving into how to change more of the other rooms as well and add to the interconnectedness I have created and embellished here. 







Sources
“Adventure (1980 Video Game),” *Wikipedia*, 2021.
Baker, Chris. “How One Man Invented the Console Adventure Game,” *Wired*, 2015.
“Colossal Cave Adventure,” *Wikipedia*, 2021.
Porges, Seth. “The True Story behind the Original Video Game ‘Easter Egg’ that Inspired ‘Ready Player One,’” *Forbes*, 2017.
Robinett, Warren. “Design of *Adventure* for the Atari 2600: The First Action-Adventure Game,” 2015.
Robinett, Warren. “Design of *Adventure* for the Atari 2600: The First Action-Adventure Game,” Game Developers Conference, March 2-6, 2015, San Francisco, CA, Conference Presentation.

