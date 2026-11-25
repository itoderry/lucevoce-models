# dict-1: credits

LuceVoce's dictionary packs (`.lvpack`, each a `manifest.json`, `dictionary.lvdict` and `LICENCE.txt` with the source's
licence and credit), made on 20 Nov 2026 by LuceVoce's `tools/dict_build/make_packs.sh` from the wordnets below, every
source pinned by its SHA-256. The change made to each: the wordnet converted to LuceVoce's dictionary format, and, for a
synset with no definition of its own, the Open English WordNet's definition of the same concept (by its ILI id), marked
"(English)".

| Pack | Source | Licence of the source, and of the pack |
|---|---|---|
| dict-it-multiwordnet | MultiWordNet, Italian, Fondazione Bruno Kessler, through the Open Multilingual Wordnet 2.0 | CC BY 3.0 |
| dict-it-italwordnet | ItalWordNet, Istituto di Linguistica Computazionale of the CNR, Pisa (corrected by Tommaso Petrolito), through the Open Multilingual Wordnet 2.0 | ODC-BY |
| dict-es-mcr | Multilingual Central Repository 3.0, Spanish, through the Open Multilingual Wordnet 2.0 | CC BY 3.0 |
| dict-pl-plwordnet | plWordNet (Słowosieć), Wrocław University of Science and Technology, through the Open Multilingual Wordnet 2.0 | plWordNet licence (Princeton WordNet's terms) |
| dict-pt-openwnpt | OpenWN-PT, the Open Wordnet for Portuguese, through the Open Multilingual Wordnet 2.0 | CC BY-SA |
| dict-ro-rown | Romanian Wordnet (RoWN), Research Institute for Artificial Intelligence of the Romanian Academy (RACAI), through the Open Multilingual Wordnet 2.0 | CC BY-SA |
| dict-nl-odwn | Open Dutch WordNet, Vrije Universiteit Amsterdam, through the Open Multilingual Wordnet 2.0 | CC BY-SA 4.0 |
| dict-ja-wnja | Japanese Wordnet, NICT, through the Open Multilingual Wordnet 2.0 | WordNet licence |
| dict-zh-cow | Chinese Open Wordnet, Francis Bond and Shan Wang, Nanyang Technological University, through the Open Multilingual Wordnet 2.0 | WordNet licence |
| dict-de-odenet | OdeNet, the Open German WordNet, Hochschule Darmstadt (github.com/hdaSprachtechnologie/odenet, commit 8ba7412) | CC BY-SA 4.0 |
| dict-uk-ukrajinet | Ukrajinet, the Ukrainian WordNet, Hochschule Darmstadt (github.com/hdaSprachtechnologie/ukrajinet, commit 9392b80) | CC BY-SA 4.0 |

The English definitions: Open English WordNet, 2025 edition, by the Open English WordNet team, CC BY 4.0
(github.com/globalwordnet/english-wordnet).

The Open Multilingual Wordnet 2.0: github.com/omwn/omw-data, release v2.0.

A pack made from a CC BY-SA source is an adaptation and is shared under the same licence. LuceVoce never bundles them:
each is downloaded only when its reader asks for it.

Moby Thesaurus (dict-en-moby, added 24 Nov 2026): Moby Thesaurus II by Grady Ward, "Public Domain material by grant
from the author, January, 2001" (Project Gutenberg ebook 3202, gutenberg.org/ebooks/3202; the file files.zip, SHA-256
3a54e61dd3b4153313e00c3113bda1e939af505d1336a350a0fd93a80538a6d8). Changed: for each root word, only the twelve related
words closest to it are kept (LuceVoce's `tools/dict_build/make_moby_pack.sh` and `src/dict/thesaurus.cpp`).

Wiktionary dictionaries (dict-<l>-wiktionary for fr, de, es, it, pt, pl, nl; added 25 Nov 2026): the words of each
language's own Wiktionary, by its contributors, as extracted by kaikki.org with wiktextract (kaikki.org says its data
"is made available under the same licenses as Wiktionary", read 25 Nov 2026: CC BY-SA 4.0, and the GFDL). Sources,
https://kaikki.org/<l>wiktionary/raw-wiktextract-data.jsonl.gz of 1-2 Nov 2026, by SHA-256:

- Wiktionnaire (fr.wiktionary.org): 33c7b73bc11d2533c9c0e0be6484ded76bd9ff29337065f2070b4f1b7d2e4f3c
- Wiktionary (de.wiktionary.org): 3405adc801ae68406304f9317421d3df6bca74ffcaa041a88afc44c5a5debcbe
- Wikcionario (es.wiktionary.org): 206001cbdfc783cf4076789366e2c0cb27860da739ddfcc0189c4c878b189da1
- Wikizionario (it.wiktionary.org): 075c981ca609a66d62471b9484b612b3269843aa6790806acd4bbb7615811d80
- Wikcionário (pt.wiktionary.org): 0990ec2517efca42cc04c3b854a46f28f3204ab5acd337f641c32c00dd45ddae
- Wikisłownik (pl.wiktionary.org): 30fda85e7309d8c3d3345780e7140ca55daa49653fed060f0498c128413bf906
- WikiWoordenboek (nl.wiktionary.org): 1657c961242ca63ce276b1259445be6930ad1c98fd4005fea52c4e55de675c56

Changed: only the words of the pack's language; at most twelve meanings per word and part of speech, two examples
of at most 240 bytes per meaning, the first pronunciation; a word that is only a form of another is listed as one of
that word's forms (LuceVoce's `tools/dict_build/make_kaikki_packs.sh` and `src/dict/kaikki.cpp`). Licence of the packs:
CC BY-SA 4.0 (https://creativecommons.org/licenses/by-sa/4.0/).
