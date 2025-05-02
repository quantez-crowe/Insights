# Insights from my Excel project [Who's That Pokémon!](xx) 


With this project, I wanted to try my hand at making a tool that compares up to two Pokemon via user search. With this tool, a user can select which Pokemon they would like to compare across 6 generations of Pokémon. This was a fun project, as I was able to use a variety of Excel functions and features (e.g., XLOOKUP, INDIRECT, IMAGE, data validation, defined names). I was also able to incorporate a radar chart, which is a feature of some games that allows the trainer to compare the various attributes of the Pokémon.

In this dataset, we had the following fields:
* #: ID for each Pokémon. This correlates to when the Pokemon was added to the game. Lower numbers indicate 'older' Pokémon, while higher numbers indicate the most latest additions to the franchise.
* Name: Name of each Pokémon (e.g., Pikachu, Charizard, etc.)
* Type 1: Each Pokémon has a type, which determines weakness/resistance to attacks (e.g., Normal, Electric, Fire, etc.).
* Type 2: Some Pokémon are dual type and have an additional type (e.g., Normal/Flying, Rock/Ground).
* Total: Sum of all a Pokémon's various attributes (i.e., HP, Attack, Defense, SP Attack, SP Defense, Speed)
* HP: hit points, or health, defines how much damage a Pokémon can withstand before fainting
* Attack: The base modifier for physical attacks. The higher the value, the more damage is done to the opposing Pokemon.
* Defense: The base damage resistance against physical attacks. The higher the value, the less damage physical attacks do. 
* SP Atk: Special Attack, the base modifier for non-physical (special) attacks (e.g. fire blast, bubble beam). The higher the number, the more damage is done to opposing Pokemon.
* SP Def: Special Defense, the base damage resistance against non-physical (special) attacks. The higher the value, the less damage special attacks do.
* Speed: determines which pokemon attacks first each round. The higher the value, the faster the Pokemon.

The coolest feature of this tool is the Pokémon selection feature, which returns an image from the [PokeDex](https://www.pokemon.com/us/pokedex) based on the Pokemon selected. I accomplished this via Excel's IMAGE function, which inserts images into cells from a source. One challenge, was that I needed the image to update dynamically, based on the user's selection. To accomplish this, I first found my image URL, and noticed that I could split it at the final '/', since it ended with the Pokémon's ID number and the file extension (.png):

![image](https://github.com/user-attachments/assets/00fcb3a2-821d-4a97-95e1-651755fff982)

So, I separated each into their individual parts, and created the following formula:

![image](https://github.com/user-attachments/assets/5d1bf281-4b0f-4f19-941d-fa12855af344)

Where V3 contains a CONCAT function that combines each aspect of the URL:

![image](https://github.com/user-attachments/assets/8e295933-86ca-4f9d-809c-666d07694f1c)

The result is an image that populates with the user's selection in real-time:

![image](https://github.com/user-attachments/assets/513eab72-6612-44eb-b8d9-af5a2b7c9ef4)

The dropdowns were crafted using XLOOKUP, data validation, and defined names. The XLOOKUP function was used to return the various attributes based on the selected Pokémon's name, which were restricted to a dropdown selection versus a text input. This also presented a challenge, as there are over 700 Pokémon in this dataset, and including them all would be cumbersome. The solution was to create dependent dropdowns by defining names. I created lists of all Pokémon associated with each of the 6 generations, and defined their names as follows: 

![image](https://github.com/user-attachments/assets/91d763a2-e7ad-4bd0-8a7f-4ce0f181a8b3)

This enabled me to utilize data validation, where I could implement a dependent dropdown, so that only relevant values would show based on the generation selected. I accomplished this with the INDIRECT function, which references any lists that use the selected name. In this case, 'Gen1_' is selected, so the Pokémon available in the Pokémon Name dropdown will be exclusive to Generation 1. Neat!

![image](https://github.com/user-attachments/assets/6bf2781e-9851-4f92-ad34-42e76c68b5dd)

Lastly, the radar chart. This is a tool used in-game to compare a Pokémon's stat distribution, allowing for a easy method of assessing a Pokémon's strengths and weaknesses. In this example, we see Pikachu's stat distribution, and notice that it is a rather speedy Pokemon in particular:

![image](https://github.com/user-attachments/assets/953d0482-12a9-4c68-b4bc-cb3e88f54944)

To appreciate a Pokémon's stats even more, comparing it to another is a great strategy. Here, we compare Pikachu with its evolved form, Raichu. Here, we can see that while Pikachu is a fast Pokémon, Raichu is not only faster, but has a much higher base Attack and Special Attack stat:

![image](https://github.com/user-attachments/assets/a7bbaf32-ab13-415b-808e-70be46762b0c)

Overall, this was a really fun project and I was glad to have completed it. I think I took a unique approach, by not only including the lookup function, but also including the dynamic image search and the radar chart. 



### Question 1: Which type is the most/least common? How many pokemon are associated with each?

Pokémon can be either single or dual type (i.e., two different types are associated with the Pokémon). For example, the fan-favorite Pokémon Pikachu is a single-type (Electric), whereas Charizard is a dual-type (Fire-Flying). Across 6 generations, the most common Pokémon type is Water (120). The least common is Fairy (35). This was solved via an array using COUNTIF. After combining columns C & D via the CONCAT function in Column F, I used the COUNTIF function to return instances where each type occurred in Column F. This was necessary, as a standard pivot table won't recognize that a type may appear in either column: 

![image](https://github.com/user-attachments/assets/2366b372-204f-41d7-acb0-58e2c35feecc)



### Question 2: What are the top-10 strongest Pokémon?

Pokémon strength is determined by the sum of its individual attributes (i.e., Attack + Defense + HP + Speed + Special Attack + Special Defense). The top 5 are:
  1. Arceus, (720)
  2. Kyurem- Black, (700)
  3. Kyurem- White, (700)
  4. Palkia, (680) (there are 12 other Pokemon with a stat total of 680)

![image](https://github.com/user-attachments/assets/ba988be7-4013-4091-beb6-38879fe45f6d)

**I hereby confirm that all the work presented here is entirely my own, and no unauthorized assistance was used in its completion.**


