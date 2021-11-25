# Labo's module 5 - Analyse van kwalitatieve vs kwantitatieve variabelen

## Labo 5.1 - Android Persistence

In de eerste hoofdstukken hebben we de resultaten van performantieme-
tingen voor persistentiemogelijkheden in Android geanalyseerd (Akin, 2016). Er werden experimenten uitgevoerd voor verschillende combinaties van hoeveelheid data (klein, gemiddeld, groot) en persistentietype (GreenDAO, Realm, SharedPreferences, SQLite). Voor elke hoeveelheid data hebben we kunnen bepalen welk persistentietype het beste resultaat gaf.

Nu gaan we uitzoeken of het op het eerste zicht beste persistentietype ook *significant* beter is dan de concurrentie.

Concreet: ga aan de hand van een toets voor twee steekproeven voor elke datahoeveelheid na of het gemiddelde van het best scorende persistentietype significant lager is dan het gemiddelde van enerzijds het tweede beste type.

Kunnen we de conclusie aanhouden dat voor een gegeven datahoeveelheid één persistentietype het beste is, d.w.z. significant beter is dan gelijk welk ander persistentietype?

Resultaten, ter controle:

| Grootte | Beste | 2e beste          | $p$-waarde |
| :------ | :---- | :---------------- | :--------- |
| Small   | Realm | SharedPreferences | 0.170      |
| Medium  | Realm | GreenDAO          | 2.506e-4   |
| Large   | Realm | SQLite            | 1.7e-3     |

## Labo 5.2

Een groot aantal studenten heeft deelgenomen aan een test die in verschillende opeenvolgende sessies werd georganiseerd. Omdat het opstellen van een aparte opgave voor elke sessie praktisch onhaalbaar was, is telkens dezelfde opgave gebruikt. Eigenlijk bestaat er dus het gevaar dat studenten na hun sessie info konden doorspelen aan de groepen die nog moesten komen. De latere groepen hebben dan een voordeel ten opzichte van de eerste. Blijkt dit ook uit de cijfers?

Het bestand `puntenlijst.csv` bevat alle resultaten van de test. Elke groep wordt aangeduid met een letter, in de volgorde van de sessie.

- Dag 1: sessies A, B
- Dag 2: sessies C, D, E
- Dag 3: sessies F, G, H

Sessies A en B zijn doorgegaan op een andere campus, dus er zou kunnen verondersteld worden dat er weinig tot geen communicatie is met de studenten van de andere sessies.

Als er info met succes doorgespeeld werd, dan verwachten we dat de scores van de groepen die later komen significant beter zijn dan de eerste.

**Merk op** dat de omgekeerde redenering niet noodzakelijk geldt: als blijkt dat het resultaat van de latere sessies inderdaad significant beter blijkt, dan betekent dat niet noodzakelijk dat de oorzaak (enkel) het doorspelen van informatie is. Er kunnen ook andere oorzaken zijn (bv. “zwakkere” klasgroepen zijn toevallig eerder geroosterd).

1. Ga op verkenning in de data. Bereken de gepaste centrum- en spreidingsmaten voor de dataset als geheel en voor elke sessie afzonderlijk.
2. Maak een staafgrafiek van de gemiddelde score per sessie. Is dit voldoende om een beeld te vormen van de resultaten? Waarom (niet)? Verbeter de grafiek door “error bars” toe te voegen.
3. Maak een boxplot van de scores opgedeeld per groep. Vergelijk onderling de hieronder opgesomde sessies. Denk je dat er een significant verschil is tussen de resultaten? Wordt ons vermoeden dat er informatie doorgespeeld wordt bevestigd?
4. Ga door middel van een geschikte statistische toets na of de verschillen tussen de hierboven opgesomde groepen ook significant zijn. Kunnen we concluderen dat de latere groepen beter scoren of niet?

**Merk op** dat je deze onderzoeksvraag in de praktijk zou beantwoorden met een ANOVA-test, die echter buiten het bereik van deze cursus valt. Een ANOVA-test kan de vraag beantwoorden of meer dan 3 of meer steekproeven uit eenzelfde verdeling getrokken zijn. Met een t-toets kan je enkel 2 groepen onderling vergelijken.