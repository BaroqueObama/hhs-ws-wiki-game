# HHS CS Workshop: Wikipedia Game with BFS
Learn Breadth-First-Search (BFS) through a program that plays the Wikipedia game.  
The [Wikipedia game](https://en.wikipedia.org/wiki/Wikipedia:Wiki_Game) involves trying to navigate from a "start" Wikipedia page to a "goal" Wikipedia page by traversing pages through clicking wikilinks. Fastest wins.  
The code prompts the user for the starting and ending Wikipedia page. It then attempts to find a path between those two pages using BFS.  
## Code:
### WikiGame Class
- Begins with start link/topic and goal link/topic.
- Iterate BFS:
  - Use BS4 to get a list of wikilink topics from Wikipedia page.
  - If the goal topic isn't found:
    - Picks the first `n` topics in the list.
    - Adds those topics to the queue to search through.
    - Adds the topic that was searched in a list of visited topics.
    - Picks the next topic from the queue to search through. 
  - If goal topic is found:
    - Return path from start to goal topic.
## Example:
**User Input:**
```
What is the start link?: https://en.wikipedia.org/wiki/Macadamia
What is the goal link?: https://en.wikipedia.org/wiki/Computer_science
```
**Output:**
```
Search Started
-1 From Macadamia, searching through: Macadamia
0 From Macadamia, searching through: Genus
0 From Macadamia, searching through: Species
0 From Macadamia, searching through: Flowering_plant
0 From Macadamia, searching through: Proteaceae
0 From Macadamia, searching through: New_South_Wales
0 From Macadamia, searching through: Queensland
0 From Macadamia, searching through: Help:IPA/English
0 From Macadamia, searching through: Bush_tucker
0 From Macadamia, searching through: Aboriginal_Australians
1 From Genus, searching through: Taxonomic_rank
1 From Genus, searching through: Biological_classification
1 From Genus, searching through: Extant_taxon
1 From Genus, searching through: Fossil
1 From Genus, searching through: Virus_classification#ICTV_classification
1 From Genus, searching through: Family_(taxonomy)
1 From Genus, searching through: Binomial_nomenclature
2 From Species, searching through: Organism
2 From Species, searching through: Sex
2 From Species, searching through: Mating_type
2 From Species, searching through: Reproduction
2 From Species, searching through: Fertility
2 From Species, searching through: Offspring
2 From Species, searching through: Sexual_reproduction
2 From Species, searching through: Taxonomy_(biology)
2 From Species, searching through: Biodiversity
3 From Flowering_plant, searching through: Basal_angiosperms
3 From Flowering_plant, searching through: Core_angiosperms
3 From Flowering_plant, searching through: Plant
3 From Flowering_plant, searching through: Flowers
3 From Flowering_plant, searching through: Fruit
3 From Flowering_plant, searching through: Forb
3 From Flowering_plant, searching through: Grass
3 From Flowering_plant, searching through: Broad-leaved_tree
3 From Flowering_plant, searching through: Shrub
4 From Proteaceae, searching through: Family_(biology)
4 From Proteaceae, searching through: Southern_Hemisphere
4 From Proteaceae, searching through: Australia
4 From Proteaceae, searching through: South_Africa
4 From Proteaceae, searching through: Platanaceae
4 From Proteaceae, searching through: Nelumbonaceae
5 From New_South_Wales, searching through: States_and_territories_of_Australia
5 From New_South_Wales, searching through: Eastern_states_of_Australia
5 From New_South_Wales, searching through: Victoria_(state)
5 From New_South_Wales, searching through: South_Australia
5 From New_South_Wales, searching through: Coral_Sea
5 From New_South_Wales, searching through: Tasman_Sea
5 From New_South_Wales, searching through: Australian_Capital_Territory
5 From New_South_Wales, searching through: Jervis_Bay_Territory
6 From Queensland, searching through: Help:Pronunciation_respelling_key
6 From Queensland, searching through: Northern_Territory
6 From Queensland, searching through: Pacific_Ocean
6 From Queensland, searching through: Torres_Strait
7 From Help:IPA/English, searching through: International_Phonetic_Alphabet
7 From Help:IPA/English, searching through: Template:IPAc-en
7 From Help:IPA/English, searching through: Help:IPA
7 From Help:IPA/English, searching through: English_orthography#Sound-to-spelling_correspondences
7 From Help:IPA/English, searching through: English_orthography#Spelling-to-sound_correspondences
7 From Help:IPA/English, searching through: Cot%E2%80%93caught_merger
7 From Help:IPA/English, searching through: English_phonology
7 From Help:IPA/English, searching through: International_Phonetic_Alphabet_chart_for_English_dialects
7 From Help:IPA/English, searching through: Diaphoneme
7 From Help:IPA/English, searching through: General_American
8 From Bush_tucker, searching through: Indigenous_Australians
8 From Bush_tucker, searching through: Torres_Strait_Islander
8 From Bush_tucker, searching through: Kangaroo_meat
8 From Bush_tucker, searching through: Emu
8 From Bush_tucker, searching through: Witchetty_grubs
8 From Bush_tucker, searching through: Crocodile
8 From Bush_tucker, searching through: Santalum_acuminatum
8 From Bush_tucker, searching through: Solanum_centrale
9 From Aboriginal_Australians, searching through: Indigenous_peoples
9 From Aboriginal_Australians, searching through: Mainland_Australia
9 From Aboriginal_Australians, searching through: Torres_Strait_Islands
9 From Aboriginal_Australians, searching through: Australia_(continent)
9 From Aboriginal_Australians, searching through: List_of_Aboriginal_Australian_group_names
9 From Aboriginal_Australians, searching through: Australian_Aboriginal_identity
9 From Aboriginal_Australians, searching through: Australian_Aboriginal_languages
9 From Aboriginal_Australians, searching through: Wikipedia:Vagueness
10 From Taxonomic_rank, searching through: Biology
10 From Taxonomic_rank, searching through: Taxon
10 From Taxonomic_rank, searching through: Hierarchy

Path Found:
Macadamia
Genus
Taxonomic_rank
Hierarchy
Computer_science

Time taken: 76.51 seconds
```