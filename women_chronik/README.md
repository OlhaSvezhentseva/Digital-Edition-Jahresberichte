
# Female Names Extraction

## Description

`women_chronik.ipynb` extracts female names from annotations made as a part of Digital Edition Jahresberichte project 
by Aron Marquart.  `ParsedSemanticAnnotations.pickle` in Aron's repository (folder `Data`) contains all entities 
extracted from the Chronik. They are of different types, for example `E7 Activity`, `E21 Person`.

`women_chronik.ipynb` extracts entities whose class is `E21 Person` and checks if it is a female name.
To do so it either finds "Frau", "Fräulein" or "Schwester" in the entity string or finds a female name.
For that the list of all female names is used. At the end program saves extracted names in `extracted_names.txt`.
The last line contains a total number of names extracted.

## Structure
Jupyter notebook `women_chronik.ipynb` contains code to extract female names from the entities. 

File `all_female_names.txt` contains all female names.

File `extracted_names.txt` contains female names extracted from the chronik.
 

# Requirements
`python3.7`
`nltk`
`pickle`

# Usage
To be able to run the code it is necessary to change the path to the files in `women_chronik.ipynb` and make sure
you have `ParseUIMAXMI.py` and `SemanticMOdels.py` from Aron's repository (folder `Data`) in the same folder as these files.



 



## Contact
Olha Svezhentseva <Olha.Svezhentseva@mfn.berlin>

