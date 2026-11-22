# Piper voices hosted for LuceVoce (release piper-1)

Voice models copied unchanged from the Piper voices repository, https://huggingface.co/rhasspy/piper-voices
(revision e7229f7d33a10e145e109b886d661984201ac3c4 on 12 Nov 2026; the voices added on 19 Nov 2026 from revision
42301ec547bc2939386cf0ae9f9050ca05b1d3af, where the first three are unchanged). Each voice keeps its own licence, given in
its model card (attached as <voice>.MODEL_CARD). Only voices whose data, and whose base model when fine-tuned, allow
commercial use are here.

Two base models some of these voices were fine-tuned from (both trained from scratch):
- rdh (nl_BE-rdh-medium): the dutch-vl-tts data of one Flemish speaker, https://github.com/r-dh/dutch-vl-tts, CC0 1.0.
- hifi_tts_92 (en_US-hifi_tts_92-medium): the voice of Cori Samuel, reader 92 of the Hi-Fi Multi-Speaker English TTS
  Dataset (NVIDIA Corporation; Bakhturina, Lavrukhin, Ginsburg and Zhang, Interspeech 2021),
  https://www.openslr.org/109/, CC BY 4.0, https://creativecommons.org/licenses/by/4.0/.

## fr_FR-mls-medium (French, 125 speakers; LuceVoce offers four of them)

- Model: Piper voice "mls (medium)" from rhasspy/piper-voices, trained from scratch.
- Data: Multilingual LibriSpeech (MLS), French, https://openslr.org/94/ (Pratap et al., 2020), CC BY 4.0.
- Licence: CC BY 4.0, https://creativecommons.org/licenses/by/4.0/. No changes made.

## it_IT-serena-high (Italian, female)

- Model: Piper voice "serena (high)" from rhasspy/piper-voices, trained from scratch.
- Data: serena-synthetic-it-27h by Marco Baccarani, https://huggingface.co/datasets/committa/serena-synthetic-it-27h,
  CC BY 4.0: synthetic speech made with Qwen3-TTS (Apache 2.0) from sentences adapted from Tatoeba
  (https://tatoeba.org), CC BY 2.0 FR.
- Licence: CC BY 4.0, https://creativecommons.org/licenses/by/4.0/. No changes made.

## Added on 19 Nov 2026

- ro_RO-mihai-medium (Romanian, male): OHF voice-datasets, https://github.com/OHF-Voice/voice-datasets, CC0;
  fine-tuned from rdh. Licence: CC0.
- pt_BR-cadu-medium, pt_BR-jeff-medium (Brazilian Portuguese, male): OHF voice-datasets, CC0; fine-tuned from rdh.
  Licence: CC0.
- pt_BR-faber-medium (Brazilian Portuguese, male): OHF voice-datasets, CC0; fine-tuned from hifi_tts_92 (CC BY 4.0,
  credit above).
- fr_FR-siwis-medium (French, female): SIWIS French Speech Synthesis Database (University of Edinburgh),
  https://datashare.is.ed.ac.uk/handle/10283/2353, CC BY 4.0; fine-tuned from hifi_tts_92. No changes made.
- it_IT-paola-medium (Italian, female): OHF voice-datasets, CC0; fine-tuned from hifi_tts_92.
- it_IT-serena-medium (Italian, female): serena-synthetic-it-27h by Marco Baccarani (as serena-high above), CC BY 4.0;
  trained from scratch. No changes made.
- es_ES-davefx-medium (Spanish, male): OHF voice-datasets, CC0; fine-tuned from rdh.
- es_ES-sharvard-medium (Spanish, a male and a female speaker): the Sharvard corpus,
  https://datashare.ed.ac.uk/handle/10283/574 (Aubanel, García Lecumberri, Cooke and others, International Journal of
  Audiology 2014), CC BY 3.0, https://creativecommons.org/licenses/by/3.0/; fine-tuned from hifi_tts_92. No changes
  made.
- es_MX-ald-medium (Mexican Spanish, male): Ald Mexican Spanish speech dataset,
  https://huggingface.co/datasets/rmcpantoja/Ald_Mexican_Spanish_speech_dataset, the Unlicense; fine-tuned from rdh.
