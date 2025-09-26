Q1: How big is the dataset?
Ans: 36860 number of lines, 4.6M
Command: wc -l clean_dialog.csv
du -h clean_dialog.csv

Q2: What’s the structure of the data? (i.e., what are the field and what are values in them)
Ans: "title": String
"writer": String
"pony": String
"dialog": String
Command: head -5 clean_dialog.csv
head -1 clean_dialog.csv | tr ',' '\n'

Q3: How many episodes does it cover?
Ans: 25458
Command: cut -d',' -f4 clean_dialog.csv | sort -u | wc -l

Q4: During the exploration phase, find at least one aspect of the dataset that is unexpected meaning that it seems like it could create issues for later analysis
Ans: Found unexpected speaker names. Example: 3"
 Charlotte Fullerton & Betsy McGowen"
 Chris ""Doc"" Wyatt
 Joanna Lewis
 Kevin Burke & Chris ""Doc"" Wyatt"
 M. A. Larson
 Michael P. Fox & Wil Fox"
 Rita Hsiao
"A. K. Yearling"
"A.K. Yearling"
"Ace Point"
"Ahuizotl"
"Alice"
"All Discords"
"All Pegasi"
"All but Rainbow Dash"
"All but Rarity"
"All but Yona"
"All except Fluttershy"
"All except Rarity"
Command: cut -d',' -f3 clean_dialog.csv | sort -u | head -20