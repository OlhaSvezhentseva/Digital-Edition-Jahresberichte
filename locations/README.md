
# Linking of locations with wikidata items

## Description

1457 Strings were annotated by Aron Marquart as locations and extracted as a table. The table was not changed and
is represented by the file `chronik_locations_raw.xlsx`.
These locations were to be linked to corresponding Wikidata items resulting in `all_locations_wiki.xlsx`.



# General Guidelines

The aim was to represent the state of the world at the time chronik appeared. 
So, former countries and colonies were linked to corresponding items if possible.
For example "Deutsch-Ost-Africa" was linked to `Q153963` (German East Africa) described as 
"former German posesssion in the African Great Lakes region between 1884–1919".

Besides, the following guidelines can be identified:

1) In case it was not clear whether the name refers to a politic entity such as country 
or to a geophraphical entity, 
geographical entity was preferred (* unless a politic entity was a lot more relevent in the given context).
For example: "Kanarische Inseln" was linked to `Q23988230` (Canary Islands) described
as "archipelago in the Atlantic off the coast of Africa" and not to `Q6088766` (Province of Canary Islands).

2) Sometimes a string could refer to several entities, one of which being city and the other being a country
 as in the case of "Mexico". 
Then the broader meaning was to be preferred. "Mexico" was therefore linked to `Q96` (country) and not
 to `Q1489` (Mexico City). 
 
 
 * In case of the adjective "westindisch" it was linked to `Q669037` (West Indies) and not to
 `Q1151567` (West India) due to the context of colonial time.
 
# Disambiguation

In case of doubt the context was checked with the help of Aron's code. 
For example it was not clear what exactly "Rovuma" referred to. 
It could refer to a ship `Q77321750` or to a river `Q746779`.

Because of the access to the code it was possible to get the name of the document 
and page number to check the context. As it turned out to be "Fische aus dem Rovuma" it was concluded
that "Rovuma" referred to the river and was therefore linked to  `Q746779`.
 


# Issues

1) Some strings did not have a corresponding Wikidata item. When possible, they were linked to broader entities.
For example "südwestaustralisch' was linked to `Q3960` (Australian continent).

2) Some strings contained several names of several locations, as "Britisch- und Portugiesisch- OStafrika".
If possible they were linked with 2 items then.

3) Some strings did not seem to be specific locations as "hiesig" or "verschiedenen Fundorten".

All locations that could not be linked to a corresponding Wikidata item were marked with `-1`. 
The Wikidata item number or -1 is to be found in `Qnumber` column. 


 



## Contact
Olha Svezhentseva <Olha.Svezhentseva@mfn.berlin>

