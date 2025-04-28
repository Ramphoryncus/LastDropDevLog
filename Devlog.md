# **_Last Drop Development Log_**
## **_by Henry Taylor 2206046_**
---
### Week 1 - 3
I was assigned the role of QA. My first task was to play through the initial level that we received in the last drop project of the unknown facility and find any issues. There were a couple of things that I found:
1. The BP_Activatable_Platform when it collided with the player the player popped out on top of the platform which is kind of fourth wall breaker.
2. There was a minor issue with a box where the player could get stuck between the BP_MovingPlatform and the offending box.

For the BP_Activatable_Platform I added a collision box and used the On Component Begin Overlap event to activate a respawn at a billboard this is a temporary measure and could be used by anyone in conjunction with the checkpoint system that I knew was going to be created.
https://blueprintue.com/blueprint/0ecqbirs/

![PlayerDeathRespawnTest](https://github.com/user-attachments/assets/40c82303-6f5e-4792-a284-4a3c602b3f66)

For the offending box I reduced it in size and moved the larger cube next to it over slightly so the player would not get trapped between either of these cubes and the BP_MovingPlatform.

![OffendingBox](https://github.com/user-attachments/assets/f76ecb75-f46c-45dc-a9f2-935c4e646cc7)

I ended up having to do these again in week two and week three because there were some issues with the project.

We were told to read the Game Design Document compiled by the Game Design students, so I read it in full. They came up with a lot of ideas and mechanics. I had a discussion with Ethan, one of the games design project coordinators, about streamlining all of these ideas picking one mechanic for each level and choosing the most achievable mechanics that they came up with for us, as developers, to work on.

---
### Week 3 - 4
I was partnered with Sidd Ghosalkar to assist him with a water bubble mechanic where the bubble grows in size as it takes on water. Sidd did all of the blueprinting but there was one issue where the bubble was not increasing in size. I had a quick look at the blueprint and he had a check bubble size with a greater than ( > ) node I suggested it should be greater than or equal to ( >= ) and it appeared to fix the problem that he was experiencing. Unfortunately I do not have any evidence of this blueprint and it is no longer in or being used in the project. I did not take a screenshot of it at the time to support this.

I was asked to test the SAP bubble boost jump mechanic and the level that it would be used in, which was Spring, by Ihor our project coordinator. I spoke directly with Esme who I was told was responsible for the spring level and asked her to inform me when it was ready to be tested... I received no notification of its state of readiness and therefore could not test the level at that point.

### Week 4 - 6
I was assigned the task of creating a fan which would affect the player/bubble with wind, I ended up using add force and could only get it to effect the bubble as when I checked Simulate Physics on the BP_BodyChar for the AddForce to have an effect you could not move the Player Character. What I did not think of but someone else did was changing Gravity in the collision box...hopefully I will remember this for the next time I need to do something similar. It took me a little while to get going admittedly but I constructed a fan in Maya and used a simple add force node with collision box. At first I tried to use the directional wind source that I had seen in a YouTube video but you need the mega scans of foliage in the project at the start to be able to reference the directional wind source in a separate blueprint. It was a simple blueprint as I was only asked to add a fan with no activate or deactivate mechanics on it with the BubblePop, although I wanted to, I wasn't asked to do anything other than add a fan with "wind". But I did do some sound recordings of various fans that I have around my home to create an audio loop for the sound of the fan, which I altered using Audacity. I added the file to the project with a Sound Attenuator to partner with the fan sound file. I informed David Didu, one of our two audio programmers, that I had created an audio file for the fan sound and ultimately emailed him the original file from audacity and the.WAV so he had access to both for the project. I did this so he had access to it whether it made into the project or not, as there was some issues going on with GitHub or at least going on with me, and I was having some issues with the fan sound coming out of my speakers but not my headphones and I could not figure it out but maybe David could.

This is my working blueprint
https://blueprintue.com/blueprint/wd3lzvnr/

This is the unfinished blueprint trying to call the wind directional source which I later realised I needed the mega scans foliage in the project which we did not have.
https://blueprintue.com/blueprint/31rdc27t/

Low Poly Fan
![LowPolyFan](https://github.com/user-attachments/assets/ce2623e9-27ee-4189-815d-db0f31b6c87a)

High Poly Fan
![HighPolyFan](https://github.com/user-attachments/assets/94b52111-88f4-41e8-9022-0151fb9a7858)

Fan and Cowling
![FanCowling](https://github.com/user-attachments/assets/0cb7b2d0-0e4e-4941-a7a3-fdb2f53d6c53)

Final Fan and Cowling because I did not make the Cowling a 2 sided mesh
![FullFanCowling](https://github.com/user-attachments/assets/18a3cdc1-4a97-4058-9bfc-e728db8ea5e5)

Fan Texture and UV
![TexturedFan](https://github.com/user-attachments/assets/8c3a2aaf-55fc-4232-b87b-1cc2a337ddf7)
![TexturedFanUV](https://github.com/user-attachments/assets/09c0986d-70b9-4e7f-b2e6-bd653b49c26d)

Cowling Texture and UV
![TexturedCowling](https://github.com/user-attachments/assets/f96c02fe-dc70-4e71-bb41-24c52ca1c71a)
![TexturedCowlingUV](https://github.com/user-attachments/assets/50b02938-dec4-4b69-a393-71773bfcd119)

Fan Sound audio file screen shot from Audacity
![FanSoundAudacity](https://github.com/user-attachments/assets/13d4096e-057c-41e8-8ca3-440660665187)

Short OBS recording of Fan Sound from raw to all effects used

https://github.com/user-attachments/assets/25e75ec4-55f4-40f8-92b3-34c82dfc9cf9

I recorded myself blowing onto a reasonably sized pedestal fan. I slowed the tempo from 42 down to 21 and added the phaser, compressor, wah wah and reverb effects with some slight adjustments to their settings to achieve the final sound.

### Week 7 - 9
I kind of went off the reservation from week 7 to 9. I really didn't feel like being there and none of the levels had been uploaded to the main file of the GitHub repository. However they were uploaded during the scheduled lecture of week nine. This was quite disheartening.

### Week 9 - 12
My first discovery was that the mouse cursor was disappearing when the bubble burst through either, exceeding the distance/lifespan limit, or being popped by the player using right click on the mouse. This is not optimal when you are using a mouse to control a part of your player character so I added a couple of show mouse cursor nodes.

One in the BP_BubbleChar
https://blueprintue.com/blueprint/kllwghcl/

One in the BP_BodyChar
https://blueprintue.com/blueprint/sxj-b_j7/

The mouse cursor is on the screen at all times. I had considered creating a custom icon/widget for the mouse cursor but that was not vitally important, seeing the mouse cursor was, so I fixed it.

I started playing through the levels. Spring was my first stop. 

### Spring
There were no checkpoints, no kill boxes, issues with layouts where the player couldn't progress through the level. I corresponded with Dylan and Esme informing them of my findings and the changes that I thought should made to the level, because I did not want to make too many necessary but drastic changes to their creation. Concerning checkpoints and kill boxes, somebody did put a kill box with a checkpoint in so I duplicated that with reasonably situated corresponding checkpoints so the player didn't have to keep going back to redo part of the level where they've already been. I lowered the height of the switch used to activate BP_HitButtonPlat as it was too high for the player to reach even with the SAP boosted jump.

I discussed with Dylan the jumping platforms which the player could not reach boosted jump or not. I suggested that he remove the lower jumping platform, lower the static platform above it so the player could jump to it with the boosted jump and make the higher moving platforms possible for the player to jump on them without using the boosted jump because they would be too far away from the SAP dispenser to then give themselves another boosted jump to reach these platforms which would not be reachable otherwise. He did not do that. As far as I can figure he adjusted the length of time that the SAP boost jump remains effective for the player so the they can make their way past these jumping platforms with one SAP drop, have to be quick though. Dylan adjusted the moving platforms but the lowest moving platform had to be raised slightly because the player would not be able to make the jump from it to the static platform. Before he made these changes, however, I did add a chackpoint and SAP dispenser at the final part of the level with the moving platforms so the player could reach the switches to activate the moving platforms. These have subsequently been removed or did not get pushed properly to GitHub, not sure, but at least I took a screenshot of it this time. I made some minor adjustments to the already existing SAP dispenser just shrunk it down a little and added all the rest of the meshes and Sap Decal, to match the other SAP dispensers earlier in the level for continuity.

![SapDispenserSpring](https://github.com/user-attachments/assets/53922fea-9c54-418f-8539-737f073641dc)

I did also discovered that the start/end points for the jumping platforms and the end platforms had collisions turned on, which the player could jump upon so I set the collisions to Custom and Ignore All so the player can't jump on these Hidden in Game meshes.

Screenshot taken after Cube mesh/Collision fix.

![SpringEndPlatforms](https://github.com/user-attachments/assets/f41d196a-7e90-4ba8-8b56-d9a8d38b2513)


It was at this point that I discovered a fatal flaw with all of the levels, somehow either Unreal Engine or someone had offset the mesh of a cube or cubes corresponding to their collision volumes. This meant that the player would not be able to proceed through any of the sliding doors or properly pickup pickups and would collide with things that they can't see because the collision volumes were sticking out of everywhere. I posted a message in discord and Jakub responded saying that I would have to reset the pivot points in Modelling on the cube mesh, this was not the case however, I had to reposition the mesh so that it lined up witht the collision volume. Thankfully when I fixed one, it fixed them all.

![OffsetCollision](https://github.com/user-attachments/assets/35ab1135-bc09-4044-9791-6435261497f7)

One cube to rule them all. One cube to find them. One cube to bring them all, and in the darkness bind them... my precious.

### Winter
There are a few issues I found with the winter level. There were not enough checkpoints in my opinion so I added a few extra ones, either they didn't get pushed properly or they got removed. There was an issue with the ice bubble coming out of the pipes where there would have been an infinite drop, through a kill box that did not register the ice bubble. I did make Ethan aware of this, which he subsequently fixed. There was a jump to a moving platform (BP_ActivatableMoving), above the choppers, crushers and conveyor belts that was activated when you are an ice bubble that you either made or didn't as BP_BodyChar with no killbox and no way back, it was on the very limit of the player jump distance so I adjusted the distance so that there was no drop. This was adjusted again after I made that adjustment and a kill box was added, with a checkpoint that puts you back to having to do all the ice bubble choppers, crushers and conveyor belts again. Not how I had it, I probably put a checkpoint there but I can't remember. If I did it's gone now.

### Summer
Between 1000 and 3000+ lights needed to be rebuilt on this level not sure why that was but some of the areas were very dark and obviously missing lighting or just needed to be rebuilt. I did add one rectangular light, maybe I should have added more.

![SummerLight](https://github.com/user-attachments/assets/c8eab7ef-2afe-41b3-8b76-4b6756ac4e93)

It is awfully dark in the Summer level.

I did add a few extra checkpoints in the summer level, I think there are all there but some of them were moved or just errors in the push to GitHub. For instance this one, I had originally placed it at the curved pipe on the right, now it appears at the sliding door on the far left. I did not see the need for the player to walk all the way along those pipes, again, especially after they would have fallen down through the gaps of the cogs/platform that followed, which were not lit at all, and that is why I put that rectangular light there.

![SummerMovedCheckpoint](https://github.com/user-attachments/assets/ff802e48-3129-40a0-a8c3-ad4d45284251)

I encountered a few irregularly scaled fans, I adjusted them to a uniform scale, because when they were spinning they did make me feel a little ill. They didn't look right it. The BP_WindTurbineCharacter meshes were also irregular they got the same treatment.

Irregular Fan
![IrregularFan](https://github.com/user-attachments/assets/d28e1a4b-1565-4a34-b6bc-1ec9013607e6)

Uniform Fan

![UniformFan](https://github.com/user-attachments/assets/1a00efb5-8f16-48ad-9214-7c30d20fdf9a)

Concerning the BP_WindTurbineCharacter when activated they were not rotating continuously, it took me a little while to figure it out, in the end I adjusted the Timeline so it was a constant 1 and Looping. It didn't matter that they had a Timeline where it started from zero and then rotated to a full speed because they are never seen by the player when they start rotating. This was an easy fix to the problem, rather than trying to figure out how to make it work properly via other means as in completely redoing the blueprint which was unnecessary. I did try a few different methods that did not work before this final solution. It was here that I found out about changing Gravity in the collision volume from my original fan, which had Add Force. To be honest I do not know if I would have thought of adjusting Gravity as an alternative. I probably would have kept plugging away at Add Force and trying to figure out how to move the BP_BodyChar with physics being simulated on the collision capsule.

![WindTurbineTimeline](https://github.com/user-attachments/assets/7531f972-4ee5-48e4-916f-814fa45ed760)

Not my blueprint I just made the above alteration. 
https://blueprintue.com/blueprint/dk5haaaf/

It was at this point that I also added the fan sound in the hope that it would only play when the BP_WindTurbineCharacter were activated, that was not the case. I removed the play sound at location on the BP_wind turbine character but the fan sound persists and it has not even been assigned it's sound attenuator so it's basically like some kind of trance inducing hypnotic background music may be? That was not what I intended. I still can't hear it through my headphones only my speakers.

### Autumn
This one was a little bit of a shock, 45,237 lights needed to be rebuilt... Holy shhh!! Aside from that the lighting that I saw and the level seemed to be okay. There were a couple of issues that I found. I noticed that my Death/Respawn at billboard test blueprint had been reappropriated for the BP_Door. I only found this out when I walked into one of these BP_Doors and found myself teleported into the door unable to move and in a constant collision with it so I was never going to move. I had a look at the blueprint, low and behold, there it was with my comment box so I knew it was mine. I promptly disconnected the executor which solved that problem immediately. 

Disconnected Death

![OldDeathRespawnSurprise](https://github.com/user-attachments/assets/b0dd3eba-9438-4f23-9bdc-4212255718f2)

Cheeky Respawn Camel

![RespawnCamelBillboard](https://github.com/user-attachments/assets/e7bb9e7a-4026-45f6-ad9a-04c1e7ae8710)

I did leave the blueprint nodes in place and just in case whoever used it did want to use it properly at some point in the future. Removing the executor made no significant difference to that part of the level. There would have been an issue with a lack of pickups, If you drop the first one without activating the second switch in front of one of the BP_WindTurbines you were stranded. Fortunately this was fixed by someone else. I would have done the same, two extra cubes simple. If it had not been then the player would have been stuck there whether they were in a wall or not. Fun fact, this level has no checkpoints and you cannot die, but before the pickups issue was solved you could have been stuck at the BP_Doors and BP_WindTurbines forever.

Moving on to the lower part of the autumn level. It took me a little while to figure out what I needed to do to get the end BP_SlideDoor open before the riser with all the fans in it. Well I thought I figured about but when I tried an electrified bubble or a pickup touching the end door neither of them worked. I looked at the blueprint and it had an Activate/Deactivate event but there was nothing that I could see was going to activate or deactivate through trial and error nothing worked from what I could see. Figuring that the difficult to reach BP_Pickup was the intended "activator" I selected the cube mesh and checked Simulation Generates Hit Events and added a On Component Hit event to the BP_SlideDoor with Cast To BP_Pickup. You do have to kind of throw the pickup at it but it works...eventually.

https://blueprintue.com/blueprint/1un7vzal/

![FinalPickupFans](https://github.com/user-attachments/assets/882fc0e9-025f-4dab-be5c-84b24792239c)

