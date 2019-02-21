# Script usage and data fix report

## Flow

1. Fork the repo where [gh-pages](https://mikhama.github.io/mentor-dashboard) was deployed.
2. Download [sheets](https://drive.google.com/open?id=1ULj8KjnNNCgUdGunQ1TY00dNbCsqAsHW).
3. Run the script.
4. It will show data-mistmatches to console output. Fix them in sheets and run script again.
5. Commit `dashboard-data.json` file to the repo.
6. Finally you can see mentor dashboard with new data.

## Script Usage
```
Usage: node data-parser.js [options]
       node data-parser.js [-p PATH_TO_PAIRS] [-s PATH_TO_SCORE] [-t PATH_TO_TASKS]

Options:
  -h, --help                    output this text

Use options that are listed below in order to direct path to xlsx files.
When you don't use these options then default paths are used!

  -p, --pairs PATH_TO_PAIRS     default path: './Mentor-students pairs.xlsx'
  -s, --score PATH_TO_SCORE     default path: './Mentor score.xlsx'
  -t, --tasks PATH_TO_TASKS     default path: './Tasks.xlsx'
```

Script analyzes the files `Mentor score.xlsx`, `Mentor-students pairs.xlsx` and `Tasks.xlsx`.
It creates `dashboard-data.json` file, and output to console data mismatches if they have place.

After analyze the data mismatches that have been found was putted in `mistmatches.txt` file.

We need to change some data in xlsx-files by hand.

## Data that was changed

1. In file `Tasks.xlsx`:
  - Task "Presentation" was added.
  - Task "CodeJam "Scoreboard"" was renamed to "Code Jam "Scoreboard""

2. In file `Mentor-students pairs.xlsx`:
  - Student "NataliaSirotko" was added to mentor "Siarhei Prystauka".
  - Student "RemZiQ" was added to mentor "Sergey Maksimuk".
  - Student "Temons" was added to mentor "Sergey Maksimuk".
  - Student "SozonikOleg" was added to mentor "Sergey Maksimuk".
  - Mentor github link (SergeyShatter) was changed to (NaaruSon).
  - Mentor github link (BezakDenis) was changed to (BloodofDen).
  - Mentor "Varvara	Turovets"	with github link (turovets) was added to page "second_name-to_github_account". In column "F" was added github link of related mentor (vinfinit). 

3. In file `Mentor score.xlsx`:
  - Github links (Artsiom-Zhuk) and (mkinitcpio) were swapped together.
  - Github links (Nemkev) and (Shank111) were swapped together.
  - Github links (rolling-scopes-school/aliakseibabko-2018Q3) and (Shutya) were swapped together.
  - Empty github link was changed to (Shutya).
