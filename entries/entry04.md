# Entry 4
##### 3/27/23

## What I've Done

So far in the process of creating my game, I've completed each of the following:
- Creating the player
- Keyboard inputs
- Sprite animation
- Weapons and effects

These are what I've worked on so far and now I'm going to explain a bit of what was done for each portion. So now let us dive a bit into the process of each part. 

### Creating the Player

#### Movement

![image](https://user-images.githubusercontent.com/73478976/235146170-efdb0b69-417f-4dc2-9fcb-4a8be991725c.png)
![image](https://user-images.githubusercontent.com/73478976/235147065-949694b7-6132-49c6-9795-0a4feab1221e.png)
<br>Here is where we define our variables for the display size and set the movement, shooting, and grenade vals. They're set to false as so the character isn't moving on it's on own. You can see that the framerate is 60, that is in order for the movement to be much slower and not run off the screen at a fast rate
<br>
<br> ![image](https://user-images.githubusercontent.com/73478976/235206819-d7350a43-6264-41eb-ad02-b949803f7c86.png)
<br> The following is in order to check for if there is a keypress, and when a key is pressed. Delta y and x change based on which one going by the xy chart. Ok, that's finished and now there is movement, but there also is an issue...

![image](https://user-images.githubusercontent.com/73478976/235208646-4ed22744-67a3-4e8c-ab8c-5023fba66f20.png)
<br> The sprite is constantly drawn. So we need to keep refreshing the background while maintaining the soldier being drawn
<br> ![image](https://user-images.githubusercontent.com/73478976/235208013-39bb208e-c1e6-4131-a7ea-b0671b0278d9.png)
<br> ![image](https://user-images.githubusercontent.com/73478976/235208172-ea28d97d-c79d-426f-b77e-aef9f0231a76.png)
<br> So we'll write a class that can draw a background, but for it to constantly draw and overide any trail. SO it'll need to be in the while loop for that to happen. Resulting in this: [Video result](https://user-images.githubusercontent.com/73478976/235211173-495dc00d-ae80-42d4-b961-7f004d97dfba.webm)
<br>![image](https://user-images.githubusercontent.com/73478976/235210938-871bf77e-7d03-416b-94bd-8ac8bcf7e7e0.png)

#### Drawing/Animation
<br> You may be wondering how I actually drew the sprite on the canvas. At first it looked liek this:
<br> ![image](https://user-images.githubusercontent.com/73478976/235213213-bc439254-18b6-471c-822f-49ef25367438.png)
<br> But the it changed into this:
<br> ![image](https://user-images.githubusercontent.com/73478976/235230017-0db205e5-910e-4a60-93fc-7eb9222958da.png)
<br> It may look confusing, but in short. It takes all the images from each animation set (idle, death, etc.) and enters each list seperatel into a python list. Which allows me to have animation for my sprite as it'll iterate through each image in the selected animation type for when it is called. So when the characters hp hits 0 and the death animation is called, it'll go through every frame of that animation instead of one image like before. Also, in order to make sure that the image was down to the size I wished it to be, ``` pygame.transform.scale ``` was used to bring it down to size.
 



### Weapons (shooting)

![image](https://user-images.githubusercontent.com/73478976/235229218-6db3c251-5379-43c0-9dee-581770c5340c.png) <br> `positions bullet off the players hitbox(rect) when you shoot. That way it doesn't collide with the player and inflict self damage  `

![image](https://user-images.githubusercontent.com/73478976/235235349-b9849b6f-e74a-46dd-856a-3fc774b3c145.png) <br> `bullet properties`







<br> ![image](https://user-images.githubusercontent.com/73478976/235233273-c62c6e58-e9da-40a1-8c78-9069a6a06583.png)
<br> What allows this all to work is the event handler, which job is to be a trigger. In this instance, keypresses for where it'll change the variable as to what I assigned it to watch for.
<br> ![image](https://user-images.githubusercontent.com/73478976/235234098-1a82bf90-32e9-447b-a40e-1a3db56cdf7e.png)
<br> Like wise for when the button has been released. It'll revert the variable back to it's base state



[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
