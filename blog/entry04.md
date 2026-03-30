# Entry 4
##### 3/29/26

## Content
During the past couple weeks, I learned more about my game and p5js. I'm planning to use p5js on my website to make it more interactive. I'm thinking about making a shape that follows the users mouse to act as a cursor. I can also learn how to make an animation on my website where rain drops or little blocks fall down constantly on the page. This can make the website more interactive and fun to use. This will engage the user and attract them to learn more about the website and my mini game. 

I tried to make my mini game as realistic as possible through [kaboomjs](https://kaboomjs.com/). As a result, I attempted to make a health bar on the sprite. Everytime the enemy sprite touches the sprite, it loses one health point. It has a total of five health points. Then I made a conditional that tests when the sprite is at zero health points. If the conditional is true, the code returns the text `gameover`. Here are the steps in order of how I coded the health points:
* First, I made a variable to have the amount of health points stored in it:
```js
let health = 5;
```
* Then I made an event listener that functions when the `bullet` sprite collides with the sprite.
* After collision, the health bar decreases by one health point:
```js
player.onCollide("enemy", () => {
  health -= 1=
})
```
* Finally, I made a conditional to test when the health bar is equal to `0`. This returns the text `gameover`:
```js
if (health == 0) {
    go("gameover")
  }
```
## Engineering Design Process
I am currently in stage 7 of the engineering design process. This stage is where I `improve as needed`. In this stage, I am going beyond the minimum viable product as I try to improve the product as much as needed beyond it's mvp. The next stage in the engineering design process is to `communicate the result`. This is the stage where I share my product with other people and get some insight on how I can improve the game and get some reviews on it.
## Skills
Some skills I learned while trying to improve my game are `how to google` and `growth mindset`.
### How to google
While I was learning more about my tool and how to use it with my mini game, I learned more about `how to google`. I learned about more websites to research on such as [gamedevacademy.org](https://gamedevacademy.org/kaboom-js-tutorials/). This website gave me a colossal amount of information and videos that gave me more information on [kaboomjs](https://kaboomjs.com/) and how it works. As a result, this is an example of how I learned how to search for articles about my tool.
### Growth mindset
Another skill I learned while learning about my tool is how to have a `growth mindset`. After finishing the minimum viable product of my mini game, I realized that I can improve the game more and add more details to it. This was a part of my growth mindset because I had the mindset to grow and improve my game more.

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
