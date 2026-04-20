# Entry 5
##### 4/19/26

## Content
At this point in making my mini-game, I finalized my Minimum Viable Product (MVP) of the Freedom Project. My final game is a little sprite shooting `bullet` sprites at the `enemy` sprites that spawn anywhere on a random `y-coordinate`. When the `bullet` sprite collides with the `enemy` sprite, the `enemy` sprite dissappears and raises the score on the `score` title by one. 

To make my MVP I put my code in [kaboomjs](https://kaboomjs.com/play?example=add&code=eJx1UsFuwjAMvfcrrJwckaFQQJuQymW77bI74pBSa5rWNlXawapp%2Fz43aVkQkEMU2y8vzy%2F%2BNLm1FcrkaBy0B%2BsIMtCJKQrcJcCro%2B8OhRkqG9BCKp9tbIupVrDUY0L4uyLZB6amND05pvoncnToMF0rSNcRyUIzC29jyjgyOFEGEs9p61fqX%2BypZilCocy2oTiv7JHwIR1YtLzAFde4W7DTNYxBA%2BMlrr2Ji2BvjtqWcY05UMD%2BhJbODpxdeFKwGpucfBh5%2BRgVYjeG5V999B6eHfNO5V9lSZ3wCXbrVyaltQ2mClBCtoW7SpbxH05aVoNNztQFrn2ZW7yvSVBNVR8%2FbetnW5YfBeGkS00o1mMU5JGmgtrO2R6NvAjzEIaBnGWw8OE78SiGQZM7vZ8Ps8kzFlIbEDALN1jFHwKvudU%3D).
* Firstly, I added the `score` title in the top left corner of the screen:
```js
add([
    text("acore: 0"),
    pos(20, 30),
    "score"
])
```
* Then I made the little `player` sprite that shoots the `bullet` sprite at the `enemy` sprite:
```js
var player = add([
    rect(25, 25),
    pos(100, 100),
    area(),
    "player"
])
```
* I gave the `player` sprite directions to move and keys to move all ways:
```js
onKeyDown("a",()=>player.move(-200, 0))
onKeyDown("d",()=>player.move(200, 0))
onKeyDown("w",()=>player.move(0, -200))
onKeyDown("s",()=>player.move(0, 200))
```
* This means that the `player` sprite moves at a speed of 200 in every direction
* Then I made a `bullet` sprite that is positioned to start from the `player` sprite's coordinates so that it looks like a bullet being shot:
```js
onKeyPress("space",()=>{
    add([
        rect(8, 4),
        pos(player.pos),
        area(),
        move(725, 200),
        "bullet"
    ])
})
```
* I also made a loop function to create non-moving `enemy` sprites at a random x-coordinate between `50, 400` and a random y-coordinate between `50,300`
```js
loop(2, () => {
    add([
        rect(30, 30),
        pos(rand(50, 400), rand(50, 300)),
        area(),
        "enemy"
    ])
})
```
* Lastly, I created a function that increases the score by one if the `bullet` sprite collides with the `enemy` sprite.
```js
onCollide("bullet", "enemy", (a, b) => {
    destroy(a)
    destroy(b)
    score += 1
    get("score")[0].text = "score: " + score
})
```
## Engineering Design Process
I am currently still in stage 7 of the Engineering Design process which is to improve as needed because there are still many functions about the game that doesn't work yet. For instance, I wanted the enemy targets to move at a certain speed but instead I made them stationary while the `player` s[rite can not lose. So I want to go beyond the minimum viable product and build a harder and more challenging game for people to play.
## Skills
While I was building the MVP of my Freedom Project, I learned how to communicate with other people and how to have a growth mindset.

### Communication
I learned how to communicate with my classmates during class as I showed them my product. They told me on what I can improve on and I took it as advice. I talked to my classmate during 6th period and he saw my game but he didn't like the fact that there was no losing in the game. The game was just all about shooting targets. This helped me think about more ways to make my game more challenging and fun to play.
### Growth Mindset
Having a growth mindset is very useful, especially when making a project. Since I already finished my Minimum Viable Product, I can now think of specific ways to make my product better. This skill is what helps people improve on their skills and abilities. Having a growth mindset gives you more potential to create something greater than before.
[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
