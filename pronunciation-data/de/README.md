# German pronunciations (IPA) from the German Wiktionary

`de.tsv`: 47197 rows, 38726 distinct keys. Columns: `form`, `ipa` (without slashes), `pos`, `note`
(both empty). Several rows for the same form are alternative pronunciations, the preferred one first;
forms that differ only by case (`Weg`, `weg`) are separate rows, the lowercase form first. This is the
data shipped in the MonVocabulary app (`Pronunciation/de.sqlite`).

## Source and authors

- Pronunciations written by the Wiktionary contributors on https://de.wiktionary.org (see each word's
  page history for the list of authors).
- Extracted by german-ipa-dict by devio-at, https://github.com/devio-at/german-ipa-dict
  (commit `a08113e0ab80f049b625fc360196491f56243ca1`, 2023-02-22, file `de_dewikt.csv`, SHA-256 `1021fa07108658e4837388229d1e9b3e12a2d88e9a4009fcb548aa3d60daa699`), as
  republished and corrected in ipa-dict, https://github.com/open-dict-data/ipa-dict (commit `43c3570eb3553bdd19fccd2bd0091534889af023`,
  2025-05-24, file `data/de.txt`, SHA-256 `d36d11dbcc226468a22f0fb3a0794ee0ce142bf277e26e517a8bfd0de1ec2653`). The ipa-dict file is the main source; the
  german-ipa-dict file is used for the variant qualifiers and for the few words missing from ipa-dict.
- Selection only (no content copied): FrequencyWords by Hermit Dave, OpenSubtitles 2018 German list,
  https://github.com/hermitdave/FrequencyWords.

## Modifications

Selected the forms among the 50,000 most frequent German words (OpenSubtitles 2018 list by Hermit Dave), plus forms shorter than 4 characters and the words of the app's starter list; removed multi-word expressions and affixes. IPA cleaned: slashes, syllable dots and tie bars removed, g → ɡ, word-initial glottal stop removed, doubled or misplaced stress marks fixed, unstressed duplicates and variants with non-IPA characters dropped. Variants reordered (the extraction had sorted them): unqualified before regional or colloquial ones, Duden standard forms first, a few words by hand. Dropped a few foreign readings of capitalized forms that hide a German word (Die /daɪ/, Dies /daɪs/, Allen /ˈælən/, Hole /hɔʊ̯l/, Manche /mɑ̃ːʃ/) and the rare form lust /luːst/ (Lust /lʊst/ is used instead); second primary stress made secondary in the irgend- family (irgendwie /ˈɪʁɡn̩tˌviː/, as in the Duden); OK given the pronunciation of okay.

- Kept: forms among the 50,000 most frequent words (case-insensitive), forms shorter than 4 characters,
  and every word of the app's German starter list. Removed: multi-word expressions, affixes, forms
  without letters.
- IPA: slashes, brackets, syllable dots and tie bars removed (t͡s → ts), g → ɡ; word-initial ʔ removed
  (the source almost never writes it), word-internal ʔ kept; doubled stress marks merged, stress marks
  at the end of a word removed, stress marks written before a diacritic or ː moved after it.
- Variants: duplicates merged; a variant without stress identical to a stressed one dropped; variants
  with characters outside the app's IPA set dropped (a few loanwords with ã, õ); readings dropped by
  hand: Allen /ˈælən/, Die /daɪ/, Dies /daɪs/, Hole /hɔʊ̯l/, Manche /mɑ̃ːʃ/, lust /luːst/; second primary stress made secondary in irgendein, irgendeine, irgendeinem, irgendeinen, irgendeiner, irgendeines, irgendwer, irgendwie, irgendwo.
- Added forms (missing from both files): OK (pronunciation of okay).
- Order (the extraction had sorted the variants alphabetically): unqualified variants before variants
  marked as regional, colloquial, foreign or "also"; then the Duden standard form before its variant
  (-ɪç before -ɪk, n̩ before an assimilated nasal, ɛː before eː, aːɐ̯ before aʁ…); verbs in über-,
  unter-, hinter-, wider-: stem stress (inseparable verb) first; set by hand for: Alkohol, Anna, Chance, Chancen, China, Hochzeit, Kilometer, Miteinander, Post, Rum, Stil, Toilette, Toiletten, Uni, abendessen, durchsetzen, hallo, hierher, hierzu, miteinander, post, tausend, tun, umgehen, vorn, wiederholen; and for
  the word families kost- (kɔst), gekost- (kɔst), urteil- (ʊʁ), beurteil- (ʊʁ), verurteil- (ʊʁ), dusch- (dʊʃ), lutsch- (lʊtʃ), gelutsch- (lʊtʃ). In a capitalized form, variants shared with the lowercase form come first.

## License

This file is licensed under the Creative Commons Attribution-ShareAlike 4.0 International License,
https://creativecommons.org/licenses/by-sa/4.0/ (Wiktionary text contributed before June 2023 is
under CC BY-SA 3.0, which allows adaptations under version 4.0). It is provided as is, without
warranty of any kind.
