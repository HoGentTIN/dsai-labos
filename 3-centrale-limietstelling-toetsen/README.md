# Labo's module 3 - Kansrekening, de centrale limietstelling, toetsen

## Kansrekening

### Labo 3.1: Kansrekening in de normaalverdeling

Bereken:

1. $P(Z < 1.33)$
2. $P(Z > 1.33)$
3. $P(Z < −1.33)$
4. $P(Z > −1.33)$
5. $P(Z < 0.45)$
6. $P(Z > −1.05)$
7. $P(Z < 0.65)$
8. $P(−0.45 < Z < 1.20)$
9. $P(−1.35 < Z < −0.10)$
10. $P(−2.10 < Z < −0.90)$

### Labo 3.2 - Kansdichtheid plotten

1. Plot de kansdichtheid en cumulatieve waarschijnlijkheidscurve voor een normale verdeling met een gemiddelde $\mu = 2.5$ en $\sigma = 1.5$.
2. Bereken de oppervlakte voor het gebied onder de dichtheidscurve tussen x = 0.5 en x = 4. (Antwoord: 0.750)

### Labo 3.3 - Student-t vs. normale verdeling

Plot de kansdichtheid en cumulatieve waarschijnlijkheidscurve voor een Student t-verdeling met 3 vrijheidsgraden. Teken ook de standaardnormaalverdeling zodat je beide kan vergelijken.

### Labo 3.4 - Theoretische vs reële kansdichtheid

1. Genereer 25 willekeurige getallen verdeeld volgens de standaardnormaalverdeling. Plot een histogram met kansdichteidsfunctie en de theoretische kansdichtheid.
2. Doe hetzelfde voor 250 en 2500 getallen. Zie je hoe de werkelijke kansdichtheid de theoretische benadert naarmate de steekproefgrootte stijgt?

### Labo 3.5 - Cholesterol

Een gezondheidsonderzoek tussen 1988 en 1994 gaf aan dat de gemiddelde cholesterolwaarde bij vrouwen tussen 20 en 29 jaar 183 mg/dl bedroeg, met een standaardafwijking gelijk aan 36. We nemen nu een aselecte steekproef van 81 vrouwen.

1. Plot de kansverdeling van het steekproefgemiddelde $\overline{x}$
2. Wat is de kans dat je een steekproefgemiddelde $\overline{x} < 185$ uitkomt? (Antwoord: ≈69,1%)
3. Bepaal de kans dat $175 < \overline{x} < 185$ (Antwoord: ≈66,9%)
4. Bereken de kans dat $\overline{x} > 190$ (Antwoord: ≈4,0%)

### Labo 3.6

Een aselecte steekproef van 64 stuks wordt getrokken uit een populatie met onbekende verdeling. De verwachting en de standaardafwijking van de populatie zijn wel gekend: $\mu = 20$ en $\sigma = 16$.

1. Plot de kansverdeling van het steekproefgemiddelde.
2. Bereken de z-score voor $\overline{x_1} = 15.5$ (Antwoord: ≈2.28%) en $\overline{x_2} = 23$ (Antwoord: ≈6.68%).
3. Bepaal de kans dat 16 < $\overline{x}$ < 22 (Antwoord: ≈81.9%)

## Betrouwbaarheidsintervallen

### Labo 3.9 - rlanders.csv

Laad de dataset `data/rlanders.csv` en selecteer enkel de variabele `Money`. We veronderstellen dat de waarden uit deze steekproef normaal verdeeld zijn rond een onbekend populatiegemiddelde $\mu$, maar dat de populatiestandaardafwijking wel gekend is, nl. $\sigma = 98$.

1. Bereken een 99%-betrouwbaarheidsinterval voor het populatiegemiddelde.
2. Bereken een 95%-betrouwbaarheidsinterval voor het populatiegemiddelde.
3. Stel dat $\sigma$ onbekend is. Bereken voor dat geval een 95%-betrouwbaarheidsinterval voor het populatiegemiddelde.
4. Stel tenslotte dat de steekproef enkel bestaat uit de eerste 25 observaties uit deze dataset. Bereken een 95%-betrouwbaarheidsinterval voor deze situatie.

### Labo 3.10 - Service Level Agreement

Een webhostingfirma heeft een Service Level Agreement met een klant voor een gegarandeerde uptime van “five nines” (99,999%). Die wordt aan het einde van elk jaar gecontroleerd en als de minimale uptime niet gehaald wordt, moet de hostingfirma een boete betalen.

