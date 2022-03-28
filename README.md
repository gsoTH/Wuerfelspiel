<!--
[![Build and Tests](https://github.com/gsoTH/Wuerfelspiel/actions/workflows/build-and-test.yml/badge.svg?branch=master)](https://github.com/gsoTH/Wuerfelspiel/actions/workflows/build-and-test.yml)
-->
#### Ziele/Kompetenzen :seedling:
- Objektorientierte Analyse und Modellierung üben (UML-Klassendiagramme erstellen)
- Testgetriebene Entwicklung (UnitTests)
- Vorhandene Klassen wiederverwenden (Vererbung einsetzen, z.B. Spezialwürfel einbauen)
- Wiederverwendbare GUI-Elemente einsetzen (UserControls)
- Verknüpfung zwischen GUI-Elementen und anderen Klassen.
___

# Wuerfelspiel
![Kniffel](https://i.pinimg.com/236x/47/cc/5e/47cc5e1c3d139196e10c98fc81727561.jpg)

## Anforderungen :dart: 
In diesem Repository soll ein Würfelspiel entwickelt werden, das diesen Anforderungen genügt;
1. Es soll das Spiel [Kniffel](https://de.wikipedia.org/wiki/Kniffel) nachgebaut werden. Mindestanforderung ist der sogenannte [obere Block](https://de.wikipedia.org/wiki/Kniffel#Oberer_Block) inkl. einer Zwischensumme, auf die unter Umständen ein Bonus aufgeschlagen wird. Zwischensumme + Bonus ergibt die Summe des oberen Blocks.
2. Die entwickelte Spiellogig soll in Konsolen-Programmen und in Windows-Forms-Programmen genutzt werden können. Das bedeutet, dass die Logik in eigenen Klassen, nicht innerhalb z.B. der Programm.cs oder Form1.cs liegt. In der Programm.cs bzw. Form1.cs soll die Spiellogik nur eingebunden werden.
3. Alle Klassen sollen so aufgebaut sein, dass das Programm erweiterungsfähig ist, so dass ein ähnliches Spiel wie [Balut](https://de.wikipedia.org/wiki/Balut_(W%C3%BCrfelspiel)#Spielregeln) leicht umgesetzt werden kann. 

### Abgrenzungen :no_entry:
- Vorerst nur die wichtigsten Würfel umsetzen: W6, W8, W10, W12, W20. Keine Bildwürfel (:hearts:, :clubs:, :diamonds:, :spades:, :pineapple: o.ä.)


## Fachliche Beschreibungen :memo:
- Kniffel ist ein Würfelspiel mit fünf Würfeln, einem Würfelbecher und einem speziellen Spielblock.
- Würfel haben eine unterschiedliche Anzahl an Seiten (w). Falls keine Zahl angegeben wird, geht man von einem W6 aus.
- Einen Würfel kann man würfeln, wodurch eine zufälliger Wert erzeugt wird. Das Ergebnis des letzten Wurfes muss abgefragt werden können, ohne es automatisch neu zu würfeln. Für viele Spiele kann man Würfel "sichern", wodurch sie beim nächsten Wurf nicht mit berücksichtigt werden (bspw. bei Kniffel).
- Für einige Spiele ist es wichtig, den Wert der genau unten liegenden Seite zu kennen, weil diese verwendet werden darf. Bei einem W6 ist z.B. die 2 gegenüber von der 5. Wenn also eine 5 gewürfelt wurde, muss die 2 als "Gegenwert" auch abgefragt werden können.


## Würfel :game_die:
Jeder kennt die Würfel, die für Spiele wie Kniffel oder Monopoly verwendet werden. Sie besitzen 6 Seiten, die mit einem bis sechs Punkten markiert sind. Die ältesten solcher Würfel sind über 5000 Jahre alt. Sie sind so populär, dass sie sogar als ASCII-Zeichen vorhanden sind: ⚀⚁⚂⚃⚄⚅

Profi-Brettspieler nennen solche Würfel "W6". W steht für Würfel, 6 für die Seitenzahl. Es gibt aber auch Würfel mit anderen Seitenzahlen: W8, W10, W12 und W20 sind die bekanntesten. Es gibt aber auch asymetrische Würfel wie den W7 und welche mit besonders vielen Seiten, wie z.B. einen W100 (angeblich beliebt bei Lehrern, die ihre Noten mit Prozentwerten berechnen). 
Außerdem gibt es Würfel, die Bilder, Symbole oder Farben auf ihren Seiten tragen.

[Eine ziemlich lange Liste an Würfeln findet man auf der Wikipedia](https://de.wikipedia.org/wiki/Spielw%C3%BCrfel#Formen).

Würfel können "ideal" sein. Das bedeutet, dass alle Ziffern ähnlich oft geworfen werden. Wenn man 600 Würfe mit einem idealen durchführt, sollte jede Ziffer ungefähr 100 mal vorkommen. Wenn das nicht so ist, gilt der Würfel nicht als ideal,

Je nach Spielart kann es interessant sein, nicht nur die obenliegende Zahl, sondern auch die gegenüberliegende Zahl zu kennen. Für die wichtigsten Würfel sind in der Standardausführung diese "Gegensummen" bekannt.

| W   | ideal? | Σ gegenü. Seiten (Standardwürfel) |
|-----|--------|-----------------------------------|
| W6  | ja     | 7                                 |
| W8  | ja     | 9                                 |
| W10 | ja     | 11 (0 wird als 10 gerechnet)      |
| W12 | ja     | 13                                |
| W20 | ja     | 21                                |

Bei den meisten Würfeln, die gegenüberliegende Seiten haben, lässt sich daraus die Regel ableiten, dass die Summe der gegenüberliegenden Seiten immer n+1 beträgt.



<!---
Platzhalter 
fürs Auskommentieren von Inhalten
-->