- pl_PL-darkman-medium (Polish, male; LuceVoce calls it Darek): OHF voice-datasets, CC0; fine-tuned from rdh.
  Licence: CC0.
- pl_PL-gosia-medium (Polish, female; Gosia): OHF voice-datasets, CC0; fine-tuned from hifi_tts_92 (CC BY 4.0, credit
  above). Added on 20 Nov 2026.
- nl_BE-rdh-medium (Flemish, male; LuceVoce calls it Ruben): dutch-vl-tts by r-dh, https://github.com/r-dh/dutch-vl-tts,
  CC0 1.0; trained from scratch (the rdh base model itself). Licence: CC0. Added on 20 Nov 2026.
- nl_BE-nathalie-medium (Flemish, female; Nathalie): OHF voice-datasets, CC0; fine-tuned from hifi_tts_92 (CC BY 4.0,
  credit above). Added on 20 Nov 2026.
- nl_BE-flemishguy-medium (Flemish, male; Wout), nl_NL-alex-medium (Alex), nl_NL-pim-medium (Pim),
  nl_NL-ronnie-medium (Ronnie) (Dutch, male): OHF voice-datasets, CC0; fine-tuned from rdh. Licence: CC0. Added on
  20 Nov 2026.
- nl_NL-mls-medium (Dutch, 52 readers; LuceVoce offers four, named Sanne, Lotte, Daan and Bram): Multilingual
  LibriSpeech (MLS), Dutch, https://openslr.org/94/ (Pratap et al., 2020), CC BY 4.0, recordings from LibriVox
  volunteers; trained from scratch. Licence: CC BY 4.0, https://creativecommons.org/licenses/by/4.0/. No changes made.
  Added on 20 Nov 2026.
- cs_CZ-jirka-medium (Czech, male; Jirka) and sk_SK-lili-medium (Slovak, female; Lili): OHF voice-datasets, CC0;
  fine-tuned from hifi_tts_92 (CC BY 4.0, credit above). Added on 20 Nov 2026.
- fi_FI-harri-medium (Finnish, male; Harri): the Finnish single-speaker speech dataset on Kaggle
  (https://www.kaggle.com/bryanpark/finnish-single-speaker-speech-dataset), CC0 by the voice's model card; fine-tuned
  from rdh (CC0). Licence: CC0. Added on 20 Nov 2026.
- no_NO-talesyntese-medium (Norwegian, female; Ingrid): the NST Norwegian speech data, Språkbanken at the National Library
- zh_CN-chaowen-medium (Chinese, male; Chaowen): the OHF-Voice voice-datasets recording of the speaker 超文 (chaowen), https://github.com/OHF-Voice/voice-datasets, CC0; fine-tuned from the hifi_tts_92 base model (Hi-Fi TTS, LibriVox reader 92, CC BY 4.0, https://www.openslr.org/109/). Licence: CC0, with the Hi-Fi TTS credit. Added on 22 Nov 2026.
- eu_ES-antton-medium (Basque, male; Antton): the Antton dataset of the Itzune project, https://huggingface.co/datasets/itzune/antton-dataset, CC BY 4.0; fine-tuned from a CC0 Flemish base model. Licence: CC BY 4.0. Added on 22 Nov 2026.
- eu_ES-maider-medium (Basque, female; Maider): the Maider dataset of the Itzune project, https://huggingface.co/datasets/itzune/maider-dataset, CC BY 4.0; fine-tuned from the hifi_tts_92 base model (Hi-Fi TTS, CC BY 4.0). Licence: CC BY 4.0. Added on 22 Nov 2026.
- kk_KZ-issai-high (Kazakh, six speakers; Nurlan, Iseke, Aigerim, Raya, Dana, Aliya): the Kazakh text-to-speech corpus of the Institute of Smart Systems and Artificial Intelligence (ISSAI), Nazarbayev University, https://github.com/IS2AI/Kazakh_TTS, CC BY 4.0; trained from scratch. Licence: CC BY 4.0. Added on 22 Nov 2026.
- ne_NP-chitwan-medium (Nepali, male; Chitwan): the OHF-Voice voice-datasets Nepali recording, https://github.com/OHF-Voice/voice-datasets, CC0; fine-tuned from a CC0 Flemish base model. Licence: CC0. Added on 22 Nov 2026.
  of Norway, https://www.nb.no/sprakbanken/ (originally made by Nordisk språkteknologi), CC0 1.0 (catalogue licence "CC Zero");
  fine-tuned from a CC0 Flemish base model. Licence: CC0. Added on 21 Nov 2026.
- sv_SE-nst-medium (Swedish, male; Nils): the NST Swedish dictation speech database (22 kHz), Språkbanken at the National
  Library of Norway, https://www.nb.no/sprakbanken/ (originally made by Nordisk språkteknologi), CC0 1.0 (catalogue
  licence "CC Zero"); trained from scratch by KBLab at the National Library of Sweden. Licence: CC0. Added on 21 Nov 2026.
