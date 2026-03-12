# Entry 3
##### 2/2/26

### Content
During the winter break, I made a lot of progress learning my tool. I watched many youtube videos that show people making something with my tool, expiremented in jsbin to test some code, and tinkered with my tool on the [kaboom](https://kaboomjs.com/) website itself. Before the winter break, I tried to make a code where the sprite would shoot bullets when the user presses `k`, but it didn't work. So I watched another video on youtube during winter break that taught me all the basics of javascript in kaboomjs. After I did some research on how to use the `keypress` function, I came up with this code firt:
```js
onKeyPress("k", () => {
});
```
This means that when the user presses `k`, the sprite does a function based on my code. Then I added another sprite called `bullet` that moved to the right or left at a very high speed. This represented the bullet being shot from the sprite:
```js
 add([
        sprite("bullet"),
        pos(player.pos.x , player.pos.y),
        move(right, 500),
    ]);
```
I added this code in the `keypress` function. This code meant that the `bullet` sprite was created. The `pos` of the sprite would be at the sprite or players position x and y coordinates. The third line meant that the sprite would move right, or I can change it to left, at a speed of 500 so that the bullet looks like its being shot instead of moved. Then I also added a target for the `bullet` sprite to hit. Before I got some help, I made the `bullet` sprite move past the target without hitting it. Then I watched a [video](https://www.youtube.com/watch?v=VaADdGSKEbA&list=PLNwtXgWIx3rh34-c2WoTgKq4R0ZojqJ_B&index=3) of someone explaining how to make my sprite collide with another object. Firstly, I made a variable to store the information in. 
```js
var target = add([
    sprite("target"),
    pos(400, 200),
    area(),
    "target",
]);
```
After storing the code to a variable, I made a sprite called target that looks similar to this [image](https://assets.targetimg1.com/webui/store-locator/targetlogo-6.jpeg). The `area()` concept ensures that the target sprite has a hitbox, so that the `bullet` sprite can collide with it. I also went beyond the minimum viable product for my game and researched on how to make the game harder. I wanted to know if I could add levels or bosses in the game to make the game more difficult. I didn't want it to be the same consistent gameplay the entire time. Then I found an idea to make the enemy move faster after defeating each target. Firstly, I had to make an original speed for the enemy, so I made it `50`. I set it to the variable: `targetSpeed`.
```js
let targetSpeed = 50
```
After setting an original speed, I knew that the `+=` function would increase the enemies speed by a specific amount each time but I didn't know if I should put it in a function or what to do with it. So I gave AI this prompt: `what function or concept do I use to make the speed of a sprite faster each time it dies in kaboomjs?`. It provided a function but I didn't understand it that much, even when I asked it to explain it. Then it provided an alternative concept which was to use the `loop` concept. It gave me this code:
```js
loop(4, () => {
})
```
This was very easy to understand because it simply meant that every 4 seconds, a function would occur. So I added this code in the loop: `enemySpeed += 50`. This meant that each 4 seconds, the enemy would increase their speed by 50. This was the final code:
```js
loop(4, () => {
  enemySpeed += 50
})
```
### Engineering Design Process
My current stage in the Engineering Design Process is still stages 5 and 6. I am still in stage 5 because I am stil adding tweaks to the code that I tinker with so that it runs with no problems. However, I am also entering stage 6 because I am testing the code as I tweak it to make sure everything is correct. My next stage is to officially be in stage 6 where I am only testing the code and adding a few tweaks in stage 7.

### Skills
Some skills I learned while tinkering with my tool are consideration and debugging. Firstly, I learned how to debug my code and find the small errors I make. For example, I may spell something wrong in my code which would cause everything to crash. I also learned to consider everything while typing the code. For example, while I was making the code on how to shoot the `bullet` sprite, I put the collision between the two sprites into consideration so I ended up going back and finding out how to make the two sprites collide.

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
