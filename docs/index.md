
Welcome! This is a page created by Andreu Nosàs Soler, student of the Bachelor’s Degree in Videogame Design and Development from CITM. It is an introduction of progression systems and a guide in how to create them in a RPG.

## Introduction

Most players are familiar with the concept of difficulty progression, the fact that games should get harder over time. However, difficulty is only one portion of the progress of a game, and there are other elements that require to be structured and managed carefully so that the videogame can provide the user with a compelling and enjoyable experience throughout the gameplay. With that in mind, let’s see what Gameplay progression really is.
This are a couple of definitions of the term that we can get from Oxford Languages:

```js
noun
1.forward or onward movement towards a destination.
"the darkness did not stop my progress"
2.development towards an improved or more advanced condition.
"we are making progress towards equal rights"
```

```js
verb
1.move forward or onward in space or time.
"as the century progressed the quality of telescopes improved"
2.develop towards an improved or more advanced condition.
"work on the pond is progressing"
```

All of these definitions could be applied to video games, since both the pattern of advance and the act of moving towards the ultimate goal of beating the game are key to creating an enjoyable experience for the player. This pattern of advance will keep the player in the game loop if done correctly.

Progression in video games can be divided into the three following categories depending on which is the focus:

1. Player progression: improvement of the skill and knowledge of the game that is being played. Many action based games are designed around this concept.

