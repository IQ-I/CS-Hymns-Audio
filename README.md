# C&S Hymns — Yorùbá hymn audio

Pre-generated Yorùbá audio for the C&S Hymns app (Yorùbá hymnal + Akunleko), and the app's remote
on/off switch for the Yorùbá voice (see **[KILL_SWITCH.md](KILL_SWITCH.md)**).

- `config/voice.json`: the remote switch + where the audio lives.
- `v1/index.json`: which hymns have audio.
- `v1/hymns/<y|cns>/<number>.json`: per-hymn verse/line timings, file names, sizes, sha256.
- Audio files (AAC 64 kbps mono, 22.05 kHz, one file per hymn per voice) are attached to the Releases
  `yo-voice-v1-male` and `yo-voice-v1-female`.

## Voices
- **male** (Ohùn Ọkùnrin): the built-in speaker of [multilingual-tts/VITS-OpenBible-Yoruba](https://huggingface.co/multilingual-tts/VITS-OpenBible-Yoruba).
- **female** (Ohùn Obìnrin): the same voice, pitch-shifted up 4 semitones.

The audio was rendered from tone-marked text. The tone marks were added with machine help
(`Davlan/mT5_base_yoruba_adr` plus hymn-vocabulary rules) and are **under review by Yorùbá speakers**.
The on-screen lyrics in the app are unchanged.

## Licence and credits
The audio and timing data in this repository are released under **CC BY-SA 4.0** (see `LICENSE`).

- The voice model is VITS-OpenBible-Yoruba by multilingual-tts (CC BY-SA 4.0), trained on the Open.Bible Yorùbá recordings and text.
- The original work by Biblica, Inc. is available for free at www.biblica.com and open.bible.
- Changes: synthetic speech generated from C&S hymn texts; the female voice is pitch-shifted.
