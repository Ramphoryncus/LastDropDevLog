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
I was assigned the task of creating a fan which would affect the player by means of wind or add force. It took me a little while to get going admittedly but I constructed a fan in Maya and used a simple add force node with collision box. At first I tried to use the directional wind source that I had seen in a YouTube video but you need the mega scans of foliage in the project at the start to be able to reference the directional wind source in a separate blueprint. It was a simple blueprint I was only asked to add a fan with no activate or deactivate mechanics on it although I wanted to I wasn't asked to do anything other than add a fan. But I did do some sound recordings of various fans that I have around my home to create an audio loop for the sound of the fan which I altered using Audacity and I added the file to the project I also made a Sound Attenuator to partner with the fan sound file. I informed David Didu, one of our two audio programmers, that I had created an audio file for the fan sound and ultimately emailed him the original file from audacity and the.WAV so he had access to both for the project. I did this so he had access to it whether it made into the project or not, as there was some issues going on with GitHub or at least going on with me, and I was having some issues with the fan sound coming out of my speakers but not my headphones and I could not figure it out but maybe David could.

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

Short OBS recording of Fan Sound frim raw to all effects used
https://github.com/user-attachments/assets/25e75ec4-55f4-40f8-92b3-34c82dfc9cf9