![you died](https://i.ytimg.com/vi/-ZGlaAxB7nI/maxresdefault.jpg)
> After dying many times, in souls games the player gets better and can defeat the challenge that he is facing.

2. Character or abstracted progression: our character becomes stronger outside of the player’s skill. RPGs are the best example of this (leveling up)

![level up](https://media.rawg.io/media/crop/600/400/screenshots/062/0622bec29ae3ef0e8762a9c9f3e7b0f4.jpg)

3. Game progression: moving through the different levels and areas of the game until reaching the credits.

![kojima](https://media.tenor.com/NRCKemMTCx8AAAAC/hideo-kojima-credits.gif)


There are also 5 key elements of gameplay progression that we have to keep in mind in order to create a good progression system:

1. Game Mechanics: they directly affect the control complexity and the learning curve of the game. There are two ways to create this progress:
  - Gated access: make some mechanics unavailable initially. Metroidvanias are a great example.
  
  ![HK](https://i0.wp.com/playerassist.com/wp-content/uploads/2021/11/258188612_301604788635894_7952432341718812820_n.jpeg?fit=828%2C466&ssl=1)
  >Double jump feature in Hollow knight is unlocked later in the game
  
  - Directed gameplay: all mechanics are available from the get go, the gameplay will entice the players to use them as the game goes on.
  
   ![Souls](https://i.ytimg.com/vi/8nmobLqGOsY/maxresdefault.jpg)
   >In souls games you have all the abilities tied to the character from the beginning.

2. Experience duration: how much time it takes to finish a level, stage, mission, which can be increased with mission distance and opponent difficulty.
3. Scene rewards: create the levels of the game in a way that new visual rewards like exciting environmental wonders or fancy visual effects are staggered at a pace that keeps the player invested in the game.

![ER](https://user-images.githubusercontent.com/99950309/222971042-3fd4492f-93bc-46d3-8ca0-17279dbdb7b9.png)
>In Elden Ring, after defeating the first demigod, Elden Ring shows us how much is left to explore.

4. Practical rewards: unlocking new content pieces or upgrading our characters that directly change, expand and improve how the game is played.
5. Difficulty:  how hard are enemies to beat and also very important, how much risk the player takes in order to beat it with respect to player health (death), weapon durability, use of items (health potions).

If game designers do not structure correctly all these elements, they may overwhelm the user with too much, or boring them with too little so they stop playing. The concept that defines this matter is the Flow.
Flow is a mental state of operation in which the person is fully immersed in whatever he is doing, with a feeling of energized focus, full involvement, and success in the process of an activity.

![Flow](https://user-images.githubusercontent.com/99950309/222971230-5e57344f-fa22-4edf-aeaa-aceb46cfcb70.png)

It is key to the design of the game to keep the player on the flow zone, otherwise our users will stop playing the game.
A good progression system should motivate players to keep playing, no matter if they are winning or losing. As long as the player is moving forward, they will be motivated to keep playing, otherwise they will be frustrated and stop playing the game.

### Type of progression in RPGs

#### Level based progression:

The most classic one, players gain experience points when defeating enemies, leveling up their character when they reach a certain amount of points, becoming stronger when doing so. The following levels usually are harder to get, so it is harder to become stronger as the game goes on.
Most JRPGs and CRPGs use this system.


#### Training progression:

The player increases their power when they perform certain actions or use specific tools to perform these. Skyrim is the best example of this kind of system, where running or killing enemies with a given type of weapon increases the proficiency with it.

![Skyrim](https://user-images.githubusercontent.com/99950309/222971416-153f3a0a-91ec-4df1-b852-269ebc67cbf3.png)

#### Skill tree progression:
players can customize how their character develops with a skill tree, where they can allocate earned points to gain different kind of abilities, creating a build path to pursue (similar to previous one but it is important to note how you obtain the resources to advance through them and how they are created).

![Borderlands 3](https://user-images.githubusercontent.com/99950309/222971511-c4f7aa38-d6a4-475f-8814-1d071f5c90ee.png)

#### Equipment based progression:
Player focuses on finding better armor and weapons to upgrade their character, at the cost of giving up whatever they had beforehand. A great example of this is the MH saga.

![MH](https://user-images.githubusercontent.com/99950309/222971576-802d03c0-669b-451b-8624-25dd1d61a711.png)

Most RPGs integrate these systems together, FFIX keeps the traditional xp leveling systems of RPGs and introduces the equipment based progression with training progression, where you have to equip certain items to gain cool new abilities, and when you have used them enough you can get the abilities without the equipment needed.

![Level Up FFIX](https://user-images.githubusercontent.com/99950309/222971666-4b337a2f-e51e-4210-9883-e615f675c609.png)

![Equipment FFIX](https://user-images.githubusercontent.com/99950309/222971619-f8df9862-36c2-476b-b737-1ccdeace02e4.png)

## Math in progression systems

![Bender](https://media.tenor.com/PZomwjyO_78AAAAd/bender-we-need-to-use-math.gif)

As we have seen, the most typical way in RPGs to create a progression system is with level progression requiring a given number of experience to reach each level.
In order to see how to create such a system, we will see 4 different types of functions where we plot the values of the experience required(y) and the current level(x). With these, we will be able to define how much experience (and time) the player invests in the game in order to gain a level. This are the curves that we will see:

![curves](https://user-images.githubusercontent.com/99950309/222972447-4bc62cc5-6a07-449c-ae64-a054a347f9f4.png)

>Example of progression curves: Linear (blue, A), logarithmic (orange, B), quadratic (red, C) and exponential (green, D).

If our experience curve is linear, each level will require the same amount of extra amount of experience with the following function:

Linear curves for the purpose of determining the xp required to level are not used given how boring they can be, since they are predictable and can feel grindy. However, they can be used to make the progress of some stats with each level increase.

If we use an exponential curve or polynomial, the player will need more experience to reach the next level that the previous one, and therefore the player levels-up slower at the end game. 

And if we use a logarithmic curve, at every level we will need less experience than the previous level. The exponential and plolynomial are the most popoulars in RPGs, but you can choose whichever you see fit for your gameplay ideas.

Mind that exponential and polynomial curves have a subtle difference, while the exponential curves grow at the same ratio all the time (having astronomical values beyond any reasonable expectation of achievement at later levels), the polynomial cruves growth actually gets smaller as the level increases. In exponential progression systems we will have to raise the rewards to keep up with the level required to get them (easily exploitable, since you can kill a harder boss and get so much xp that you rush through the game). Polynomial systems they can get grindy since and repetitive since the differences at higher levels are too subtle.

### Examples:

- World of Warcraft, we have a formula for the experience required to level up at a certain level:

<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">
  <mi mathvariant="normal">&#x394;</mi>
  <mi>E</mi>
  <mo stretchy="false">(</mo>
  <mi>L</mi>
  <mo stretchy="false">)</mo>
  <mo>=</mo>
  <mo stretchy="false">(</mo>
  <mo stretchy="false">(</mo>
  <mn>8</mn>
  <mo>&#xD7;</mo>
  <mi>L</mi>
  <mo stretchy="false">)</mo>
  <mo>+</mo>
  <mi>D</mi>
  <mi>i</mi>
  <mi>f</mi>
  <mi>f</mi>
  <mo stretchy="false">(</mo>
  <mi>L</mi>
  <mo stretchy="false">)</mo>
  <mo stretchy="false">)</mo>
  <mo>&#xD7;</mo>
  <mi>M</mi>
  <mi>X</mi>
  <mi>P</mi>
  <mo stretchy="false">(</mo>
  <mi>L</mi>
  <mo stretchy="false">)</mo>
  <mo>&#xD7;</mo>
  <mi>R</mi>
  <mi>F</mi>
  <mo stretchy="false">(</mo>
  <mi>L</mi>
  <mo stretchy="false">)</mo>
</math>

Where diff is a difficulty factor
Where diff if a difficulty factor, MXP is the basic experience given by a monster of level L and RF is a generic scaling factor. This formula start as a quadratic experience curve and then explode into exponential (thanks to the Diff formula).

![WOW](https://user-images.githubusercontent.com/99950309/222973681-b235f828-b885-4b79-b85e-258925aae025.png)


- Diablo 3, the formula varies depending on what threshold of levels is the user:

![diablo3](https://user-images.githubusercontent.com/99950309/222973751-3fbaa123-e76f-44c1-80c1-3cf4f8a42316.png)

- Dreamcast game Armada (Metro 3D, 1999), uses the formula of 8 x (current level)^3 to determine the XP requirements.

![Dreamcast](https://raw.githubusercontent.com/AndyCubico/RPG_Progression/main/docs/images/dreamcastgame.jpg)



## Game loop and avoiding repetition



