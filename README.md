# Final Project Assignment 2: Explore One More! (FP2) 
DUE March 30, 2015 Monday (2015-03-30)

This is just like FP1, but where you do a different library. (Full description of FP1 is [on Piazza.][piazza])

During this assignment, you should start looking for teammates. See the project schedule [on Piazza.][schedule]

Write your report right in this file. Instructions are below. You can delete them if you like, or just leave them at the bottom.
You are allowed to change/delete anything in this file to make it into your report. It will be public.

This file is formatted with the [**markdown** language][markdown], so take a glance at how that works.

This file IS your report for the assignment, including code and your story.

Code is super easy in markdown, which you can easily do inline `(require net/url)` or do in whole blocks:
```
#lang racket

(require net/url)
```

### My Library: rsound

Write what you did!
Remember that this report must include:
 
* a narrative of what you did
* the code that you wrote
* output from your code demonstrating what it produced
* any diagrams or figures explaining your work 
 
The narrative itself should be no longer than 350 words. Yes, you can add more files and link or refer to them. This is github, handling files is awesome and easy!

Ask questions publicly in the Piazza group.

For the second part of this project, I elected to play with an audio library. Since I originally used a GUI library,
I took that code from that an altered it to suit my needs for this library. So what I did was create a few different 
buttons in the GUI window, and figured that I would alter the code so that instead of showing a message in the 
window, I would make each button produce a tone. This was a lot easier than I expected, and all I did was replace the
code to show a message with the relatively simple code to play a specific note. I did this to create three buttons
that play three different notes, one that plays all three notes simultaneously, and made the close button emit a 
"ding" noise when pressed.





### How to Do and Submit this assignment

1. To start, [**fork** this repository][forking].
1. Modify the README.md file and [**commit**][ref-commit] changes to complete your solution.
  2. (This assignment is just one README.md file, so you can edit it right in github without cloning)
  3. (You may need to clone and push if you want to add extra files)
1. [Create a **pull request**][pull-request] on the original repository to turn in the assignment.

<!-- Links -->
[piazza]: https://piazza.com/class/i55is8xqqwhmr?cid=411
[schedule]: https://piazza.com/class/i55is8xqqwhmr?cid=453
[markdown]: https://help.github.com/articles/markdown-basics/
[forking]: https://guides.github.com/activities/forking/
[ref-clone]: http://gitref.org/creating/#clone
[ref-commit]: http://gitref.org/basic/#commit
[ref-push]: http://gitref.org/remotes/#push
[pull-request]: https://help.github.com/articles/creating-a-pull-request

