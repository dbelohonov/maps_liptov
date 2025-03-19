# Project Liptov Maps

Work in progress


### !! Code is stored in ../notebooks/maps.ipynb file !!
### !! Maps are stored in result_maps folder !!

### Here I will give a brief explanation of every single map in this project

#### LM_RK_autonomy_binary:
 + This map shows whether more people commute within the municipality limits or outside (this includes all destinations).
 + "binary" is added because only two options exist.
 + Only in four municipalities (Ruzomberok, Liptovsky Mikulas, Demanovska Dolina and Liptovsky Hradok) more people commute within the municipality. *There are 5 polygons because Liptovsky Mikulas has complicated borders.
 + Round markers represent every single municipality in the Liptov region (81) where size depends on amount of people working in the municipality (including locals and commute workers).

#### LM_RK_autonomy:
 + This map shows percentage of workers commuting outside the municipality (this includes all destinations).
 + Lowest proportion of people commuting for a work outside are in Ruzomberok and Liptovsky Mikulas. Low values are also visible in Demanovska Dolina and Liptovsky Hradok.
 + Round markers represent every single municipality in the Liptov region (81).
 + Also it is quite visible that higher proportion rates are in municipalities closer to regional centres (like RK or LM).

#### LM_RK_flows:
 + This maps shows all commute flows in the Liptov region. We are particularly interested in RK and LM comparison, therefore they are highlighted.

#### LM_RK_gravity:
 + We have counted the gravity force for every city using this equation: (number of commutes from this municipality to one centre / whole number of commutes from this municipality *100) / (road distance between municipality and the city)**2 * 10
 + With the exemption of some neighboring villages the gravity forces to any city are not so strong.
 + Interesting is that there are more municipalities with significant gravity force to LM than those to RK.

#### LM_RK_gravity_plot:
 + The purpose of these plots is similar to previous maps. They show decline of gravity force with the distance for Ruzomberok and Liptovsky Mikulas.
 + The decline of this force in RK is much steeper and sharper than in case of LM.

#### LM_RK_most_popular:
 + Map shows the most "popular" destinations for everyday commute from this municipality. Commutes inside municipality aren't counted there.
 + There are actually three centres in Liptov region (Ruzomberok, Liptovsky Mikulas and Liptovsky Hradok).
 + The village in the norther part of region can be considered as an outlier due to its small size and low number of workers.

#### LM_RK_most_popular_all:
 + This is the same map but commutes within municipality limis are taken into consideration.
 + Now, we see much more options, which is indirectly shown on the LM_RK_gravity. Some villages with lighter colors are big enough to attract some big amount of locals.

#### LM_RK_second_popular:
 + Very few villages are highlighted, as we counted only those with significant secondary destination of commute (more than 75% of primary destination). Commutes within villages aren't taken into consideration.






git clone https://github.com/dbelohonov/maps_liptov.git .

## Virtual environment (venv) setting

```bash
python --version
pip --version
python -m venv .venv
pip list
python.exe -m pip install --upgrade pip
pip install poetry
poetry install
```


