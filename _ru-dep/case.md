---
layout: relation
title: 'case'
shortdef: 'case marking'
---

Russian uses a combination of oblique morphological cases and prepositions to express semantic case.
Prepositions in UD are treated as dependents of the noun they attach to. The relation between the noun and the preposition is labeled `case`.

~~~ sdparse
В пятницу.Acc по дороге к деревне.Dat мы разговаривали о событии.Loc . \n On Friday during-the-journey to the village we-have-talked about the event .
case(пятницу.Acc, В)
case(Friday, On)
case(деревне.Dat, к)
case(village, to)
case(событии.Loc, o)
case(event, about)
~~~
