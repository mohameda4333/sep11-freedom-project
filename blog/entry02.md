# Entry 2
##### 12/15/25

## Content
I am using [kaboomjs](https://kaboomjs.com/) to make a mini game that includes a sprite shooting at targets out of a toy gun. I have been learning my tool by watching tutorials on youtube such as the [CodeMe Club](https://www.youtube.com/watch?v=_X6vPV9KiCE). This video was very useful to me in the beginning since it helped me learn the basics of my tool. The person in the video also showed an example that I used to tinker with. I made progress by taking things slowly through the basics first. For example, I added a block at a certain position that moved depending on the users input of the arrow keys:
```js
kaboom()

let player = add([
    rect(40, 40),
    pos(100, 100),
])

onKeyDown("right", () => {
    player.move(200, 0)
})

onKeyDown("left", () => {
    player.move(-200, 0)
})
```
This allowed the block to move left or right at a speed of `200` depending on what arrow key the user presses. I also learned how to add sound effects to my sprite depending on the users input. I saw this example on a youtube video and researched online on how to make this code. This is the result:
```js
loadSound("shoot", "https://kaboomjs.com/examples/sounds/laser.mp3");
loadSound("boom", "https://kaboomjs.com/examples/sounds/boom.mp3");

onKeyPress("space",{
    play("shoot");
});

onKeyPress("upArrowKey", {
    play("boom");
});
```
This is just an example, but if I had a file called `laser.mp3` and `boom.mp3`, it would make a certain sound effect, (depending on what the user uses), when the user presses the `space bar` or the `up arrow key`.
## Engineering Design Process (EDP)
I am currently in step 5 of the engineering design process. This step is where I create the prototype. I am trying to create a mini game with kaboomjs to master the basic controls of the game such as moving with the keys and adding effects/sound depending on the users input. The next process is testing the prototype. After I learn how to make the basic controls of a mini game, I will test it and share it with my friends to see if it works well.
## Skills

### Time Management
One of the main skills I learned while learning my code was time management. I learned how to manage my time and find the free time to learn about kaboomjs. I have basketball practice and gym outside of school so I have to look for a day that I am free on to tinker with my tool.
### Attention To Detail
Another skill I learned to use while tinkering with my tool was attention to detail. The small mistakes I made in my code led to the entire game crashing and not responding to my keys. For example, when I tried to make the `uparrowkey` input, I put `uparowkey`. Since I misspelled the code, my sprite didn't move up when I pressed the up arrow key.
## Takeaways
Tinkering with my tool was really fun because while I made the code for my game, I got to play with my game for a little bit and explore other games similar to mine.
[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
