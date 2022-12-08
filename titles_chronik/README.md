
# Titles Extraction

## Description

`titles.ipynb` extracts titles from annotations made as a part of Digital Edition Jahresberichte project 
by Aron Marquart.  `ParsedSemanticAnnotations.pickle` in Aron's repository (folder `Data`) contains all entities 
extracted from the Chronik. They are of different types, for example `E7 Activity`, `E21 Person`.

First `titles.ipynb` extracts entities whose class is `E21 Person` and tokenizes them. 
Then it implements the following strategy to filter out people's names:

For every token except the last one (the last token is usually a surname):
1. Check if a token contains only 2 characters and one of them is a dot -> it's likely to be an abbreviation of a name.
2. If a tokens occurs in the list of names -> it's very likely to be a name.

Otherwise the token is considered to be a title. 
At the end program saves extracted titles in `titles.txt`.



The program implements the naive way to extract possible titles without having to check every word.
Therefore there are false positives besides real titles. False positives are strings that were mistakenly identified
as titles. Some of them are names, names of relations in a family, appellations, etc. 
Such result were not removed because of the aim was see how well the
following naive algorithm works on the given type of data.


## Structure
Jupyter notebook `titles.ipynb` contains code to extract titles from the entities. 

File `titles.txt` is a generated file that contains all titles extracted from the chronik.

File `MaleGivenNames.txt` contains all male names.
 

# Requirements
`python3.7`
`nltk`
`pickle`

# Usage
To be able to run the code it is necessary to change the path to the files in `titles.ipynb`
and make sure
you have `ParseUIMAXMI.py` and `SemanticMOdels.py` from Aron's repository (folder `Data`)
in the same folder as these files.



 



## Contact
Olha Svezhentseva <Olha.Svezhentseva@mfn.berlin>

