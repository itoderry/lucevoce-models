# Piper voices hosted for LuceVoce (release piper-1)

Voice models copied unchanged from the Piper voices repository, https://huggingface.co/rhasspy/piper-voices
(revision e7229f7d33a10e145e109b886d661984201ac3c4), on 12 Nov 2026. Each voice keeps its own licence, given in its model card
(attached as <voice>.MODEL_CARD). Only voices trained from scratch on data that allows commercial use are here.

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

## es_ES-carlfm-x_low (Spanish, male)

- Model: Piper voice "carlfm (x_low)" from rhasspy/piper-voices, trained from scratch.
- Data: carlfm01 my-speech-datasets, https://github.com/carlfm01/my-speech-datasets, public domain.
- Licence: public domain. No changes made.

The Piper voices repository itself is MIT. Sizes and SHA-256 of every model file are in LuceVoce's source
(src/voice/piper.cpp), which checks each download against them.
