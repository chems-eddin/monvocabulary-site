# Norwegian Bokmål pronunciations (IPA, Eastern Norwegian) from NB Uttale

`nb.tsv`: 46175 rows, 40244 distinct keys. Columns: `form`, `ipa` (without slashes), `pos`
(Universal Dependencies tag, or empty), `note` (empty). Several rows for the same form are different
pronunciations, the most likely one first. This is the data shipped in the MonVocabulary app
(`Pronunciation/nb.sqlite`).

## Source and authors

- NB Uttale 1.0, Språkbanken (the Norwegian Language Bank) at the National Library of Norway,
  https://www.nb.no/sprakbanken/ressurskatalog/oai-nb-no-sbr-79/ — based on the NST lexicon
  (Nordisk Språkteknologi, late 1990s).
- File `nb_uttale_leksika/e_spoken_pronunciation_lexicon.csv` from `nb_uttale_leksika.zip` (2023-03-10, SHA-256 `6e87e9e99a6081a5fc4164077750652880f4a663c860f50c3d45b18ba003bc80`); member SHA-256
  `dd2965958ccced2c99e77f49c38ac3dfdb15ccbec29fc99b8451ddfaebc93afc`.
- Selection only (no content copied): FrequencyWords by Hermit Dave, OpenSubtitles 2018 Norwegian
  list, https://github.com/hermitdave/FrequencyWords.

## Modifications

Eastern Norwegian, spoken-style lexicon. Selected the forms among the 50,000 most frequent Norwegian words (OpenSubtitles 2018 list by Hermit Dave), plus forms shorter than 4 characters and the words of the app's starter list; removed multi-word entries and affixes. IPA: tone 1 written ˈ, tone 2 written ²ˈ, long i written iː (the source IPA table has ɪː for X-SAMPA i:), syllable dots and tie bars removed, g → ɡ. One row per distinct pronunciation of a form, the most likely first (readings from the NST list of frequent word forms first, then by part of speech and stress; some frequent words checked by hand); POS tags mapped to Universal Dependencies. Corrected by hand: selvfølgelig səlˈfœlɡəlɪ (short final i), lyskrysset ²ˈlyːsˌkrʏsə (secondary stress placed after lys); added the unstressed reading ɔ of og (CONJ), missing from the source, as its first reading.

- Kept: forms among the 50,000 most frequent words (case-insensitive), forms shorter than 4 characters,
  and every word of the app's Norwegian starter list. Removed: multi-word entries, affixes, forms
  without letters.
- IPA (from the `ipa_transcription` column): tone 1 `'` → `ˈ`, tone 2 `"` → `²ˈ`, secondary stress `ˌ`
  kept; `ɪː` → `iː` (NOFABET II, X-SAMPA i:); `_` inside acronyms removed; syllable dots and tie bars
  removed (æ͡ɪ → æɪ), g → ɡ.
- POS: NN/NM → NOUN, JJ → ADJ, VB → VERB, AB → ADV, PP → ADP, PN → PRON, DT → DET, KN → CONJ,
  IN → INTJ, IE → PART, RG → NUM, RO → ADJ, PM → PROPN; "og" (tagged IN in the source) → CONJ.
- Order of the pronunciations of a form (the source has no frequency per reading): readings found in
  the NST list of frequent word forms (ids 27317–139999) before readings that only come from generated
  paradigms; then function words, verbs (except bare imperatives), adjectives and definite singular
  nouns, other nouns, imperatives, letter names, genitives, proper nouns; stressed before reduced
  forms; then source order. Two verb readings that differ only by tone: tone 1 first; set by hand for: bilen, boka, bussen, bør, de, din, du, faen, faren, folka, funnet, hende, håret, karen, klubben, laget, lyst, moren, nesa, og, ost, råd, skipet, skrevet, snakket, sukker, tenner.

## License

NB Uttale is released under CC0 1.0 (https://creativecommons.org/publicdomain/zero/1.0/). This file
is released under CC0 1.0 as well. Credit: NB Uttale, Språkbanken at the National Library of Norway.
