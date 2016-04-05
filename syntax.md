Syntax
============

This document describes the syntax of the Azzaral language, in Extended
Backus-Naur form.

# Sentence
The basic building block of the language, a sentence is a set of expressions,
linked logically using "connectors".

```
sentence = expression, {connector, expression};
```

The full list of connectors in the language is available in
[dictionary/misc#connectors](dictionary/misc.md#connectors)

# Expression
An expression in Azzaral is the most important block in the language, used to
describe an action or a state.

```
expression = verb, {flag}, subject, {subject};
```

The verb (full list in [dictionary/verbs](dictionary/verbs.md)) is the first element of the
expression as it will determine its meaning. It can be folowed by a list of
markers (full list in [dictionary/misc#markers](dictionary/misc.md#markers)) used to convey additional
informations about the whole expression. Finally, one or more subject define the
context of the verb (the number of subjects and the way they are linked is
completely dependant on the verb).

# Subject
A subject is a very generic structure as it can be used to describe a very broad
variety of "things", such as a person or an object.

```
subject = noun, {adjective}
noun = proper noun | common noun | pronoun
```

A subject is primaryly adressed by a noun, proper or common, or a pronoun
(full list of common nouns in [dictionary/nouns](dictionary/nouns.md), pronouns in
[dictionary/misc#pronouns](dictionary/misc.md#pronouns)). This noun can be completed with a set of
adjectives (full list in [dictionary/adjectives](dictionary/adjectives.md)).
