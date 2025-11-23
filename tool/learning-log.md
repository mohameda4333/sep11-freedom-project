# Tool Learning Log

## Tool: [Kaboom.js](https://kaboomjs.com/)

## Project: Game to test gun aim on target

---

### 9/29/25:
* I went on the [playground](https://kaboomjs.com/play?example=add) in kaboomjs and I tried to tinker in it.
* For example, in the `movement` section, I changed the code and I tinkered with the speed of the sprite.
* Then I searched up a youtube video of [how to make a game with kaboomjs](https://www.youtube.com/watch?v=hgReGsh5xVU).
* You can edit settings like width and height.
* You can create things like sprites or obstacles.
* Then you add the input of how the user interacts with the game.
* I will try to make a little game similar to the one I tinkered with next.

### 11/2/25:
* I tinkered with my tool through jsbin. I went to the "setup" page on jsbin: (https://kaboomjs.com/doc/setup). Then I copy and pasted the code into jsbin. The result was a gray and white squared background with the text: "Hello". Then I tried adding a sprite but it gave me an error because I put the code: "addsprite.png". I realized I had to have an image with that title and add it to the code. Then it would show a green sprite centered at (120, 80).
* I also went on the website itself and did some research:
* I learned that downloading the code makes it easier to work with kaboom.js.
* It reminded me of what I did in computer science because I can make sprites and give them an order. I can also place it somewhere specific based on the coordinates I put in the code.

### 11/23/25:
* I tried adding a block code to see how it works:
```js
kaboom()

let player = add([
    rect(40, 40),
    pos(100, 100),
    color(0, 0, 255)
])
```
* I changed the block color from blue to red using the rgb `color(255, 0, 0)`
* I also changed the size of the block from `(40,40)` to `(30,60)`
* Then I learned that I can make the square move with the arrow keys:
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
* I tinkered with the speed and changed it from `200` to `500`
* I also tried to make `up` and `down` keys
* I am currently trying to research how to shoot bullets out of the character.


<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
