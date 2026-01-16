# DeepASMR Testset

Public testset JSONs for two datasets:
- whisper40 (Chinese)
- CHAINs (English)

Each dataset provides four tasks:
- A2A: ASMR whisper → ASMR whisper
- A2N: ASMR whisper → normal speech
- N2A: normal speech → ASMR whisper
- N2N: normal speech → normal speech

## File locations
- Testsets: `test/<dataset>/*_testset.json`
- `<dataset>` is `CHAINs` or `whisper40`.

## Item schema
Each sample is an object with fields in this order:
- key: string identifier starting from "0".
- transcription: target text.
- prompt_transcription: text of the prompt audio.
- prompt_audio: dataset-rooted relative path to the prompt audio
- ground_truth: dataset-rooted relative path to the target audio.

Example:
```json
[
  {
    "key": "0",
    "transcription": "Example target text",
    "prompt_transcription": "Example prompt text",
    "prompt_audio": "CHAINs/whsp/data/whsp/irm11/irm11_s26_whsp.wav",
    "ground_truth": "CHAINs/whsp/data/whsp/irm11/irm11_s01_whsp.wav"
  }
]
```