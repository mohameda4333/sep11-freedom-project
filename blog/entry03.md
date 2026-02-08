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
I added this code in the `keypress` function. This code meant that the `bullet` sprite was created. The `pos` of the sprite would be at the sprite or players position x and y coordinates. The third line meant that the sprite would move right, or I can change it to left, at a speed of 500 so that the bullet looks like its being shot instead of moved. Then I also added 

### Next Steps

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