- et_EE-news-medium (Estonian, four speakers: Albert and Kalev, male; Mari and Vesta, female): the Speech corpus of Estonian
  news sentences, University of Tartu, https://metashare.ut.ee/repository/browse/speech-corpus-of-estonian-news-sentences/37b7c5d6a0d411eebb4773db10791bcfb0c0cf788d2d4030bfaf2f2e6e55dd8d/
  (paper: https://arxiv.org/abs/2010.02636), CC BY ("Available - Unrestricted Use" on META-SHARE); fine-tuned from
  hifi_tts_92 (CC BY 4.0, credit above). Licence: CC BY, https://creativecommons.org/licenses/by/4.0/. No changes made.
  Added on 21 Nov 2026.
- hu_HU-anna-medium (Hungarian, female; Anna) and hu_HU-berta-medium (Hungarian, female; Berta): OHF voice-datasets,
  https://github.com/OHF-Voice/voice-datasets, CC0; fine-tuned from hifi_tts_92 (CC BY 4.0, credit above). Added on
  20 Nov 2026.
- hu_HU-imre-medium (Hungarian, male; Imre): OHF voice-datasets, CC0; fine-tuned from rdh. Licence: CC0. Added on
  20 Nov 2026.
- de_DE-thorsten-medium (German, male; Thorsten): the Thorsten-Voice recordings by Thorsten Müller,
  https://github.com/thorstenMueller/Thorsten-Voice, CC0; fine-tuned from rdh. Licence: CC0. Added on 20 Nov 2026.
- de_DE-thorsten_emotional-medium (German, Thorsten in eight moods; LuceVoce offers seven): Thorsten-Voice, CC0;
  fine-tuned from thorsten. Licence: CC0. Added on 20 Nov 2026.
- de_DE-kerstin-medium (German, female; Kerstin): OHF voice-datasets, CC0; fine-tuned from hifi_tts_92 (CC BY 4.0,
  credit above). Added on 20 Nov 2026.
- de_DE-mls-medium (German, 236 readers; LuceVoce offers four, named Lena, Clara, Jonas and Felix): Multilingual
  LibriSpeech (MLS), German, https://openslr.org/94/ (Pratap et al., 2020), CC BY 4.0, recordings from LibriVox
  volunteers; trained from scratch. Licence: CC BY 4.0, https://creativecommons.org/licenses/by/4.0/. No changes made.
  Added on 20 Nov 2026.
- uk_UA-ukrainian_tts-medium (Ukrainian, three speakers: Lada, Mykyta, Tetiana; it reads letters, "phoneme_type":
  "text"): its model card names OHF voice-datasets, CC0, which holds no Ukrainian data; its speakers are the Lada,
  Mykyta and Tetiana recordings of Open Source Ukrainian Text-to-Speech datasets by Yehor Smoliakov,
  https://github.com/egorsmkv/ukrainian-tts-datasets, with texts from https://github.com/egorsmkv/uk-tts-dataset-text,
  both under the Apache License 2.0, https://www.apache.org/licenses/LICENSE-2.0; trained from scratch. Credited here
  under the Apache License 2.0. No changes made.

The Piper voices repository itself is MIT. Sizes and SHA-256 of every model file are in LuceVoce's source
(src/voice/piper.cpp), which checks each download against them.
