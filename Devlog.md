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
