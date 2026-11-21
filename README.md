# LuceVoce models

Model files that LuceVoce, an app that reads books aloud, downloads on request. The files are attached to this
repository's releases; the repository itself holds this description, the licence, the notices (`NOTICE.txt`) and
the credits of each release (`credits/`, the newest copy of a release's `CREDITS.md`).

## kokoro-coreml-1

Release: [kokoro-coreml-1](https://github.com/itoderry/lucevoce-models/releases/tag/kokoro-coreml-1)

`kokoro-coreml-1.zip` holds the Kokoro-82M voice model converted to Core ML, so that LuceVoce's Kokoro voices can
read on the Neural Engine of a Mac, an iPhone or an iPad. Seven compiled models (`.mlmodelc` folders) and a
`NOTICE.txt`:

- KokoroAlbert, KokoroPostAlbert, KokoroAlignment, KokoroProsody, KokoroNoise, KokoroVocoder, KokoroTail

| | |
|---|---|
| Size | 76,959,442 bytes |
| SHA-256 | `31066b2951629890b7942e0de4c5e23beb1ce1d5cd32e1cd196f3420a07a7754` |

Where it comes from:

- The model is [Kokoro-82M](https://huggingface.co/hexgrad/Kokoro-82M) by hexgrad, Apache License 2.0.
- It was converted to Core ML with [laishere/kokoro-coreml](https://github.com/laishere/kokoro-coreml)
  (commit 484907db6a8347a6afb6e7b86850ea2878c6a3fb, Apache License 2.0) and compiled with Xcode's coremlcompiler.
  Nothing else was changed.

What the licences ask and how it is met: Apache 2.0 allows passing the model on, changed or not, also in a
commercial product, when the licence text comes with it (`LICENSE` here, and LuceVoce ships it too), the change is
stated (the conversion, above and in `NOTICE.txt`) and the upstream notices are kept (neither project has a NOTICE
file of its own).

Kokoro's own credits for training data that asks for one:

- French voice ff_siwis: The SIWIS French Speech Synthesis Database, by Junichi Yamagishi, Pierre-Edouard Honnet,
  Philip Garner and Alexandros Lazaridis, University of Edinburgh, Centre for Speech Technology Research
  (https://hdl.handle.net/10283/2353), CC BY 4.0.
- Japanese voices jf_gongitsune, jf_nezumi, jf_tebukuro and jm_kumo: readings by TNC (TV Nishi-Nippon) announcers
  from the Koniwa corpus, tnc set (https://github.com/koniwa/koniwa), CC BY 3.0.

The archive holds the network only. The voices themselves (`voices-v1.0.bin`) and the ONNX model that LuceVoce
uses on every platform are in the release `kokoro-onnx-1`, below.

## kokoro-onnx-1

Release: [kokoro-onnx-1](https://github.com/itoderry/lucevoce-models/releases/tag/kokoro-onnx-1)

The two files LuceVoce's Kokoro voices need on every platform, read with ONNX Runtime:

| File | What it is | Size | SHA-256 |
|---|---|---|---|
| `kokoro-v1.0.onnx` | the Kokoro-82M voice model as an ONNX model | 325,532,387 bytes | `7d5df8ecf7d4b1878015a32686053fd0eebe2bc377234608764cc0ef3636a6c5` |
| `voices-v1.0.bin` | the voices (one style table for each voice) | 28,214,398 bytes | `bca610b8308e8d99f32e6fe4197e7ec01679264efed0cac9140fe9c29f1fbf7d` |

Where they come from:

- The model and the voices are [Kokoro-82M](https://huggingface.co/hexgrad/Kokoro-82M) by hexgrad, Apache License 2.0.
- The conversion to ONNX and the packing of the voices into one file are the work of
  [thewh1teagle/kokoro-onnx](https://github.com/thewh1teagle/kokoro-onnx) (its release `model-files-v1.0`; the
  project's code is MIT, and it states the model's licence as Apache 2.0).
- Both files are copied from that release byte for byte. Nothing was changed. They are kept here so that LuceVoce
  does not depend on another project's release page staying where it is.

The licence's conditions are met as for the Core ML archive above (the licence text, the statement of what was
changed, here nothing by LuceVoce, and the credits for the training data, which apply to these files too).

## piper-1

Release: [piper-1](https://github.com/itoderry/lucevoce-models/releases/tag/piper-1)

Piper voices, copied unchanged from the Piper voices repository,
[rhasspy/piper-voices](https://huggingface.co/rhasspy/piper-voices) (revision e7229f7d33a10e145e109b886d661984201ac3c4,
12 Nov 2026; the voices added on 19 Nov 2026 from revision 42301ec547bc2939386cf0ae9f9050ca05b1d3af), each with its model
card (`<voice>.MODEL_CARD`) and the release's `CREDITS.md`. Only voices whose data, and whose base model when
fine-tuned, allow commercial use are here. Two base models some of them were fine-tuned from, both trained from
scratch: rdh (`nl_BE-rdh-medium`, [dutch-vl-tts](https://github.com/r-dh/dutch-vl-tts), CC0) and hifi_tts_92
(`en_US-hifi_tts_92-medium`, Cori Samuel in the [Hi-Fi Multi-Speaker English TTS Dataset](https://www.openslr.org/109/),
NVIDIA, CC BY 4.0).

| Voice | Language | Data and its licence | The voice's licence |
|---|---|---|---|
| `fr_FR-mls-medium` | French, 125 speakers (LuceVoce offers four) | [Multilingual LibriSpeech](https://openslr.org/94/), French (Pratap and others, 2020), CC BY 4.0 | CC BY 4.0 |
| `it_IT-serena-high` | Italian, one synthetic voice | [serena-synthetic-it-27h](https://huggingface.co/datasets/committa/serena-synthetic-it-27h) by Marco Baccarani, CC BY 4.0: speech made with Qwen3-TTS (Apache 2.0) from sentences adapted from [Tatoeba](https://tatoeba.org) (CC BY 2.0 FR) | CC BY 4.0 |
| `es_ES-carlfm-x_low` | Spanish, one speaker | [carlfm01/my-speech-datasets](https://github.com/carlfm01/my-speech-datasets), public domain by its author | public domain |
| `ro_RO-mihai-medium` (19 Nov 2026) | Romanian, one speaker (Mihai) | [OHF-Voice/voice-datasets](https://github.com/OHF-Voice/voice-datasets), CC0; fine-tuned from rdh | CC0 |
| `pt_BR-cadu-medium`, `pt_BR-jeff-medium` (19 Nov 2026) | Brazilian Portuguese, one speaker each (Cadu, Jeff) | OHF-Voice/voice-datasets, CC0; fine-tuned from rdh | CC0 |
| `pt_BR-faber-medium` (19 Nov 2026) | Brazilian Portuguese, one speaker (Faber) | OHF-Voice/voice-datasets, CC0; fine-tuned from hifi_tts_92 | CC0 data, CC BY 4.0 base |
| `fr_FR-siwis-medium` (19 Nov 2026) | French, one speaker (Sophie in LuceVoce) | [SIWIS French Speech Synthesis Database](https://datashare.is.ed.ac.uk/handle/10283/2353), University of Edinburgh, CC BY 4.0; fine-tuned from hifi_tts_92 | CC BY 4.0 |
| `it_IT-paola-medium` (19 Nov 2026) | Italian, one speaker (Paola) | OHF-Voice/voice-datasets, CC0; fine-tuned from hifi_tts_92 | CC0 data, CC BY 4.0 base |
| `it_IT-serena-medium` (19 Nov 2026) | Italian, a smaller Serena | serena-synthetic-it-27h, as above, CC BY 4.0; trained from scratch | CC BY 4.0 |
| `es_ES-davefx-medium` (19 Nov 2026) | Spanish, one speaker (David in LuceVoce) | OHF-Voice/voice-datasets, CC0; fine-tuned from rdh | CC0 |
| `es_ES-sharvard-medium` (19 Nov 2026) | Spanish, two speakers (Martín, Sara in LuceVoce) | [Sharvard corpus](https://datashare.ed.ac.uk/handle/10283/574) (Aubanel, García Lecumberri and Cooke), CC BY 3.0; fine-tuned from hifi_tts_92 | CC BY 3.0 |
| `es_MX-ald-medium` (19 Nov 2026) | Mexican Spanish, one speaker (Aldo in LuceVoce) | [Ald Mexican Spanish speech dataset](https://huggingface.co/datasets/rmcpantoja/Ald_Mexican_Spanish_speech_dataset), the Unlicense; fine-tuned from rdh | Unlicense |
| `pl_PL-darkman-medium`, `pl_PL-gosia-medium` (20 Nov 2026) | Polish, a male and a female voice (LuceVoce: Darek, Gosia) | [OHF voice-datasets](https://github.com/OHF-Voice/voice-datasets), CC0; fine-tuned from rdh (CC0) and hifi_tts_92 (CC BY 4.0) | CC0 (hifi_tts_92 credited) |
| `no_NO-talesyntese-medium` (21 Nov 2026) | Norwegian, one speaker (Ingrid) | NST Norwegian speech data ([Språkbanken](https://www.nb.no/sprakbanken/), National Library of Norway), CC0; fine-tuned from a CC0 Flemish base | CC0 |
| `sv_SE-nst-medium` (21 Nov 2026) | Swedish, one speaker (Nils) | NST Swedish dictation speech database, 22 kHz ([Språkbanken](https://www.nb.no/sprakbanken/), National Library of Norway), CC0; trained from scratch by KBLab | CC0 |
| `et_EE-news-medium` (21 Nov 2026) | Estonian, four speakers (Albert, Kalev, Mari, Vesta) | [Speech corpus of Estonian news sentences](https://metashare.ut.ee/repository/browse/speech-corpus-of-estonian-news-sentences/37b7c5d6a0d411eebb4773db10791bcfb0c0cf788d2d4030bfaf2f2e6e55dd8d/) (University of Tartu), CC BY; fine-tuned from hifi_tts_92 | CC BY 4.0 |
| `fi_FI-harri-medium` (20 Nov 2026) | Finnish, one speaker (Harri) | [Finnish single speaker speech dataset](https://www.kaggle.com/bryanpark/finnish-single-speaker-speech-dataset) (Kaggle), CC0 by the voice's card; fine-tuned from rdh | CC0 |
| `hu_HU-anna-medium`, `hu_HU-berta-medium`, `hu_HU-imre-medium` (20 Nov 2026) | Hungarian, one speaker each (Anna, Berta, Imre) | [OHF voice-datasets](https://github.com/OHF-Voice/voice-datasets), CC0; fine-tuned from hifi_tts_92 (anna, berta) and rdh (imre) | CC0 (hifi_tts_92 credited) |
| `nl_BE-rdh-medium` (20 Nov 2026) | Flemish, one speaker (Ruben in LuceVoce) | [dutch-vl-tts](https://github.com/r-dh/dutch-vl-tts), CC0; trained from scratch | CC0 |
| `nl_BE-nathalie-medium` (20 Nov 2026) | Flemish, one speaker (Nathalie) | [OHF voice-datasets](https://github.com/OHF-Voice/voice-datasets), CC0; fine-tuned from hifi_tts_92 | CC0 data, CC BY 4.0 base |
| `nl_BE-flemishguy-medium`, `nl_NL-alex-medium`, `nl_NL-pim-medium`, `nl_NL-ronnie-medium` (20 Nov 2026) | Flemish and Dutch, one speaker each (Wout, Alex, Pim, Ronnie) | OHF voice-datasets, CC0; fine-tuned from rdh | CC0 |
| `nl_NL-mls-medium` (20 Nov 2026) | Dutch, 52 speakers (LuceVoce offers four: Sanne, Lotte, Daan, Bram) | [Multilingual LibriSpeech](https://openslr.org/94/), Dutch (Pratap and others, 2020), CC BY 4.0 | CC BY 4.0 |
| `cs_CZ-jirka-medium`, `sk_SK-lili-medium` (20 Nov 2026) | Czech and Slovak, one speaker each (Jirka, Lili) | OHF voice-datasets, CC0; fine-tuned from hifi_tts_92 | CC0 data, CC BY 4.0 base |
| `de_DE-thorsten-medium`, `de_DE-thorsten_emotional-medium` (20 Nov 2026) | German, one speaker, plain and in eight moods (LuceVoce: Thorsten, and seven of the moods) | [Thorsten-Voice](https://github.com/thorstenMueller/Thorsten-Voice) by Thorsten Müller, CC0; fine-tuned from rdh, the moods from thorsten | CC0 |
| `de_DE-kerstin-medium` (20 Nov 2026) | German, one speaker (Kerstin) | [OHF voice-datasets](https://github.com/OHF-Voice/voice-datasets), CC0; fine-tuned from hifi_tts_92 | CC0 data, CC BY 4.0 base |
| `de_DE-mls-medium` (20 Nov 2026) | German, 236 speakers (LuceVoce offers four: Lena, Clara, Jonas, Felix) | [Multilingual LibriSpeech](https://openslr.org/94/), German (Pratap and others, 2020), CC BY 4.0 | CC BY 4.0 |
| `uk_UA-ukrainian_tts-medium` (19 Nov 2026, revision 42301ec) | Ukrainian, three speakers (Lada, Mykyta, Tetiana) | [Open Source Ukrainian Text-to-Speech datasets](https://github.com/egorsmkv/ukrainian-tts-datasets) by Yehor Smoliakov, texts from [uk-tts-dataset-text](https://github.com/egorsmkv/uk-tts-dataset-text), both Apache 2.0; the model card names CC0 data ([OHF-Voice/voice-datasets](https://github.com/OHF-Voice/voice-datasets)) | Apache 2.0 (CC0 by its card) |

The Piper voices repository and Piper itself are MIT (Copyright (c) 2022 Michael Hansen). What the licences ask and
how it is met: CC BY 4.0 and CC BY 3.0 allow passing the voices on, also in a commercial product, with credit to the creators, a
link to the licence and a statement of changes (none here); the credits are in `CREDITS.md`, here, and in LuceVoce's
own notices.

## whisper-ggml-1

Release: [whisper-ggml-1](https://github.com/itoderry/lucevoce-models/releases/tag/whisper-ggml-1)

The speech models LuceVoce on Windows offers for voice notes, to write down a note's words on the computer itself:
`ggml-base.bin`, `ggml-small.bin` and `ggml-medium.bin`, copied unchanged from whisper.cpp's model repository,
[ggerganov/whisper.cpp](https://huggingface.co/ggerganov/whisper.cpp) (revision 5359861c739e955e79d9a303bcbc70fb988958b1,
13 Nov 2026), with the release's `CREDITS.md`.

- The weights: [OpenAI Whisper](https://github.com/openai/whisper), MIT License, Copyright (c) 2022 OpenAI.
- The ggml format: [whisper.cpp](https://github.com/ggml-org/whisper.cpp), MIT License, Copyright (c) 2023-2024 The
  ggml authors.

The MIT License allows passing them on, also in a commercial product, with the copyright notice and the licence.

## translate-1

Release: [translate-1](https://github.com/itoderry/lucevoce-models/releases/tag/translate-1)

The language files of LuceVoce's on-device translation: for each direction (English with Romanian, French, German,
Spanish and Italian, both ways) a model (`model.<pair>.intgemm.alphas.bin.gz`), a short list
(`lex.50.50.<pair>.s2t.bin.gz`) and a vocabulary (`vocab.<pair>.spm.gz`), copied unchanged from Mozilla's
[firefox-translations-models](https://github.com/mozilla/firefox-translations-models), with the licence text
(`LICENSE-MPL-2.0.txt`); its credits are in `credits/translate-1-CREDITS.md`.

- Licence: Mozilla Public License 2.0 ("The model files are distributed under the MPL 2.0 license", Mozilla). The MPL
  allows passing the files on, also in a commercial product, with the licence and with the files themselves available
  in their source form: they are the source, unchanged, here and at Mozilla.

## dict-1

Release: [dict-1](https://github.com/itoderry/lucevoce-models/releases/tag/dict-1)

Dictionaries in more languages, which LuceVoce offers to download in Settings > Study > Dictionaries: eleven packs made
from wordnets (Italian twice, Spanish, Polish, Portuguese, Romanian, Dutch, Japanese, Chinese, German, Ukrainian), each
with its licence and credit inside, made by LuceVoce's `tools/dict_build/make_packs.sh` from sources pinned by SHA-256.
A synset without a definition of its own takes the Open English WordNet's (CC BY 4.0), marked "(English)". The sources,
licences and changes are in `credits/dict-1-CREDITS.md`.

- Licences: CC BY 3.0, ODC-BY, the WordNet licence and plWordNet's (Princeton's terms), all allowing use in a commercial
  product with credit; and CC BY-SA for the Portuguese, Romanian, Dutch, German and Ukrainian packs, which are
  adaptations shared under the same licence and never bundled in LuceVoce.

## Licence

Each release keeps its own licence: kokoro-coreml-1 and kokoro-onnx-1 under the Apache License, Version 2.0 (`LICENSE`
and `NOTICE.txt`), with CC BY credits for Kokoro's training data above; piper-1 under CC BY 4.0, and public domain for
the Spanish voice; whisper-ggml-1 under the MIT License; translate-1 under the Mozilla Public License 2.0; dict-1 under each source's licence
(`credits/dict-1-CREDITS.md`). Every file is
kept so that it can be part of a paid app: nothing here is under the GPL, the LGPL, or a non-commercial or
no-derivatives licence. Each file's size and SHA-256 are in LuceVoce's source, which checks every download against them.
