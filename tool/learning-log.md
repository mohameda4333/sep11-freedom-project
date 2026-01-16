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
### 12/7/25
* I learned how to add a health bar to my sprite. I made the hp a variable and then assigned its position and health:
```js
let hp = 3;

const hpText = add([
    text("HP: 3"),
    pos(20, 60),
]);
```
* This adds a health bar to the sprite which is assigned to be 3 health points.
* I also learned how to add sound effects from a youtube video. Once I assign a variable to the sound, I can play the sound depending on what I choose as the input, for example the space bar and the up arrow key:
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
* Now, I am trying to learn how to add an intro the game like a title screen. I am currently trying to understand the code for it. I want the title screen to say: "Press space to begin". Then I make a code that starts the game when the user presses the space bar.

### 1/15/26
* I learned how to shoot bullets out of my sprite. When the user presses the letter b, the bullet moves forward:
```js
onKetPress("b", () => {
    add([
        rect(6, 3),
        pos(player.pos),
        move(right, 700),
        area(),
        cleanup(),
        "bullet"
    ])
})
```
* I researched how to make the bullet dissapear being shot, and I found out about the cleanup() concept. This makes the bullet dissapear after the sprite shoots it.
* Then I also added a target for the sprite to shoot at:
```js
let target = add([
    rect(40, 40),
    pos(300, 150),
    color(0, 255, 0),
    area(),
    "target"
])
```
<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
