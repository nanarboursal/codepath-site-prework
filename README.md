# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: **Nanar Boursalian**

Time spent: **5** hours spent in total

Link to project: https://glitch.com/edit/#!/codepath-intership-prework

## Required Functionality

The following **required** functionality is complete:

* [X] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [X] "Start" button toggles between "Start" and "Stop" when clicked. 
* [X] Game buttons each light up and play a sound when clicked. 
* [X] Computer plays back sequence of clues including sound and visual cue for each button
* [X] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [X] User wins the game after guessing a complete pattern
* [X] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [X] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [X] Buttons use a pitch (frequency) other than the ones in the tutorial
* [X] More than 4 functional game buttons
* [X] Playback speeds up on each turn
* [X] Computer picks a different pattern each time the game is played
* [ ] Player only loses after 3 mistakes (instead of on the first mistake)
* [X] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:
* [X] Fun Fact!: The chosen frequencies make it so playing the buttons in the following order will play the beginning of the Harry Potter theme song!
      
    1, 2, 3, 4, 2, 5, 6(hold), 4(hold), 2, 3, 4, 1, 2, 1(hold)

## Video Walkthrough

Here's a walkthrough of implemented user stories:
![](http://g.recordit.co/wxhsWux9p5.gif)


## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 

I used www.W3schools.com for color codes and img span tag properties! I also used Stack Overflow to help format my buttons!

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 

I had a lot of challenges with stopping the tone when pressing the buttons. Initially, the tone would stop when the user released the button, meaning that the functionality was working well. However, after implementing a couple of the optional features, I was stress testing the program when I noticed that the tone would continue occasionally when a button was pressed, even after the hold on the button releases. This bug was extremely unpredictable; it would not occur on every single button, and it would not occur at the same buttons when the game was restarted. At no point did I alter the stopTone() function, so this issue really puzzled me. When I had first realized that the bug was there, I had just implemented the feature that speeds up the playback of clues. As such, I perceived the issue to be with this implementation. Therefore, I reversed all of the code that I wrote for this feature to see if that would restore the game. Unfortunately, it did not. I approached the issue in another way, instead implementing the stopTone() function within the guess(btn) function. Unfortunately, this did not succeed either. I retraced the majority of my steps throughout the tutorial, believing that I made some sort of typo or misstep. I compared all of my functions to what the functions were supposed to look like, but I found no errors. Finally, my last resort was to rewind my Glitch project to a time when I knew the project worked. From there, I slowly implemented the optional features, testing each and every feature along the way. Surprisingly, I found the issue after implementing my first optional feature: including images within the buttons. As it so happened, the CSS that I included for the images was clashing with the properties of the button when the button was active. Therefore, the active state was persisting when the button was no longer held, and the tone was continuing to play. After understanding the bug, I was able to fix the CSS so that the image would not interfere with the functionality of the tone. From this challenge, I took away the importance of testing your code after every implementation. In technical courses, the importance of unit testing, component testing, and system testing is explained in theory. However, undergoing the consequences of not adhering to proper testing methods makes this point much more clear for future projects.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 

After completing my submission, I have a lot of questions about CSS properties. After doing a bit of research into display properties, I noticed that there are a plethora of CSS properties, and each one has a distinct feature that shapes the structure and composition of the HTML tag that it is associated with. I find frontend UI/UX design to be a creative outlet for people in my field. In other words, UI/UX design is a form of art for computer scientists and software engineers. Therefore, I would find it extremely interesting to delve into this type of engineering and see what I could create once I understand more of the properties associated with CSS. Additionally, I wish to understand more about JavaScript as a backend language. Understandably, many applications and programs are much more complex than this simple light and sound memory game. Therefore, there are other processes that must go into backend development, and I would like to see that it practice.

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 

If I had more time to work on this project, the first functionality that I would implement is making it so when the user presses the buttons, the Harry Potter logos appear. I liked the way that the logos appeared when the clue sequence was being played; however, I believe that adding the logos to when the user presses the buttons as well would make the game more intuitive. Furthermore, I would refactor the positioning of the buttons so that when the Harry Potter logo images do appear, the buttons do not shift downward. I believe that this issue lies with a bug in the CSS, but I was not completely sure of all of the properties that the CSS had to offer. Therefore, if I had more time, I would continue to research how I could solidify the positioning of the button when the image appears. Finally, I would implement a feature that allows the user to click a button for a hint, which would, essentially, play the previous clue over again. The user would get 2-3 hints per game. Once they use all of their hints, they are on their own.



## License

    Copyright Nanar Boursalian

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.