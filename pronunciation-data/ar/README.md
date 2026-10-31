# Arabic vocalized forms (MonVocabulary)

`ar.tsv` lists, for frequent Arabic words, their possible vocalized readings (short vowels, shadda,
sukun and hamza written out), one reading per line, most likely reading first for each unvocalized
spelling. Columns: `form` (vocalized form), `ipa` (always empty: the MonVocabulary app computes the IPA
from the vocalized form with its own rules), `pos` (part of speech, Universal Dependencies tags), `note`
(short English gloss). 63836 lines.

## Source

- Wiktionary, English edition, Arabic entries: https://en.wiktionary.org/
- Extracted with wiktextract (Tatu Ylonen) and published by kaikki.org: https://kaikki.org/dictionary/Arabic/
- File: https://kaikki.org/dictionary/Arabic/kaikki.org-dictionary-Arabic.jsonl.gz
- Version: kaikki.org-dictionary-Arabic.jsonl.gz, extracted 2026-10-25 from the enwiktionary dump of 2026-10-01 (wiktextract f9fe161, 6f96ddf), SHA-256 4922ad59efa8216b5e8a6e3510bf5c0ba4c87ff9e8eb0e23bca96724f755fcc6

## Authors

Wiktionary contributors (en.wiktionary.org), via kaikki.org (wiktextract). The list of authors of each
entry is in the history of its Wiktionary page.

## License

Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0):
https://creativecommons.org/licenses/by-sa/4.0/ . This file is an adaptation of Wiktionary content and is
distributed under the same license. It is provided as is, without warranty of any kind.

## Modifications

- Kept the vocalized forms of headwords, headword lines (plurals, feminines, non-past, verbal nouns),
  inflection tables (declension, conjugation, pronoun-suffixed forms of prepositions and particles such
  as `لَكَ`, `مِنْهُ`, `إِنَّهُ`) and bot-created verb-form pages; dropped everything else (etymologies,
  examples, translations, Wiktionary IPA). Removed extraction artifacts from headwords (trailing tatweel
  of `لِـ`, `بِـ`; an `Audio:` label).
- Added possessive forms of nouns, derived from their nominative construct forms (`صَدِيقُ` →
  `صَدِيقِي` "my friend", `صَدِيقُكَ` "your friend"): the "my" form joins the other readings of its
  spelling; the other pronouns only fill spellings that have no reading at all.
- Merged the forms of a word that differ only by their final case ending (-u, -i, -a, -un, -in, final
  sukun); the accusative -an written with alif is kept. Different words with the same pausal form
  stay separate readings.
- Ranked the readings of each spelling: lemmas and the pronoun-suffixed forms of function words first,
  then inflected forms and proper names, then classical, archaic or dialectal variants and construct
  duals; ties broken by the size of the Wiktionary entry, function words first. The main reading of
  130 very frequent spellings was chosen by hand. At most 6 readings are kept per spelling.
- Added by hand 39 readings that Wiktionary lacks, mostly words with a pronoun suffix (`حَالُكَ` "your
  condition", `يُمْكِنُكَ` "you can"); removed 3 spellings whose only readings were rare homographs of
  "and" + a function word (`وهي`, `وقد`, `وفي`).
- Shortened glosses to the first sense (parentheses removed, 40 characters at most); inflected forms get
  the gloss of their lemma followed by a short grammatical label, such as `to write (1s past)`.
- Filtered to the spellings of the 50,000 most frequent words of OpenSubtitles 2018 (FrequencyWords by
  Hermit Dave, https://raw.githubusercontent.com/hermitdave/FrequencyWords/cdd980291e6cd9ab0e5b3b78b0fe1d1f64385c23/content/2018/ar/ar_50k.txt), also after removing a proclitic and the article, plus the words and
  expressions of the app's starter list, the multi-word expressions made of frequent words and the
  lemmas of the main readings.
