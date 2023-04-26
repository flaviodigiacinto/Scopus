# Scopus
This code allow to get information about the articles published by the faculty staff of UCSC (RTDA, RTDB, Ricercatori, Professori di prima e seconda fascia) from Scopus API
1. The excel file ("Ricercatori.xlsx") reports a list of the family names, the given names and the Scopus IDs for all the structured staff of UCSC (medicine faculty), updated to the end of the 2022. Some researchers have more than one Scopus profile associated, due to the automatic process of Scopus profile creation. Thus, the database was manually checked to add multiple profiles IDs and to verify cases of homonymy. However, it could still contains some issues as well as it could still miss some profiles.
2. Once you have donwloaded the xlsx file you have to download and install the pybliometrics tool to simplify the access to the scopus API (https://pypi.org/project/pybliometrics/). Before you can access the Scopus API (even using the pybliometrics package) you need to request and obtain a scopus key, and even with the key the access to the scopus api could be limited to a certain number of requests.
3. You can use the code named main.py to obtain the data for the UCSC faculty members and create an excel file which contains the basic metrics for the peoples in Ricercatori.xlsx file as well as create another excel file which contains a list of all the articles published by the samegroup of researchers 
4. You can generate a pdf with a report of the new publications from the members of the faculty, updating only the new publications which didn't appear before. The program read the publications which were already shared using the file "Articoli_recenti.xlsx" so this MUST BE UPDATED (loading a new version on github) each time a new report is sent. 

The only part of the code which must be modified are the three lines with the paths:
line 182: where the file "Ricercatori.xlsx" is located on your local machine
line 184: where the file "Articoli_recenti.xlsx" is located on your local machine
line 186. where you want to save the pdf report (if not modified it is saved within the current folder)
