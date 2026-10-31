# Italian pronunciations (IPA) derived from the English Wiktionary

`it.tsv`: 40140 rows, 37505 distinct keys. Columns: `form`, `ipa` (standard Italian, without
slashes), `pos` (universal part-of-speech tag or empty), `note` (lemma of an inflected form, or empty).
Several rows for the same form are alternative pronunciations or homographs, the preferred one first.
A row with an empty `ipa` is an inflected form that has no pronunciation in Wiktionary: its `note` gives
the lemma, whose pronunciation is in the file. When the lemma's conjugation table in Wiktionary writes the
form with a stress accent, `form` keeps it (`pènsi` for pensi, `avrèi` for avrei): the accent on a non-final
vowel is not part of the spelling, it marks the stressed vowel and, on e and o, its open (è ò) or closed
(é ó) quality. This is the data shipped in the MonVocabulary app (`Pronunciation/it.sqlite`).

## Source

- Italian entries of the English Wiktionary, https://en.wiktionary.org/
- Authors: the Wiktionary contributors (see the history of each page on en.wiktionary.org)
- Extracted by kaikki.org with wiktextract (Tatu Ylonen), https://kaikki.org/dictionary/Italian/
- File `kaikki.org-dictionary-Italian.jsonl`, extraction of 2026-10-25 from the enwiktionary dump of
  2026-10-01, SHA-256 `c4de3437631be893aa029920eeca83ff1ca844c632e043c571589e79d500614c`
- Word selection only: FrequencyWords (Hermit Dave), OpenSubtitles 2018 Italian list `it_50k.txt`,
  commit `bd9e23103f0a7f89b4c604ecf8638e6f62ee0211`, https://github.com/hermitdave/FrequencyWords (no data copied from it)

## Modifications

Italian entries of the English Wiktionary (kaikki.org extraction of 2026-10-25, dump of 2026-10-01): kept phonemic IPA only; removed syllable dots, tie bars, liaison marks, optional segments and vowel length; chose the standard pronunciation first (regional, dialectal and proscribed variants dropped when a standard one exists); filtered to the 50,000 most frequent word forms of OpenSubtitles 2018 (FrequencyWords), their lemmas and the app's starter list; added the lemma (note column, empty IPA) for inflected forms that have no IPA in Wiktionary, with the stress accent of Wiktionary's conjugation table kept in the form column (pènsi for pensi); read unaccented spellings of 6 frequent words (perche, cosi...) as the accented word first; kept the optional consonant that lengthens an inherently long one (traduzione); corrected 13 isolated errors and added 19 frequent function words missing from the source (the article i, articulated prepositions such as della), transcribed by hand.

- Only phonemic transcriptions (between slashes) kept; phonetic ones, ones marked with an asterisk and
  narrow transcriptions with symbols foreign to standard Italian dropped.
- Syllable dots, tie bars (t͡s → ts, t͡ʃ → tʃ, d͡ʒ → dʒ), liaison marks ‿, optional segments in
  parentheses and vowel length marks removed; Latin g replaced by ɡ; geminates written as double
  consonants (ˈɡrattsje); stress marks kept before the stressed syllable. An optional consonant that
  lengthens an inherently long one (ts, dz, ʃ, ɲ, ʎ) is kept, as in standard Italian:
  tra.du(t)ˈt͡sjo.ne → tradutˈtsjone.
- Untagged or "standard" pronunciations first, then "traditional" ones; regional, dialectal, rare,
  nonstandard or proscribed variants kept only when an entry has nothing else.
- Homographs ordered: lowercase before capitalised forms, current senses before archaic, poetic or
  rare ones and before letter and note names, then page order, except: che /ke/ first, fossi /ˈfossi/ first, ed /ed/ first;
  repeated pronunciations merged.
- Unaccented spellings of frequent words that Wiktionary also lists as rare words read as the accented
  word first (row with the unaccented form, the accented word in `note`), then their own readings:
  perche as perché, cosi as così, giu as giù, citta as città, finche as finché, caffe as caffè.
- Multi-word entries, affixes, letters and symbols left out.
- Corrected by hand (Wiktionary value after the cleaning above → this file): congratulazioni /konɡratulatˈtsjɔni/ → /konɡratulatˈtsjoni/, pensieri /penˈsjeri/ → /penˈsjɛri/, fuochi /ˈfwoki/ → /ˈfwɔki/, vuote /ˈvwote/ → /ˈvwɔte/, vuoti /ˈvwoti/ → /ˈvwɔti/, museruola /muzeˈrwola/ → /muzeˈrwɔla/, ciecamente /ˌtʃekaˈmɛnte/ → /ˌtʃɛkaˈmente/, dà /da/ → /ˈda/, all' /ˈal/ → /all/, farei /faˈrej/ → /faˈrɛj/, vi /ˈvi/ → /vi/, Vi /ˈvi/ → /vi/, bel /bɛl/ → /ˈbɛl/.
- Added by hand (no pronunciation in the source): i /i/, del /del/, dello /ˈdello/, della /ˈdella/, delle /ˈdelle/, dal /dal/, nello /ˈnello/, nella /ˈnella/, negli /ˈneʎʎi/, sul /sul/, sulla /ˈsulla/, sui /ˈsui/, sugli /ˈsuʎʎi/, sulle /ˈsulle/, coi /ˈkoi/, dell' /dell/, dall' /dall/, nell' /nell/, coll' /koll/.

## License

Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0),
https://creativecommons.org/licenses/by-sa/4.0/ — this file is an adaptation of Wiktionary content and
is shared under the same license. Attribution: Wiktionary contributors (en.wiktionary.org), via kaikki.org (wiktextract).
