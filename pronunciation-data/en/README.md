# English pronunciations (General American IPA) derived from CMUdict

`en.tsv`: 135090 rows, 126006 distinct keys. Columns: `form`, `ipa` (without slashes), `pos`, `note`
(both empty). Several rows for the same form are alternative pronunciations, the preferred one first.
This is the data shipped in the MonVocabulary app (`Pronunciation/en.sqlite`).

## Source

- The CMU Pronouncing Dictionary, https://github.com/cmusphinx/cmudict
- Commit `74790861f652b15e4ac49015a90074ad62a27690` (2025-10-24), file `cmudict.dict`, SHA-256 `81917843c7f44ce2b094ac63873c2c7a4cf802040792c455ba3ca406891c3d22`
- Authors: Carnegie Mellon University and the contributors to CMUdict

## Modifications

Converted from ARPAbet to IPA (General American); syllabified to place stress marks; when a word has several primary stresses, all but the last made secondary (ok → ˌoʊˈkeɪ); for 20 words, the usual reading put first or added (read ˈɹid, live ˈlɪv, excuse ɪkˈskjuz, Buckingham ˈbʌkɪŋəm…; full list in the published README).

- ARPAbet phonemes mapped to IPA: AH0 → ə, AH1/AH2 → ʌ, ER0 → ɚ, ER1/ER2 → ɝ, R → ɹ, Y → j,
  JH → dʒ, CH → tʃ, other phonemes as usual; no flapping, no dark l. ER0 before a vowel is written
  ə + ɹ, the ɹ starting the next syllable (interesting → ˈɪntəˌɹɛstɪŋ).
- Words syllabified by maximal onset (legal English onsets, s + stop clusters as onsets, no ŋ onset,
  no s + f onset inside a word, a stressed lax vowel keeps a coda unless a stronger stress follows)
  so that ˈ (primary) and ˌ (secondary) stand before their syllable (transfer → tɹænsˈfɝ). Two
  frequent morpheme boundaries fixed by hand: out- + ɹ (outrage → ˈaʊtˌɹeɪdʒ) and -room after t, d, k
  (restroom → ˈɹɛstˌɹum).
- Inconsistent secondary stresses dropped (vowel unchanged): word-final /i/ or /oʊ/ after the primary
  stress (tomorrow → təˈmɑɹoʊ, company → ˈkʌmpəni); /ɪ/ of the first syllable right before the
  primary stress (decide → dɪˈsaɪd, important → ɪmˈpɔɹtənt).
- Several primary stresses in a word (CMUdict `OK OW1 K EY1`, `OUTSIDE`, `FOURTEEN`, `WELL-KNOWN`):
  all but the last made secondary (ok → ˌoʊˈkeɪ, as CMUdict writes `OKAY OW2 K EY1`).
- Comments and entries containing digits removed; variants that yield the same IPA merged. When a
  dotted and an undotted spelling share a lookup key, only the expected one is kept (`u.s.`, `in`).
- Usual reading put first (the other CMUdict readings follow), or added when CMUdict lacks it; it
  replaces the CMUdict reading that only differed by a secondary stress (perfect ˈpɝˌfɪkt):
  - `accent`: AE1 K S EH0 N T → ˈæksɛnt, noun first (American), without a secondary stress.
  - `and`: AE1 N D → ˈænd, stressed form first for the word on its own (the app uses the weak form in phrases).
  - `basil`: B EY1 Z AH0 L → ˈbeɪzəl, American reading of the herb added (CMUdict only has the British one).
  - `buckingham`: B AH1 K IH0 NG AH0 M → ˈbʌkɪŋəm, usual reading added (CMUdict only has a spelling pronunciation).
  - `costume`: K AA1 S T UW0 M → ˈkɑstum, noun first (American).
  - `dr`: D AA1 K T ER0 → ˈdɑktɚ, “Dr.” read as doctor first (CMUdict lists drive first).
  - `enjoy`: IH0 N JH OY1 → ɪnˈdʒɔɪ, reading without a secondary stress first.
  - `excuse`: IH0 K S K Y UW1 Z → ɪkˈskjuz, verb first, as in “excuse me” (CMUdict lists the noun first).
  - `forbidden`: F ER0 B IH1 D AH0 N → fɚˈbɪdən, usual American reading added (not in CMUdict).
  - `impact`: IH1 M P AE0 K T → ˈɪmpækt, noun first.
  - `in`: IH1 N → ˈɪn, stressed form first for the word on its own (the app uses the weak form in phrases).
  - `lead`: L IY1 D → ˈlid, verb first (CMUdict lists the metal first).
  - `live`: L IH1 V → ˈlɪv, verb first (CMUdict lists the adjective first).
  - `perfect`: P ER1 F IH0 K T → ˈpɝfɪkt, adjective first, without a secondary stress.
  - `read`: R IY1 D → ˈɹid, present tense and noun first (CMUdict lists the past tense first).
  - `subject`: S AH1 B JH IH0 K T → ˈsʌbdʒɪkt, noun first (CMUdict lists the verb first).
  - `tears`: T IH1 R Z → ˈtɪɹz, noun (crying) first (CMUdict lists the verb first).
  - `use`: Y UW1 Z → ˈjuz, verb first (CMUdict lists the noun first).
  - `wind`: W IH1 N D → ˈwɪnd, noun (air) first (CMUdict lists the verb first).
  - `wound`: W UW1 N D → ˈwund, noun (injury) first (CMUdict lists the past of wind first).

## License

Copyright (C) 1993-2015 Carnegie Mellon University. All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions
are met:

1. Redistributions of source code must retain the above copyright
   notice, this list of conditions and the following disclaimer.
   The contents of this file are deemed to be source code.

2. Redistributions in binary form must reproduce the above copyright
   notice, this list of conditions and the following disclaimer in
   the documentation and/or other materials provided with the
   distribution.

This work was supported in part by funding from the Defense Advanced
Research Projects Agency, the Office of Naval Research and the National
Science Foundation of the United States of America, and by member
companies of the Carnegie Mellon Sphinx Speech Consortium. We acknowledge
the contributions of many volunteers to the expansion and improvement of
this dictionary.

THIS SOFTWARE IS PROVIDED BY CARNEGIE MELLON UNIVERSITY ``AS IS'' AND
ANY EXPRESSED OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO,
THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR
PURPOSE ARE DISCLAIMED.  IN NO EVENT SHALL CARNEGIE MELLON UNIVERSITY
NOR ITS EMPLOYEES BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL,
SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT
LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
