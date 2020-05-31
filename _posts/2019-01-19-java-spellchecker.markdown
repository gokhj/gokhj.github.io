---
layout: post
title:  "Implementing a Spellchecker on Java"
date:   2019-01-19 12:00:00 +0000
categories: projects
---

[GitHub Repo](https://github.com/gokhj/Java-Spellchecker)

This is a spell checker application implemented on Java.

I also implemented SoundEx and Levenshtein algorithms for word processing.

``Spellchecker.java`` class includes both SoundEx and Levenshtein algorithms for the user.

SoundEx Algorithm can be inspected at ``lines 108-171``.

Levenshtein Algorithm can be seen at ``lines 180-217``.

``SpellcheckerSuggestion.java`` class on the other hand is fairly shorter but extends ``Spellchecker`` to work, that means it's a more advanced version. It mainly uses the SoundEx Algorithm to match the words inside the dictionary file.

The user can change the edit distance (Levenshtein) on the ``line 52``. The default distance is 2, and increasing it will get the user more suggestions.