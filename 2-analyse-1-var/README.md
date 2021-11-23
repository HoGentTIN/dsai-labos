# Labo's module 2: Analyse van één variabele

## Labo 2.1 - Australian Athletes (ais)

1. Maak een nieuw Jupyter Notebook bestand aan en laad de AIS dataset. Neem hiervoor de code over van labo 1.1, incl. het instellen van de index en het omzetten naar categorische variabelen.
2. Gebruik een geschikt grafiektype om volgende variabelen te visualiseren. Zijn meerdere grafiektypes geschikt? Maak er één van elk! Merk op hoe sommige grafieken toch een beter inzicht geven over de data dan andere...
   - `sex`
   - `sport`
   - `ht` (toon dit ook eens opgesplitst volgens `sex` en volgens `sport`)
3. Selecteer volgende deelverzamelingen in de dataset en bereken voor elk de geschikte centrum- (en desgevallend spreidings-)maten van de variabelen `ht` en `sex`:
   1. de roeiers
   2. de roeiers, netballers en tenissers samen
   3. de vrouwelijke basketballers en roeiers samen

Ter controle vind je hier de uitkomsten van de laatste vraag. Eerst de frequenties en modus van de variabele `sex`:

|           | Selectie 1 | Selectie 2 | Selectie 3 |
| :-------- | :--------- | :--------- | :--------- |
| **f**     | 22         | 52         | 35         |
| **m**     | 15         | 19         | 0          |
| **modus** | f          | f          | f          |

Vervolgens de relevante centrum- en spreidingsmaten voor `ht` (max. 3 cijfers na de komma):

| Statistiek | Selectie 1 | Selectie 2 | Selectie 3 |
| :--------- | :--------- | :--------- | :--------- |
| gemiddelde | 182.376    | 179.066    | 180.126    |
| stdev      | 7.798      | 7.936      | 7.144      |
| min        | 156        | 156        | 156        |
| Q1         | 179.3      | 174.25     | 177.4      |
| mediaan    | 181.8      | 179.5      | 179.7      |
| Q3         | 186.3      | 183.4      | 184.65     |
| max        | 198        | 198        | 195.9      |
| IQR        | 7          | 9.15       | 7.250      |

## Labo 2.2 - Android Persistence

1. Start eveneens met een nieuw Notebook-bestand voor de Android Persistence dataset. Vergeet het omzetten naar categorische variabelen niet. Definieer een volgorde in geval van een ordinale variabele.
2. Visualiseer de variabelen `DataSize` en `PersistenceType` afzonderlijk a.h.v. een geschikt grafiektype.
3. Hoe vaak komt elke combinatie van `DataSize` en `PersistenceType` voor? Toon de frequenties van `PersistenceType` (parameter `hue`), gegroepeerd volgens `DataSize` (parameter `x`). Probeer het ook omgekeerd!
4. Visualiseer de variabele `Time` met een boxplot, telkens met meer detail. Merk je hoe je op die manier telkens een beter zicht krijgt op de data?
    - Eerst over heel de dataset (parameter `x`)
    - Vervolgens gegroepeerd volgens `DataSize` (parameter `y`)
    - Tenslotte splitsen we verder op volgens `PersistenceType` (parameter `hue`)
5. (Uitdaging) Probeer iets gelijkaardigs te doen met een dichtheidsdiagram: toon voor elke waarde van `DataSize` een spreidingsdiagram waarop voor elke waarde van `PersistenceType` een dichtheidsdiagramm van de variabele `Time` getoond wordt (tip: `sns.FacetGrid()`). Het resultaat kan er ongeveer zo uitzien:

    ![Dichtheidsdiagrammen voor elke `DataSize`, met een vergelijking van de performatie van de verschillende `PersistenceTypes`](img/persistence-density.png)

6. Bereken gemiddelde en standaardafwijking voor `Time`.

    - Over de hele dataset
    - Opgesplitst volgens `DataSize`
    - Opgesplitst volgens `PersistenceType`
    - Opgesplitst volgens `DataSize` én `PersistenceType`

Ter controle vind je hier de verwachte uitkomsten (max. 3 cijfers na de komma):

| Statistiek        | Gemiddelde | Standaardafwijking |
| :---------------- | :--------- | :----------------- |
| Hele dataset      | 6.231      | 4.230              |
| Small             | 1.741      | 0.359              |
| Medium            | 7.022      | 1.864              |
| Large             | 11.426     | 1.164              |
| GreenDAO          | 7.152      | 4.386              |
| Realm             | 6.023      | 3.884              |
| SQLite            | 7.036      | 4.146              |
| SharedPreferences | 1.674      | 0.285              |

Opgesplitst op de beide criteria:

| Gemiddelde            | Small | Medium | Large  |
| :-------------------- | :---- | :----- | :----- |
| **GreenDAO**          | 1.894 | 7.454  | 12.110 |
| **Realm**             | 1.599 | 5.818  | 10.652 |
| **SQLite**            | 1.799 | 7.794  | 11.515 |
| **SharedPreferences** | 1.674 | -      | -      |

| Standaardafwijking    | Small | Medium | Large |
| :-------------------- | :---- | :----- | :---- |
| **GreenDAO**          | 0.348 | 2.007  | 0.868 |
| **Realm**             | 0.315 | 1.331  | 1.406 |
| **SQLite**            | 0.416 | 1.599  | 0.559 |
| **SharedPreferences** | 0.285 | -      | -     |
