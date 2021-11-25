# Labo's module 4 - Analyse van 2 kwalitatieve variabelen

## Labo 4.1 - Invloed van achtergrondmuziek op koopgedrag

Marktonderzoek toont aan dat achtergrondmuziek in een supermarkt invloed kan hebben op het aankoopgedrag van de klanten. In een onderzoek werden drie methoden met elkaar vergeleken: geen muziek, Franse chansons en Italiaanse hits. Telkens werd het aantal verkochte flessen Franse, Italiaanse en andere wijnen geteld (Ryan, et al., 1998).

De onderzoeksdata bevindt zich in het bestand `data/MuziekWijn.csv`.

1. Stel de correcte kruistabel op. Gebruik hiervoor het R-commando table om de frequentietabel te bekomen.
2. Bepaal de marginale totalen.
3. Bepaal de verwachte resultaten.
4. Bereken de χ² teststatistiek.
5. Bereken Cramér’s V. Wat kan je hieruit besluiten?

Visualiseer de dataset:

1. Plot een staafdiagram (bar chart) met de percentages van soorten verkochte wijn wanneer er geen muziek afgespeeld werd.
2. Plot een geclusterd staafdiagram (clustered bar chart) van de dataset
3. Plot een rependiagram (stacked bar chart) van de dataset

Uitkomst van de belangrijkste berekeningen (afgerond tot 3 cijfers na de komma):

- χ² ≈ 18,279
- Cramér’s V ≈ 0,194

## Labo 4.2 - Survey

Laad het databestand `data/survey.csv` in. Het bevat het resultaat van een bevraging bij studenten van een Australische universiteit.

We willen de relatie onderzoeken tussen enkele discrete (nominale of ordinale) variabelen in deze dataset. Voor elke hieronder opgesomde paren, volg deze stappen:

> - Denk eerst eens na welke uitkomst je precies verwacht voor de opgegeven combinatie van variabelen.
> - Stel een frequentietabel op voor de twee variabelen. De (vermoedelijk) onafhankelijkevariabele komt eerst.
> - Plot een grafiek die het verband tussen beide variabelen visualiseert.
> - Als je de grafiek bekijkt, verwacht je dan een eerder hoge of eerder lage waarde voor de $\chi^2$-statistiek? Waarom?
> - Voer de $\chi^2$-toets uit om te bepalen of er een verband is tussen beide variabelen. Bereken de $\chi^2$-statistiek, de kritiege grenswaarde $g$ en de $p$-waarde, telkens voor significantieniveau $\alpha = 0.05$.
> - Moeten we de nulhypothese aanvaarden en verwerpen? Wat betekent dat precies voor het verband tussen de twee variabelen? Formuleer m.a.w. een antwoord op de onderzoeksvraag.
> - Bereken Cramér's V. Kom je tot een gelijkaardige conclusie als bij de $\chi^2$-toets?

De te onderzoeken variabelen:

| Onafhankelijke variabele | Afhankelijke variabele                     |
|:-------------------------|:-------------------------------------------|
| `Exer` (sporten)         | `Smoke` (rookgedrag)                       |
| `Sex` (gender)           | `Smoke`                                    |
| `W.Hnd` (dominante hand) | `Fold` (bovenste hand als je armen kruist) |
| `Sex`                    | `W.Hnd`                                    |

Uitkomsten van de belangrijkste berekeningen (afgerond tot 3 cijfers na de komma):

- `Exer/Smoke`: χ² ≈ 5.489, g ≈ 12.592, p ≈ 0.483
- `W.Hnd/Fold`: χ² ≈ 1.581, g ≈ 5.992, p ≈ 0.454
- `Sex/Smoke`: χ² ≈ 3.554, g ≈ 7.815, p ≈ 0.314
- `Sex/W.Hnd`: χ² ≈ 0.236, g ≈ 3.842, p ≈ 0.627

## Labo 4.2 - Digimeter

Elk jaar voert Imec (voorheen iMinds) een studie uit over het gebruik van digitale technologieën in Vlaanderen, de Digimeter (Vanhaelewyn & De Marez, 2016). In deze oefening zullen we nagaan of de steekproef van de Digimeter 2016 (n = 2164) representatief is voor de bevolking wat betreft de leeftijdscategorieën van de deelnemers.

Je kan de frequentietabellen vinden in volgende databestanden:

- `data/leeftijden-digimeter`: relatieve frequenties van de leeftijd van deelnemers aan de iMec Digimeter 2016 en de Vlaamse bevolking (zoals gerapporteerd in de Digimeter-publicatie)
- `data/leeftijden-bestat-vl.csv`: absolute frequenties voor de verschillende leeftijdscategorieën van de Vlaamse bevolking (Bron: BelStat, <https://bestat.economie.fgov.be/bestat/> , C01.1: Bevolking volgens verblijfplaats (provincie), geslacht, positie in het huishouden (C), burgerlijke staat en leeftijd (B)).

1. De tabel met leeftijdsgegevens van de Vlaamse bevolking als geheel heeft meer categorieën dan deze gebruikt in de Digimeter. Maak een samenvatting zodat je dezelfde categorieën overhoudt dan deze van de Digimeter. Tip: gebruik gerust een rekenblad als je daarmee sneller kan werken dan het in Python te implementeren.
2. Om de goodness-of-fit test te kunnen toepassen hebben we de absolute frequenties nodig van de geobserveerde waarden in de steekproef. Bereken deze.
3. Bereken ook de verwachte percentages ($\pi_i$) voor de populatie als geheel.
4. Voer de goodness-of-fit test uit over de verdeling van leeftijdscategorieën in de steekproef van de Digimeter. Is de steekproef in dit opzicht inderdaad representatief voor de Vlaamse bevolking?

Uitkomst van de belangrijkste berekeningen (afgerond tot 3 cijfers na de komma):

- χ² ≈ 6.700 (df = 6),
- g ≈ 12.592,
- p ≈ 0.350
