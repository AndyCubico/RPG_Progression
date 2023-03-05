
This is a page created by Andreu Nosàs Soler, student of the Bachelor’s Degree in Videogame Design and Development from CITM. It is an introduction to progression systems and a guide in how to create them in a RPG.

# Introduction

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

1.-Player progression: improvement of the skill and knowledge of the game that is being played. Many action based games are designed around this concept.

![you died](https://i.ytimg.com/vi/-ZGlaAxB7nI/maxresdefault.jpg)
> After dying many times, in souls games the player gets better and can defeat the challenge that he is facing.

2.-Character or abstracted progression: our character becomes stronger outside of the player’s skill. RPGs are the best example of this (leveling up)

![level up](https://media.rawg.io/media/crop/600/400/screenshots/062/0622bec29ae3ef0e8762a9c9f3e7b0f4.jpg)

3.-Game progression: moving through the different levels and areas of the game until reaching the credits.

![kojima](https://media.tenor.com/NRCKemMTCx8AAAAC/hideo-kojima-credits.gif)


There are also 5 key elements of gameplay progression that we have to keep in mind in order to create a good progression system:

1.-Game Mechanics: they directly affect the control complexity and the learning curve of the game. There are two ways to create this progress:
  - Gated access: make some mechanics unavailable initially. Metroidvanias are a great example.
  
  ![HK](https://i0.wp.com/playerassist.com/wp-content/uploads/2021/11/258188612_301604788635894_7952432341718812820_n.jpeg?fit=828%2C466&ssl=1)
  >Double jump feature in Hollow knight is unlocked later in the game
  
  - Directed gameplay: all mechanics are available from the get go, the gameplay will entice the players to use them as the game goes on.
  
   ![Souls](https://i.ytimg.com/vi/8nmobLqGOsY/maxresdefault.jpg)
   >In souls games you have all the abilities tied to the character from the beginning.

2.-Experience duration: how much time it takes to finish a level, stage, mission, which can be increased with mission distance and opponent difficulty.

3.-Scene rewards: create the levels of the game in a way that new visual rewards like exciting environmental wonders or fancy visual effects are staggered at a pace that keeps the player invested in the game.

![ER](https://user-images.githubusercontent.com/99950309/222971042-3fd4492f-93bc-46d3-8ca0-17279dbdb7b9.png)
>In Elden Ring, after defeating the first demigod, Elden Ring shows us how much is left to explore.

4.-Practical rewards: unlocking new content pieces or upgrading our characters that directly change, expand and improve how the game is played.

5.-Difficulty:  how hard are enemies to beat and also very important, how much risk the player takes in order to beat it with respect to player health (death), weapon durability, use of items (health potions).

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

# Math in progression systems

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



# Game loop and avoiding repetition

In order to have a good progression system and keep the flow of the game, it is very important to try to hide the game loop, that is, avoiding repetition. 
We should avoid introducing grinding in our game, limiting the player’s ability to progress is reduced to a few set options, and everything else will not move them forward.
When players are forced to make a number of repetitive tasks just to collect enough points to level up, that is usually not fun for them. The player’s actual skill progression is not accurately tied to in-game progression. Adjust the difficulty level accordingly to avoid this kind of situation. One interesting way of tackling this problem is the level progression of chrono cross, where you only level up when you defeat the bosses, earning also stars for the sense of reward, allowing you to become stronger and advance to the next level.

![chronocross](https://user-images.githubusercontent.com/99950309/222974776-d40876cd-3af1-4a01-a6bc-22479565f8bf.png)

We should also not be aiming to create what is called skinner boxes, psychological traps designed to keep us playing the game. Progression systems don't need to be skinner boxes to be good. Progression systems should be part of the experience of the game, and not something merely created to keep the player playing the game, adding play hours and no content.
Progression systems can add a long-term strategic component to our game. Most decisions that the player makes while playing are pondered in brief moments, but with a great progression system we can give the player the opportunity to plan out and contemplate these decisions for hours or even days (planning builds). An example of this could be the talent tree in World of Warcraft:

![wowSkill](https://user-images.githubusercontent.com/99950309/222974815-fd43d772-b96a-48e1-8a54-20a1546b8fee.png)

Anyone who has played an MMO knows how much time they can spend thinking about a build, to maximize damage output or be the tankiest character in the game. This adds a lot to the game, since you can have something to brainstorm about even when you are not playing the game.Be mindful of rewarding the player for thinking through the strategic conundrum that you are presenting, and a way to backtrack if they are not happy with the results of their build (re-spec).

Progression systems can also be created in such a way that the player shapes their learning curve and complexity of the game. That can be done with gated access to the game mechanics, introducing the elements one by one, allowing the player to familiarize with the given mechanic and get comfortable with it before moving on to the next one. Unlike tutorials, the player has control over how long each step of the learning curve takes, since if they have completely figured out the mechanic, they will be more efficient doing the challenges related to it, making them progress faster towards the next one.

![SelfRegulatingCurve](https://raw.githubusercontent.com/AndyCubico/RPG_Progression/main/docs/images/SelfRegulatingCurve.png)

A progression system can also enhance your narrative, for instance, faction progression, where actions you take affect your alignment with a faction in the game's world.

![ME reputation](https://user-images.githubusercontent.com/99950309/222974977-b5ac012e-3e58-4b1f-871f-d217b37719ef.png)
>Mass Effect's reputation system is a great example of this.


# Game Balance

We will begin this section with an example of how to balance the party members of a classical RPG and see what problems we could have.

## Character balance

This will be the base stats of our main character Squell at level 20:

```js
Strength: 50
Speed: 25
Stamina: 40
Spirit: 20
Defense: 40
Magic Defense: 15
```

Then we will create what are called the **Derived Stats**, the meanings of the base stats used to determine the effectiveness of them in battle. In this case they would be the following:

```js
Attack Power
ATB Speed (time until next turn)
Dodge %
Hit Points
Magical Power
Physical Damage Negated (%)
Magical Damage Negated (%)
```
### Determine Attack Power

In order to determine the attack power of Squell, we will multiply Strength by a constant of 10, since RPGs usually have a big number to show damage.

>Attack Power = Strength * (constant) = 50 * 10 = 500

To make it less boring we could add some variance:

>Attack Power = (Strength * (constant)) +/- 10% = 500 +/- 50 = 500 or 450

Now, Squells’s Attack Power will be somewhere between 450 and 550. 

### Determine Seconds Per Turn and Dodge %

This are based on speed, in this case since this stat should not increase too much throughout the game (otherwise it would be too powerful), we can divide it by the current level, getting a Speed coefficient.

>Speed Coefficient = Speed / Level = 25/20 = 1.25

With this, our character with 25 speed at level 20 would have 1.25 speed coefficient. We will make a table to see if it makes sense and is not too exploitable.

![TableSpeed](https://user-images.githubusercontent.com/99950309/222976708-c6da3ad8-59bc-41e0-8aa7-1cef7169bd77.png)

Looks good enough, now we feel comfortable calculating Squell’s Time until next turn (ATB speed), that is, the time between turns. This value should go down (the faster the character the faster he gets the turn back), to do this we will divide a constant by the speed coefficient.

We will use 15 as our constant, but you can choose any number you like. A higher cosntant will mean more time between turns (slower pace of the game).

>Seconds Per Turn = (constant) / Speed Coefficient = 15/1.25 = 12 

Dodge % is the same - just divide the Speed Coefficient by a constant. Your only limitation would be to pick a reasonable constant, since accidentally choosing a large one would result in a Dodge Rate over 100 percent.

### The Rest
We can use similar equations to figure out the rest of Squell's derived stats. For instance, Stamina could be converted to Hit Points merely by multiplying it by a constatn. We would obtain the following table:

![SquellsStats](https://user-images.githubusercontent.com/99950309/222977123-9f3baa40-5c44-4d58-abd1-50b87781113e.png)

## Balancing party members

Now let's create a second party member, a mage called Riona with the following stats:

![RionasStats](https://user-images.githubusercontent.com/99950309/222977326-acc369c2-16de-4ef6-ac57-8cbf5301ecda.png)

If we want to balance our characters, we will have to take a look at their DPS. Let’s compare them:

>Squell's DPS = Attack Power / ATB Speed = 500/12 = 42.7

>Riona's DPS = Magical Power / ATB Speed = 500/10 = 50

Based on our calculations, Riona's DPS is 50 to Squell's roughly 42, pretty much in balance. However, we have to acknowledge the fact that Riona has MP to use his damaging spells, whereas Squell does not (he just attacks). And some of Riona’s spells will be stronger than others. Thus, we cannot calculate her DPS using Magical Power alone. Instead, let's delve a bit deeper.

### Spells

With magical power we will determine the value of each individual spell. We will consider three kinds of spells: fireball 1 (single target and cheap to cast), fireball 2 (with higher mana cost and damage than fireball 1), and meteor (area of effect).

Assuming a Magical Power of 500, the Power and DPS of each spell will function as follows:

![RionasSpells](https://user-images.githubusercontent.com/99950309/222977535-4960af31-033b-4a1f-81f3-fc1bcad946f4.png)

Note that fire 2 costs three times more than 1 and not 2, it would be too efficient, but you can make it cost twice, test and see how it goes.
We can also see that Meteor is only useful against multiple enemies
We will divide the damage of each spell by its ATB speed to get the dps, and by its mana cost to get the damage per mana point.

![RionasDPS](https://user-images.githubusercontent.com/99950309/222977586-6148475e-b34c-4b70-a062-89120862d62c.png)

Riona’s Dps could be obtained by multiplying average cost and DPM, getting around 100 (6.67 * 14.86), but we have to remember that her mana pool is limited, and his DPS will drop by 80 percent if he has to use basic attacks (Attack power divided by ATB, 200/10).

We know that Squell's base DPS is 50, and that Riona's is approximately 100 when she has MP and 20 when she does not. In order to figure out the perfect ratio of magical to physical attacks to be equal, we use the following system of equations:

![Rionas_Squell_Equation](https://raw.githubusercontent.com/AndyCubico/RPG_Progression/main/docs/images/squell_riona.png)

> y = 5/8 and x = 3/8 where y is the time that she has to be with Attack damage and x the time that she can cast spells.

This means that in order to both have the same damage output, Riona would have to be 5/8 time (around 60% of the time) out of mana, which means that she is a little bit overpowered.

We should tinker with the previous values in order to balance it more, or leave as it is if that is our goal.
Consider this when blancing a your RPG:

1. What are my base stats? What are my derived stats?
2. Do the party members fall under specific class categories? If so, what are they?
3. What kind of numbers do I want to see on screen - big ones or small ones?
4. How much of a factor do I want randomness to play?
5. Is the scope of my game realistic, or will I end up spending months balancing my game?

Another thing to keep in mind are break points, places in your game where major experiential difference occurs based on minor mathematical differences. In a standard RPG, we could have the case where our character does 100 damage per hit, and the enemies in the zone have 150 hp, this would mean that it takes two hits to kill them. We will consider that when you level up, damage increases by 20 (linear progression of the stat). At level 4, you would have 160 damage, making that you can one shot the enemies, making that the challenge and difficulty of this zone dropped to the floor. It also happens when you can cast your spell twice as much or you are fast enough to always fight first. 

Breakpoints are not the same as power spikes, intentionally inserted mechanics that give the player a larger than normal boost of power when they reach a certain point in the game. A great example could be D&D's spells and abilities, which get more powerful at a certain level.

![fireball](https://user-images.githubusercontent.com/99950309/222978323-f59a4b83-d335-40a8-978a-96a12da38d8d.png)

This gives a good sense of progression, getting you excited to reach new levels. It is important to differentiate the power spike from the breakpoint, since one happens by your choice and the other from unexpected problems of the math of your system. In order to predict or control these breakpoints, you will have to thoroughly test your game and consider if they are really intended power spikes or mistakes from your mathematical system of progression.
In the case mentioned before of one shoting the enemies, you could make that the rewards at that level in that zone get really bad, so that the player should move forward from that point.

# Conclusions
- Be mindful of the different ways you can create progression
- Mix systems so that the game feels varied and fun to progress through
- Avoid repetition and grinding so that the player does not get bored.
- There is not one way to create an experience curve, do the one that suits your game better.
- Play test the game many time to see if there are any breakpoints and the game is generally balanced.

# References

* [Break Points - Balancing the Math with the User Experience - Extra Credits](https://www.youtube.com/watch?v=A_e_qu9ghHk)
* [Progression Systems - How Good Games Avoid Skinner Boxes - Extra Credits](https://www.youtube.com/watch?v=S5camMoNw-o)
* [Robert DellaFave - Balancing Turn-Based RPGs](https://gamedevelopment.tutsplus.com/series/balancing-turn-based-rpgs--gamedev-12702)
* [Av Thomas KL - The problem of repetition](https://frictionalgames.blogspot.com/2011/11/problem-of-repetition.html)
* [Josh Bycer - The dangers of grind in game design](https://game-wisdom.com/critical/video-game-grinding)
* [Josh Bycer - Understanding progression models in game design](https://game-wisdom.com/critical/progression-models)
* [Gustavo Tondello - Level Up! The role of progression for gameful design](https://medium.com/gameful-design/level-up-the-role-of-progression-for-gameful-design-ce7a87e2b70)
* [Davide Aversa - GameDesign Math: RPG Level-based Progression](https://www.davideaversa.it/blog/gamedesign-math-rpg-level-based-progression/)
* [Will Luton - THE MATHEMATICS OF GAME BALANCE](https://departmentofplay.net/the-mathematics-of-balance/)
* [Chris Bateman  - Mathematics of XP](https://onlyagame.typepad.com/only_a_game/2006/08/mathematics_of_.html)
* [Megan Smith - 10 RPGs With Equipment-Based Progression](https://gamerant.com/rpgs-equipment-based-progression/#paper-mario)
* [Rena Darling - 8 Most Unique Leveling And Progression Systems In RPGs](https://www.thegamer.com/most-unique-leveling-progression-systems-rpgs/#camping-downtime---final-fantasy-15)

