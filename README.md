# Pre-work - _Memory Game_

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program.

Submitted by: **Nikita Kotsehub**

Time spent: **10** hours spent in total

Link to project: <br>
Code: [https://glitch.com/edit/#!/dull-cyber-sidecar?path=README.md%3A1%3A0](https://glitch.com/edit/#!/dull-cyber-sidecar?path=README.md%3A1%3A0) <br>
Website: [https://dull-cyber-sidecar.glitch.me/](https://dull-cyber-sidecar.glitch.me/)

## Required Functionality

The following **required** functionality is complete:

- [x] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
- [x] "Start" button toggles between "Start" and "Stop" when clicked.
- [x] Game buttons each light up and play a sound when clicked.
- [x] Computer plays back sequence of clues including sound and visual cue for each button
- [x] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess.
- [x] User wins the game after guessing a complete pattern
- [x] User loses the game after an incorrect guess

The following **optional** features are implemented:

- [x] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
- [x] Buttons use a pitch (frequency) other than the ones in the tutorial
- [x] More than 4 functional game buttons
- [x] Playback speeds up on each turn
- [x] Computer picks a different pattern each time the game is played
- [x] Player only loses after 3 mistakes (instead of on the first mistake)
- [x] Game button appearance change goes beyond color (e.g. add an image)
- [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
- [x] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [x] List anything else that you can get done to improve the app!
- [x] After winning a pattern, user gets 'Mission Complete' picture with accompanying sound from GTA San Andreas
- [x] After losing, user gets 'You Died' picture with accompanying sound from Dark Souls
- [x] User can change the pattern length. It also increases with every success.
- [x] The game keeps track of the Max and Current scores

## Video Walkthrough

Here's a walkthrough of implemented user stories:
<img src="http://g.recordit.co/h28NYOBiyD.gif" width=1000><br>

## Reflection Questions

1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here.
   <br>

   StackOverflow: many-many searches for various Javascript, HTML, and CSS questions
   w3schools: a few guided tutorials on setInterval and setTimeout

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words)
   <br>

   The biggest challenge was setting up the timer that limits the time user has to click a button.
   At first, I thought through the logic of countdown and outlined it on paper. Then, I started experimenting with setInterval() and setTimeout().
   It had some troubles combining the two at the same time. I would have several setIntervals run at the same time.
   I tried stopping them with clearInterval(), but it did not help. I figured that it is probably because of local vs. global variables.
   I read more questions on Stack Overflow and w3chools to see examples of implementing setInterval(). When I ensured that the logic is correct,
   I decided that it might be a bug. I went over the relevant code lines and added outputs to the console to identify the bug. After 15 minutes of careful debugging,
   I found that I was re-assigning variable intId, thus erasing its connection to the corresponding Interval, not being able to stop it later.
   What helped me is firstly understand how the functions work and interact. I learned setInterval through basic, minimal reproducible examples.
   I was building up complexity and experimenting with inputs. Once I understood how the function works, its inputs and outputs, I tried implementing it in my program. When I got stuck,
   I checked for inputs and outputs and then debugged using console.log and simply talking myself through the code.

3) What questions about web development do you have after completing your submission? (recommended 100 - 300 words)

   It was interesting to see how we can create a fun web-app that runs on the user's end. I am curious to what extend we can go with this.
   Specifically, recently I wrote a web-scraper in Python that outputs stats about a YouTube channel given the URL.
   Assuming we only want to show the output without storing it in a database, could I implement this web-scraper with Javascript and make it run on the user's end?
   This, of course, depends on Javascript's capabilities, and I am curious to test how powerful it is.

   I also liked that, at first, I had a basic HTML/CSS style and focused on finishing functionality with Javascript.
   Once I had all the features, I started playing around with color palettes, Bootstrap containers, placement, alignment, etc.
   It was like putting together LEGO and trying different variations. I would be curious to learn more about creating stylish and user-friendly UI and UX efficiently.
   Furthermore, I'd like to see how I could incorporate my Adobe Illustrator skills into it. I have heard of some programs that allow you to design the website UI first and
   then get the HMLT/CSS code for it. I would be curious to see how the code and design interact with each other in such programs.

4) If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words)

1. Firstly, I would want to ensure that anyone can understand and reproduce my code. For this, I would add comments and docstrings.
2. I want my game to be friendly for all devices. Hence, I would turn away from fixed quantities like width: 50px and go to percentages to ensure that mobile users don't have to struggle with gigantic buttons.
3. Then, I would factor several functions. For example, my totalLoss() function combines all loss-related functions in a single driver function. However, when the user wins, the victory-related functions are scattered around. It would be nice to organize them in one place.
4. As a technical challenge, I would attempt using other sounds, such as bass guitar or drums. This would spice up the game and also train musical hearing skills.
5. I would continue iterating upon the design. Specifically, when I added button 8, it jumps onto the second row. It'd be better if my buttons were placed in the center with margins and would altogether form a large square rather than a single line.
6. I would make adding buttons more efficient with a loop, rather than repeating my code many times and copy-pasting the same lines.
7. It'd be handy to store the results and stats for every user. I could use cookies or a database, but that would require backend.
8. I could add many other features, but the last, and essential one, is the colorblind mode. My buttons involve many colors, and having a toggle that turns them into colorblind colors would add accessibility to my users.

## License

    Copyright Nikita Kotsehub

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
