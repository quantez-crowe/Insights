# Insights from my Excel project [Who's That Pokemon!](xx) IN-PROGRESS


With this project, I wanted to try my hand at making a tool that compares up to two Pokemon via user search. With this tool, a user can select which Pokemon they would like to compare across 6 generations of Pokemon. This was a fun project, as I was able to use a variety of Excel functions and features (e.g., XLOOKUP, INDIRECT, IMAGE, data validation, defined names). I was also able to incorporate a radar chart, which is a feature of some games that allows the trainer to compare the various attributes of the Pokemon.

In this dataset, we had the following fields:
* #: ID for each Pokemon. This correlates to when the Pokemon was added to the game. Lower numbers indicate 'older' Pokemon, while higher numbers indicate the most latest additions to the franchise.
* Name: Name of each pokemon (e.g., Pikachu, Charizard, etc.)
* Type 1: Each pokemon has a type, which determines weakness/resistance to attacks (e.g., Normal, Electric, Fire, etc.).
* Type 2: Some pokemon are dual type and have an additional type (e.g., Normal/Flying, Rock/Ground).
* Total: Sum of all a Pokemon's various attributes (i.e., HP, Attack, Defense, SP Attack, SP Defense, Speed)
* HP: hit points, or health, defines how much damage a pokemon can withstand before fainting
* Attack: The base modifier for physical attacks. The higher the value, the more damage is done to the opposing Pokemon.
* Defense: The base damage resistance against physical attacks. The higher the value, the less damage physical attacks do. 
* SP Atk: Special Attack, the base modifier for non-physical (special) attacks (e.g. fire blast, bubble beam). The higher the number, the more damage is done to opposing Pokemon.
* SP Def: Special Defense, the base damage resistance against non-physical (special) attacks. The higher the value, the less damage special attacks do.
* Speed: determines which pokemon attacks first each round. The higher the value, the faster the Pokemon.

### Question 1: Which type is the most/least common? How many pokemon are associated with each?

Pokemon can be either single or dual type (i.e., two different types are associated with the Pokemon). For example, the fan-favorite Pokemon Pikachu is a single-type (Electric), whereas Charizard is a dual-type (Fire-Flying). Across 6 generations, the most common Pokemon type is Water (120). The least common is Fiary (35). This was solved via an array using COUNTIF. After combining columns C & D via the CONCAT function in Column F, I used the COUNTIF function to return instances where each type occured in Column F. This was necessary, as a standard pivot table won't recognize that a type may appear in either column: 
![image](https://github.com/user-attachments/assets/2366b372-204f-41d7-acb0-58e2c35feecc)



### Question 2: What are the top-10 strongest Pokemon?

Pokemon strength is determined by the sum of its individual attributes (i.e., Attack + Defense + HP + Speed + Special Attack + Special Defense). The top 5 are:
  1. Arceus, (720)
  2. Kyurem- Black, (700)
  3. Kyurem- White, (700)
  4. Palkia, (680) (there are 12 other Pokemon with a stat total of 680)
![image](https://github.com/user-attachments/assets/ba988be7-4013-4091-beb6-38879fe45f6d)



### Question 3: What are the strongest Pokemon by type?


### Question 4: 


### Question 5: 

