---
layout: relation
title: 'xcomp'
shortdef: 'open clausal complement'
---

An open clausal complement (`xcomp`) of a verb or an adjective is a
predicative or clausal complement without its own subject. The
reference of the subject is necessarily determined by an argument
external to the xcomp (normally by the subject of the next higher
clause). This is often referred to as *obligatory control*. 
These complements are always non-finite, and they are
complements (arguments of the higher verb or adjective) rather than
adjuncts/modifiers, such as a purpose clause. The name `xcomp` is
borrowed from Lexical-Functional Grammar.

~~~ sdparse
Хочешь плавать ? \n Do-you-want to-swim ?
xcomp(Хочешь, плавать)
xcomp(Do-you-want, to-swim)
~~~

~~~ sdparse
Я начал там работать вчера . \n I have-started to-work there yesterday .
xcomp(начал, работать)
xcomp(started, to-work)
~~~

Note that the above condition “without its own subject” does not mean that a 
clause is an `xcomp` just because its subject is not _overt._
The subject must be necessarily inherited from a fixed position in the higher clause.
That is, there should be no available interpretation where the subject of the lower clause may be distinct
from the specified role of the upper clause.
In cases where the missing subject may or must be distinct from a fixed role in the higher clause,
[ccomp]() should be used instead, as below.  This includes cases of arbitrary subjects and anaphoric control.

~~~ sdparse
Начальник приказал выкопать ров . \n Boss ordered to-dig ditch .
ccomp(приказал, выкопать)
ccomp(ordered, to-dig)
~~~

Pro-drop languages have clauses where the subject is not present as a separate word,
yet it is inherently present (and often deducible from the form of the verb)
and it does not depend on arguments from a higher clause.
Thus in neither of the following two Russian examples is there any overt subject,
yet only the second example contains an `xcomp`.

~~~ sdparse
Пишу , потому что я это обещал . \n I-write , because I-have promised it .
advcl(Пишу, обещал)
advcl(I-write, promised)
~~~

~~~ sdparse
Я обещал писать . \n I have-promised to-write .
xcomp(обещал, писать)
xcomp(have-promised, to-write)
~~~
