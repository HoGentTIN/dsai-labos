# Labo's hoofdstuk 1: Basisbegrippen, steekproefonderzoek

## Labo 1 - Australian Athletes (ais)

1. Maak een Jupyter Notebook-bestand `labo-1-01.ipynb` aan in deze directory.
2. Zorg dat de eerste cel een Markdown cel wordt, en geef het een titel (bv. `# Labo 1.1`).
3. Voeg een Python-cel toe en kopieer alle imports die je nodig hebt voor data-analyse uit de codevoorbeelden (Numpy, Pandas, enz.) naar die cel.
4. Voeg een nieuwe Python cel toe en laad het CSV-bestand `data/ais.csv` in een variabele `ais`. Deze dataset bevat 202 observaties van Australische atleten met allerlei bloedwaarden. Het codeboek (d.w.z. de uitleg van wat elke variabele/kolom in de dataset betekent) vind je in [data/ais.md](/data/ais.md). Toon de eerste observaties van deze steekproef.
5. Vraag algemene info op over deze dataset:
    - Hoeveel rijen en kolommen heeft de dataset?
    - Toon algemene info over elke variabele, meer bepaald aantal lege velden en het type van elke variabele (bv. int64, float64, object)
    - Hoeveel kolommen van elk type zijn er?
    - Wat is het meetniveau (nominaal, ordinaal, interval, ratio) van elke variabele?
6. De kolom "id" is eigenlijk geen variabele, maar een index. Markeer deze als dusdanig.
7. De variabelen die nu als "object" beschouwd worden, zijn kwalitatieve variabelen. Wijzig het type van elk van deze variabelen in "category". Controleer of de omzetting gelukt is door opnieuw info over de types op te vragen.
8. Geef een beschrijving van de kolommen ferr, bmi, sex en sport en de unieke waarden in elk. Herken je de kenmerken van kwalitatieve en kwantitatieve variabelen in het resultaat?
9. Selecteer volgende elementen uit de dataset:
    - de tweede rij (id = 2)
    - rijen 4 t/m 6 (id's = 5 t/m 7)
    - kolommen 6 t/m 8 ("ferr","bmi","ssf")
    - de variabele "pcBfat" (op naam!). Er zijn meerdere manieren om deze op te vragen!
    - alle observaties voor de sport "Netball"
    - enkel de variabele "wt" van de observaties voor "Netball"
    - welke sporten worden beoefend door atleten met een BMI hoger dan 26? Geef ook een lijst met de unieke waarden en een frequentietabel van hoe vaak elke sport voorkomt.