# Final Project Assignment 2: Explore One More! (FP2) 
DUE March 30, 2015 Monday (2015-03-30)

### My Library: rsound, racket/gui/base

For the second part of this project, I elected to play with an audio library. Since I originally used a GUI library,
I took that code from that an altered it to suit my needs for this library. So what I did was create a few different
buttons in the GUI window, and figured that I would alter the code so that instead of showing a message in the 
window, I would make each button produce a tone. This was a lot easier than I expected, and all I did was replace
the code to show a message with the relatively simple code to play a specific note. I did this to create three
buttons that play three different notes, one that plays all three notes simultaneously, and made the close button
emit a "ding" noise when pressed.

![alt text](https://github.com/stuarttomkins/FP2/blob/master/window.png "Window Screenshot")

```
(require rsound)
(require racket/gui/base)
 
(define frame (new frame% (label "Final Project 2")))

(define msg (new message% (parent frame)
                          (label "Click a button.")))

(define panel (new horizontal-panel% (parent frame)))
(new button% (parent panel)
             (label "Low")
             (callback (lambda (button event)
                         (send msg set-label "Low Note!")
                         (play (make-tone 220 0.5 50000)))))
(new button% (parent panel)
             (label "Mid")
             (callback (lambda (button event)
                         (send msg set-label "Mid Note!")
                         (play (make-tone 330 0.5 50000)))))
(new button% (parent panel)
             (label "High")
             (callback (lambda (button event)
                         (send msg set-label "High Note!")
                         (play (make-tone 440 0.5 50000)))))
(new button% (parent panel)
             (label "Harmony")
             (callback (lambda (button event)
                         (send msg set-label "Woohoo!")
                         (play (make-tone 220 0.4 50000))
                         (play (make-tone 330 0.4 50000))
                         (play (make-tone 440 0.4 50000)))))

(new button% (parent panel) 
     (label "Close")
     (callback (lambda (button event)
                 (play ding)
                 (send frame show #f))))

(send frame show #t)
```

As with the first program, the output was nothing interesting. It produced this code:

```
  (object:button% ...)
  (object:button% ...)
  (object:button% ...)
  (object:button% ...)
  (object:button% ...)
```

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

