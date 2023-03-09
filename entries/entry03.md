# Entry 3 - My Plan Into Motion
##### 2/8/23

### Catch up
So first off, if it wasn't stated before, I'll state it again. I am creating a game platformer game using the Python coding library PyGame. I am working on creating a shooter with weapon mechanics and all that sort of good stuff. Currently, the only thing that I've done so far was a create a title screen menu 

### How was it done?

Well it'd be too much because I'd need to (would most likely) explain every single part. So instead of that, I just made an example how such process would be executed. Here's a basic process for making a menu using Pygame:

1. Import Pygame and initialize it ```py with pygame.init() ```.
2. Then create a Pygame window with ```py pygame.display.set_mode() ``` and set your wanted dimensions of the window.
3. Create a font object with ```py pygame.font.Font() ``` and set the font type and size that you want (Custom fonts are possible).
4. Create a text object with the font object and the text that you want to display. (Basically make a class for the sub-section that you'd want; play, options, credits, etc)
5. Create a rectangle object with ```py text.get_rect() ``` to get the dimensions of the text object. (Give your button a shape)
6. Set the position of the text object with ```py text_rect.center = (x, y) ``` to center the text object in the window.
7. Draw the text object onto the window with ```py pygame.draw.rect() ``` and ```py pygame.blit() ```. (To make the object/button appear in the created window on your screen)
8. Use ```py pygame.display.update() ```to update the display. (So after all the code is written, it'll follow through with what you wanted)

Here's a sample code that creates a menu with two options:

```py
import pygame

pygame.init()

# Set the dimensions of the window
WINDOW_WIDTH = 800
WINDOW_HEIGHT = 600
screen = pygame.display.set_mode((WINDOW_WIDTH, WINDOW_HEIGHT))

# Set the font type and size
font = pygame.font.Font(None, 36)

# Create text objects for each menu option
text_option_1 = font.render("Option 1", True, (255, 255, 255))
text_option_2 = font.render("Option 2", True, (255, 255, 255))

# Get the dimensions of each text object
text_option_1_rect = text_option_1.get_rect()
text_option_2_rect = text_option_2.get_rect()

# Center the text objects in the window
text_option_1_rect.center = (WINDOW_WIDTH // 2, WINDOW_HEIGHT // 2 - 50)
text_option_2_rect.center = (WINDOW_WIDTH // 2, WINDOW_HEIGHT // 2 + 50)

# Draw the text objects onto the window
screen.blit(text_option_1, text_option_1_rect)
screen.blit(text_option_2, text_option_2_rect)

# Update the display
pygame.display.update()

# Game loop
while True:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            quit()
```
This code creates a window, sets the font type and size, creates two text objects for the menu options, centers them in the window, draws them onto the window, and updates the display. The game loop at the end of the code listens for the 'QUIT' event (the user closing the window) and quits the Pygame application.

### Next Steps, MVP and Beyond!

My next steps are to create the actual game levels, aswell as a level selector. Which is in the middle of my MVP and Byond MVP at the moment. Speaking of beyond MVP, my plans are:

- Make a character that moves and interact with the environment
- Make AI enemies
  - Walk/Run
  - Attack players
- Levels/Worlds

Beyond MVP:

Beyond MVP
- Make a working menu screen 
  - A base menu (play, options, credits, etc)
    - Create a level selector
- Random level generator
- Online/Local Multiplayer



[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
