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
After storing the code to a variable, I made a sprite called target that looks similar to this [image](https://assets.targetimg1.com/webui/store-locator/targetlogo-6.jpeg). The `area()` concept ensures that the target sprite has a hitbox, so that the `bullet` sprite can collide with it.

### Next Steps

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