Om de uptime te meten, voert een monitoringsysteem elke minuut een `HTTP GET /` uit en controleert het resultaat a.h.v. de HTTP return code. In de maand januari is er één enkele HTTP request onsuccesvol geweest.

- Als deze trend zich voortzet, wat is de kans dat de SLA niet gehaald wordt aan het einde van het jaar? Gebruik de formule voor de kansverdeling van een steekproeffractie.
- De gebruikte formule is eigenlijk niet geschikt in dit specifieke geval en geeft een vertekend beeld. Wat zou de reden kunnen zijn?

## Statistische toetsen

### Labo 3.11 - Bindend Studie-advies

Er wordt gezegd dat het invoeren van een bindend studieadvies (BSA) een rendementsverhoging tot gevolg heeft in slaagkans. Voor het invoeren van het BSA was in de studentenpopulatie het gemiddelde aantal behaalde studiepunten per jaar per student gelijk aan 44 met een standaardafwijking van 6,2. Na invoering van het BSA wijst een onderzoek uit onder 72 studenten dat deze een gemiddeld aantal studiepunten haalden van 46,2.

1. Toets of er op basis van deze steekproef een aanwijzing is dat het invoeren van een BSA inderdaad leidt tot een rendementsverhoging. Gebruik methode van kritieke grenswaarde. Gebruik $\alpha$ = 2.5%.
2. Toon hetzelfde aan met de methode van de overschrijdingskans.
3. Geef een interpretatie van wat de betekenis is van $\alpha$ = 2.5%

### Labo 3.12 - Autodealers

Eén van de motieven voor het kiezen van een garage is de inruilprijs voor de oude auto. De importeur van Ford wil graag dat de verschillende dealers een gelijk prijsbeleid voeren. De importeur vindt dat het gemiddelde prijsverschil tussen de dichtstbijzijnde Ford-dealer en de dealer waar men de auto gekocht heeft hoogstens €300 mag bedragen. De veronderstelling is dat als het verschil groter is, potentiële klanten eerder geneigd zullen zijn om bij hun vorige dealer te blijven.
In een steekproef worden volgende verschillen genoteerd:

```text
400, 350, 400, 500, 300, 350, 200,
500, 200, 250, 250, 500, 350, 100
```

Toets of er een reden is om aante nemen dat het gemiddelde prijsverschil in werkelijkheid significant groter is dan €300. Gebruik een significantieniveau van 5%.

### Labo 3.13 - rlanders.csv: revisited

De variabele `Money` stelt een bruto-jaarsalaris voor (×100$). We gaan ervan uit dat deze variabele een gemiddelde μ = 500 heeft en standaardafwijking σ = 98. Als we het steekproefgemiddelde berekenen over de gehele dataset (doe dit zelf!), lijkt dat de veronderstelling te ondersteunen. Maar wat als we naar de mannen en de vrouwen afzonderlijk zouden kijken (variabele `Gender`)?

Gebruik een geschikte statistische toets om de uitspraken hieronder te verifiëren. Gebruik daarbij significantieniveau α = 5%. Bereken telkens de kritieke grenswaarde(n) en de p-waarde.

1. Het gemiddelde jaarsalaris van de mannen lijkt hoger dan de verwachte waarde. Is het ook significant hoger?
2. Het gemiddelde jaarsalaris van de vrouwen lijkt lager. Is het ook significant lager?
3. Bepaal tenslotte het aanvaardingsgebied voor het gemiddelde jaarsalaris over de gehele steekproef (vrouwen en mannen samen) als we zouden willen bepalen of het steekproefgemiddelde significant afwijkt van de verwachte waarde, zonder een uitspraak te doen of die al dan niet hoger of lager ligt.

Antwoorden:

1. Steekproefgemiddelde: $\overline{x}$≈507.535, kritieke grenswaarde: $g$≈511.456, $p$≈0.1396. We mogen de nulhypothese *niet* verwerpen. Het bruto jaarsalaris van de mannen in de steekproef is niet significant hoger dan verwacht.
2. Steekproefgemiddelde: $\overline{x}$≈472.058, kritieke grenswaarde: $g$≈477.646, $p$≈0.0199. We mogen de nulhypothese verwerpen. Het bruto jaarsalaris van de vrouwen in de steekproef is significant lager dan verwacht.
3. Het aanvaardingsgebied is het interval [487.852, 512.148].
