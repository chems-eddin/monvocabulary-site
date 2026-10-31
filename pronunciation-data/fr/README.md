# French pronunciations (IPA) derived from Lexique 3.83

`fr.tsv`: 125773 rows, 125691 distinct keys. Columns: `form` (spelling as in Lexique, e.g. `coeur`),
`ipa` (without slashes, no stress marks), `pos` (Universal POS tag from Lexique's `cgram`), `note` (empty).
Several rows for the same form are distinct pronunciations (homographs), the most frequent first
(Lexique's `freqfilms2`; « sens » and « tous » excepted, see below).
This is the data shipped in the MonVocabulary app (`Pronunciation/fr.sqlite`).

## Source

- Lexique 3.83 (2019-06-04), https://www.lexique.org/databases/Lexique383/Lexique383.zip
- Authors: Boris New & Christophe Pallier, with Ronald Peereman, Sophie Dufour, Christian Lachaud and
  other contributors (see the Lexique README)
- File `Lexique383.zip` (https://www.lexique.org/databases/Lexique383/Lexique383.zip), SHA-256 `e181d132b3b0d3d87efc98d376968441b517353933011cebea5366321a6024e6`; table `Lexique383.tsv`, SHA-256 `637ba37a767a66679c48371d673ece50cbf541b49a4e40e598963d4f3fbce52b`
- References: New, Pallier, Brysbaert & Ferrand (2004), *Lexique 2: A New French Lexical Database*,
  Behavior Research Methods, Instruments, & Computers 36 (3): 516-524; New, Brysbaert, Veronis &
  Pallier (2007), *The Use of Film Subtitles to Estimate Word Frequencies*, Applied Psycholinguistics 28 (4).
- Place names (40 rows with `pos` PROPN, absent from Lexique): French Wiktionary, https://fr.wiktionary.org/,
  Wiktionary contributors, CC BY-SA 4.0, pronunciations read on 2026-10-31 on the page of each name.

## Modifications

Extracted orthography, pronunciation and part of speech; converted Lexique phonetic codes to IPA; adapted transcriptions to the conventions of French dictionaries (optional schwas dropped where they are not pronounced, unstressed o written ɔ, e written ɛ in closed syllables, verb-final -ai written e, a few isolated corrections: est as a verb ɛ, tous as a determiner tu, essai- family es-, peur, sers…); noun « sens » (sɑ̃s) and pronoun « tous » (tus) listed first; multi-word expressions split into words where unambiguous; 40 place names added from the French Wiktionary (https://fr.wiktionary.org/, CC BY-SA 4.0), syllable dots and liaison marks removed.

- Columns kept: `ortho`, `phon`, `cgram`; `freqfilms2` (then `freqlivres`) only to order homographs.
  All forms are kept; one row per distinct pronunciation of a form.
- Lexique phonetic codes mapped to IPA: E → ɛ, O → ɔ, 2 → ø, 9 → œ, ° → ə, @ → ɑ̃, § → ɔ̃, 5 → ɛ̃,
  1 → œ̃, R → ʁ, S → ʃ, Z → ʒ, N → ɲ, G → ŋ, 8 → ɥ, g → ɡ, other codes unchanged. No stress marks.
- Optional schwa (°) dropped at the end of a word of several syllables (puisque → pɥisk), and inside
  a word between vowel + consonant and consonant + vowel outside the first syllable
  (seulement → sœlmɑ̃, samedi → samdi), except between two r or two l or before consonant + glide.
- Non-optional schwa coded `2` (premier, ce, dehors) written ə when the spelling has no eu, œ, ueil or ö.
- e written ɛ before two consonants that cannot begin the next syllable (destin → dɛstɛ̃), when the
  spelling has no é.
- Lexique's o outside the last syllable written ɔ when spelled o (comment → kɔmɑ̃), except before z,
  in -otion and in gross-, doss-, foss-; au before r written ɔ (restaurant → ʁɛstɔʁɑ̃); o before a
  word-final r written ɔ (ignore → iɲɔʁ).
- Verb forms ending in -ai (future, simple past, « ai ») end in e instead of ɛ.
- Corrected: peur, peuple, peuplent, pleuve, pleuvent (ø → œ), ait, ais and the verb est (e → ɛ), sers
  (se → sɛʁ), tous as a determiner (tus → tu; the pronoun stays tus), initial ɛs- of the essai- family
  written es- like essai and essayer (essaie → esɛ, essaim → esɛ̃), « la plupart des » (dɛ → de, like
  « des »), « champs élysées » (ʃɑ̃zelize, with the liaison).
- Order changed: the noun « sens » (sɑ̃s) and the pronoun « tous » (tus) come first, ahead of the
  more frequent verb sɑ̃ and determiner tu (the app picks those from the context).
- Multi-word expressions: a space between words when the pronunciation splits in only one way.
- Place names added from the French Wiktionary: Eiffel, Versailles, Louvre, Montmartre, Champs-Élysées, France, Lyon, Marseille, Toulouse, Lille, Strasbourg, Nantes, Bretagne, Normandie, Provence, Londres, Bruxelles, Genève, Québec, Montréal, Luxembourg, Rome, Madrid, Barcelone, Espagne, Italie, Portugal, Grèce, Irlande, Autriche, Russie, Europe, Afrique, Asie, Australie, États-Unis, Mexique, Maroc, Algérie, Tunisie. Syllable dots and liaison marks removed,
  Mexique written mɛksik (e before two consonants written ɛ, as in mexicain), Lyon ljɔ̃ (the
  Wiktionary's second pronunciation, the one of « lion » in Lexique).
- Part of speech: NOM → NOUN, VER/AUX → VERB, ADJ → ADJ, ADJ:num → NUM, other ADJ:* and ART:* → DET,
  ADV → ADV, PRE → ADP, CON → CONJ, PRO:* → PRON, ONO → INTJ; for a pronunciation shared by several
  entries, the category of the most frequent one; PROPN for the added place names.

## License

This file is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License
(CC BY-SA 4.0), https://creativecommons.org/licenses/by-sa/4.0/, like Lexique 3.83 itself.
Credit: « Lexique 3.83, Boris New & Christophe Pallier, with Ronald Peereman, Sophie Dufour, Christian Lachaud and others; place names: French Wiktionary contributors ». Provided as is, without warranties of any kind.
