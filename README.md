# Object Oriented Programming Project

Team Members:

Name	Student ID	Email	Year
Stylianos Prasianakis	1115201700233	sdi1700233@di.uoa.gr	6th year
Georgios Pantelakis	1115201900140	sdi1900140@di.uoa.gr	4th year
Contribution of Each Student

The assignment was mostly done as a team, with both of us working together on the same parts of the exercise. There was constant communication regarding the progress of the code (what needed to be done next), and both of us always had oversight of the whole project.

Comprehensive Code Description

Our superclass is the Figures class, and we use three subclasses — Werewolves, Avatar, and Vampires — which inherit from Figures. We used encapsulation for the class attributes described in the assignment, along with accessors to access them. The superclass has the methods Move, Attack, and Heal, while the Move method is overridden in the Vampires class (diagonal movement) and the Avatar class (player input).

At the start, the user enters the dimensions of the map. The map is stored in a vector of Block objects. Block is a class representing each position on the map.

Trees and water are then generated in a quantity of map_size/10 and are immediately removed from the map. Afterward, the Werewolves are created and stored in a vector pointed to by Werewolves, followed by the Vampires, stored similarly in a vector pointed to by Vampires. Finally, the Avatar is created.

The game is rendered in real time. The Avatar is marked with a W or V depending on the team it supports (chosen by the player).

All entities, the removed obstacles (marked with an X on the map), and the magic potion (marked with an M on the map) are placed at random positions.

The game then begins. First the Werewolves move, then the Vampires, and finally the user. If, after moving, a Werewolf or Vampire finds another entity next to it, it checks whether that entity is an opponent or a teammate, then either attacks or flees (in the case of an opponent) or decides whether to give medicine (in the case of a teammate). Two players cannot occupy the same block.

If the user steps on the M block (the magic potion), their potion count increases by one.

Within the game, day and night alternate every 5 rounds. Depending on the time of day, the player can pause to view game information and decide whether or not to give medicine to their team.

The game ends when an entire team — either the Werewolves or the Vampires — has died. In the code, we check whether either of the two vectors has become empty.

(Throughout the program we have left print statements as comments so that the correct functioning of the features described in the assignment can be verified.)

Assumptions

In our code, we made the following assumptions:

The Werewolves move first, then the Vampires, and finally the Avatar.
After moving each round, the Werewolves and Vampires decide whether to attack, retreat, or heal a teammate. This round logic is implemented in the play function.
Diagonal positions are considered neighboring blocks.
At the start of the program, blocks corresponding to water and trees are simply removed from the map.
IDE / Compiler
Visual Studio Community
C/C++ Optimizing Compiler Version 19.33.31630 for x86
Issues Encountered

Until we conceived the idea of the Block class, our code wasn't progressing quickly. Afterward, the functions came together more easily and the code became much clearer.

Unimplemented Features

Everything was implemented.

Difficulty Rating

7/10

Links
GitHub: https://github.com/stelpras/OOP-Project
YouTube: https://www.youtube.com/watch?v=6rYNRfW6lgQ
