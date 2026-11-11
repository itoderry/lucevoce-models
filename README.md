# LuceVoce models

Model files that LuceVoce, an app that reads books aloud, downloads on request. The files are attached to this
repository's releases; the repository itself holds only this description and the licence.

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

## Licence

The files in the releases are licensed under the Apache License, Version 2.0 (see `LICENSE` and `NOTICE.txt`).
