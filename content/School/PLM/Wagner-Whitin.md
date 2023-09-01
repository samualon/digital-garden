We stellen een graaf op van de verschillende perioden + een eindnode na de laatste periode.
![[Pasted image 20230630165001.png]]

Met $f_n$ : de totale cumulatieve totale kost van periode n naar periode 1.

We beginnen in de laatste periode (periode 8) waarbij we $f_n$ berekenen aan de hand van de laagst mogelijke combinatie van bestelkosten en voorraadkosten en werken zo verder tot $f_1$. 

Per periode $x$ overwegen we te bestellen voor de meest mogelijke perioden (voor periode 6 dus bestellen voor periode 6, 7 en 8), een periode minder dan de meest mogelijke (voor periode 6 dus bestellen voor periode 6 en 7), etc. tot we aan enkel bestellen voor de huidige periode zitten (voor periode 6 dus enkel bestellen voor periode 6).

Voor periode $x => f_x= C_o + C_h * (0 * EH_x + 1 * EH_{x+1} + 2 * EH_{x+2} + ...)$ voor elke overweging. De laagste uitkomst is dan de juiste $f_x$. Deze bestelling kunnen we dan voorstellen als een boog van de periode $x$ over de perioden waarvoor we volgens onze overweging het best bestellen.

Als we aan periode 1 zijn kunnen we dan de bogen volgen om op die manier te concluderen in welke perioden we voor hoeveel perioden moeten bestellen.

