Title: Alle gegenderten Formen (und wie man sie automatisiert entfernen kann)
Date: 2022-11-11 16:14
Category: German articles
Tags: Gendersprache, NLP

Unter einigen Parteien wird es immer mehr zur Mode, gegenderte Sprache zu verwenden. Die Mehrheit der Bevölkerung ist kein Fan davon, allerdings wird man mitunter an Universitäten abgestraft, wenn man sich verweigert. 

Es gibt allerdings mittlerweile Erweiterungen, die gegenderte Sprache vollkommen entfernen, darunter "Binnen-I-Be-Gone", dessen Entwickler aber anscheinend nicht den Quellcode seiner Extension teilen möchte - sehr ärgerlich - und "No Gender" - eine Open-Source-Alternative mit Code auf Github und offener Lizenz, dessen Maintainer allerdings auch seit 9 Monaten inaktiv zu sein scheint. Taugen die etwas? Wir werden sehen.


| Syntax      | Ungegenderte Form  | Kommentar    |
| ----------- | -----------| ----------- |
| Der Sänger oder die Sängerin |  Der Sänger | In seltenen Fällen ist eine Doppelnennung für den Kontext wichtig. |
| Der Arbeiter oder die Arbeiterin |  Der Arbeiter |  |
| Liebe Mitarbeiter und Mitarbeiterinnen   | Liebe Mitarbeiter        | Hier kann bedenkenlos die gegenderte Form entfernt werden   |
| Liebe Sänger und Sängerinnen   | Liebe Sänger        |     |
| Die Lehrenden | Die Lehrer | |
| Die Studierenden | Die Studenten | |
| Die Mitarbeitenden | Die Mitarbeiter | |
| Die LeserInnen | Die Leser | Hier bräuchte man eine grammatikalische Analyse, um die richtige Grundform zu finden |
| Den LeserInnen ist es unangenehm| Den Lesern ist es unangenehm | Hier begeht leider das "No Gender"-Addon einen grammatikalischen Fehler|
| Die Lehrerinnen und Lehrer | Die Lehrerinnen und Lehrer | |
| Den Lehrerinnen und Lehrern | Den Lehrerinnen und Lehrern ||
| einx gutx Lehrx | ein guter Lehrer oder eines guten Lehrers | Hier müsste man die Grammatik des Grundsatzes sehr gut kennen, um auf die ungegenderte Form zu kommen. |
| alle Lehrys | alle Lehrer | klingt nicht lächerlich |
| mehrere Lehrer\*innen| mehrere Lehrer | |
| Wenn ein\*e Lehrer\*in | Wenn ein Lehrer | |
| die Lehrer_innen | die Lehrer | |
| ein_e Lehrer_in  | ein Lehrer | Wie dekliniert man das? |
| zwei Lehrer·innen | zwei Lehrer | |
| ein·e Lehrer·in | ein Lehrer ||
| den Mitarbeiter/-innen ist es ein Dorn im ... | den Mitarbeitern ist es ein Dorn im ... ||
| die Mitarbeiter/-innen | die Mitarbeiter ||
| viele Mitarbeiter*innen | viele Mitarbeiter ||
| Lehrer(innen) | Lehrer| Kann man unproblematisch entfernen, ohne auf Grammatik zu achten|
| Ein(e) Lehrer(in)| Ein Lehrer ||
| Die Kolleg(inn)en | Die Kollegen ||
| einE LehrerIn | ein Lehrer ||
| ein/e LehrerIn | ein Lehrer ||
| eine Lehrerin beziehungsweise ein Lehrer | ein Lehrer | |

(Hier muss ich noch mehr einfügen, der relevante Wikipediaartikel ist gefühlt so lang wie ein halbes Buch.)

Wenn man diese Website jeweils mit Binnen-I-Be-Gone und "No Gender" aufruft, scheint Binnen-I-Be-Gone ein besseres Bild abzugeben und fast alle eindeutigen Fälle zu erwischen, es zieht in vielen Fällen sogar die Grammatik in Betracht. Allerdings gibt es auch Websites, auf denen "No Gender" bessere Ergebnise zeigt, beispielsweise auf Reddit erkennt es Felder, wo Binnen-I versagt.

Was sich hier zeigt: Eine richtige Gendersprache-Entfernung ist kompliziert: Binnen-I-be-Gone enthält 600+ Zeilen sehr komplizierten Regex-Code, der anscheinend auch grammatikalische Konstrukte berücksichtigt. Die Open-Source-Alternative ist noch nicht zu 100 Prozent so ausgereift.

Sehr schwer zu erkennen bleibt das generische Femininum, abwechselndes Gendern, das Verwenden von Passivformen, wenig sinnvolle Relativsätze oder allgemeine ungelenke Umformulierungen. Da könnte die neueste Version von OpenAIs GPT-Modellen Abhilfe schaffen. Es wird jedoch noch lange dauern, bis es praktikabel ist, jeden Text, den man liest, durch die OpenAI-Server zu jagen. Momentan kostet ein längerer Zeitungsartikel einige Cent und hat eine riesige Latenz. Aber für Bücher könnte es in naher Zukunft schon realistisch sein.