---
layout: relation
title: 'nmod'
shortdef: 'nominal modifier'
---

The `nmod` relation is used for nominal modifiers. They depend either
on another noun (group “noun dependents”) or on a predicate (group
“non-core dependents of clausal predicates”).

`nmod` is a [noun](cs-pos/NOUN) (or noun phrase) functioning as a
non-core (oblique) argument or adjunct.
This means that it functionally corresponds to an adverbial when it attaches to a verb, adjective or other adverb.
But when attaching to a noun, it usually corresponds to a non-agreeing attribute in genitive. 

In Czech the `nmod` relation covers only those possessives that are expressed using the genitive [cs-feat/Case]().
If a possessive adjective is used, the relation is labeled [amod]().

~~~ sdparse
карта студента \n card of-the-student
nmod(карта, директора)
nmod(card, of-the-student)
~~~

~~~ sdparse
студенческая карта \n student's card
amod(карта, студенческая)
amod(card, student's)
~~~

~~~ sdparse
его карта \n his card
det(карта, его)
det(card, his)
~~~

`nmod` is also used for temporal nominal modifiers:

~~~ sdparse
Последний раз мы разговаривали зимой. \n Last time we have-talked in-winter .
nmod(разговаривали, зимой)
nmod(have-talked, in-winter)
~~~

## Agreeing attribute of a noun

`nmod` noun phrases attached to nouns are usually in the genitive [cs-feat/Case]() and follow the modified noun.
However, there is also a different kind of `nmod` that precedes the modified noun and agrees with it in case and number.
A typical example is a title attached to a name of a person. The relation is similar to the [name]() relation
that links the first and the last name, but it is not labeled `name` because the title is not part of the name:

~~~ sdparse
российский президент Владимир Владимироваич Путин \n russian president Vladimir Vladimirovich Putin
amod(президент, российский)
amod(president, russian)
nmod(Владимир, президент)
nmod(Vladimir, president)
name(Владимир, Путин)
name(Vladimir, Putin)
name(Владимирович, Владимир)
name(Vladimirovich, Vladimir)
~~~

Note that the same thing can be also expressed using an [apposition](appos).
In the case of apposition, the title follows the modified name and is separated by a punctuation symbol:

~~~ sdparse
Владимир Путин , российский президент
name(Владимир, Путин)
punct(президент, ,-3)
amod(президент, российский)
appos(Путин, президент)
~~~
