# Fixture audio

All clips are WAV, 16 kHz, mono, signed 16-bit PCM. Each is under 1 MB.

## Synthetic voice

| File | Length | How it was made |
| - | - | - |
| `synthetic-1.wav` | 9.3 s | [Piper TTS](https://github.com/rhasspy/piper), voice `en_US-ljspeech-medium`, run locally, then converted to 16 kHz mono WAV |

The text was written for this repo. The Piper voice is trained on LJ Speech,
which is in the public domain (see the voice model card).

## Human speech

| File | Length | Source |
| - | - | - |
| `real-1.wav` | 11.4 s | LibriSpeech `dev-clean`, speaker 2277, utterances `2277-149896-0000` and `2277-149896-0002` joined |
| `real-2.wav` | 13.8 s | LibriSpeech `dev-clean`, speaker 3752, utterances `3752-4943-0007` and `3752-4943-0008` joined |

LibriSpeech is licensed CC BY 4.0. Credit: Vassil Panayotov, Guoguo Chen,
Daniel Povey and Sanjeev Khudanpur, "LibriSpeech: an ASR corpus based on public
domain audio books", ICASSP 2015. The recordings are LibriVox volunteer
readings of public domain books. See https://www.openslr.org/12.

The clips were fetched from the `openslr/librispeech_asr` dataset on Hugging
Face, decoded from FLAC, joined with `ffmpeg` and converted to 16 kHz mono WAV.
