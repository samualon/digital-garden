## Onderdelen
1. **Drum**: het knelpunt prioritair plannen.
	- "Geeft het ritme aan"
2. **[[Rope]]**: het vrijgeven van materiaal aan machines die geen knelpunt vormen volgens het ritme van de drum.
3. **Buffer**: het knelpunt of assemblagepunt beschermen met veiligheidsvoorraden.

## Heuristiek
1. Nog geen rekening houden met capaciteitsbeperkingen.
2. Per order [[Due date]] - [[Shipping rope]] = moment waarop product moet klaar zijn.
3. Overlappende orders die boven capaciteit zijn verschuiven tot alles onder de capaciteitsbeperking ligt. Soorteer de orders op volgende prioriteit:
	1. Earliest due date
	2. Shortest processing time

## Methoden voor andere beslissingen
In de heuristische methode zijn due dates en orders gegeven, maar vaak moeten we nog andere berekeningen doen. Hierbij kunnen we volgende twee methoden gebruiken:
1. [[Productmixbeslissingen]]
2. (Ordergroottebeslissingen / -beperkingen)