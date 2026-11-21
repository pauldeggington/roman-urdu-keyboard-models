# Roman Urdu Keyboard: model files

This repository holds the model files that the [Roman Urdu Keyboard](https://github.com/pauldeggington/roman-urdu-keyboard) Android app downloads. **You do not need to use them by hand**: the app fetches them, puts them together if they come in parts, and checks the result.

Both models are in the LiteRT-LM format that runs on a phone. The files are attached to releases, not stored in the repository itself.

| Model | Release | Files | Licence |
| --- | --- | --- | --- |
| Gemma 4 E2B | [`gemma-4-e2b`](../../releases/tag/gemma-4-e2b) | two halves, about 2.6 GB joined | Apache 2.0 |
| Gemma 3 1B | [`gemma-3-1b`](../../releases/tag/gemma-3-1b) | one file, about 0.6 GB | Gemma Terms of Use |

---

## Gemma 4 E2B

GitHub allows at most 2 GB per release file and this model is about 2.6 GB, so it is published as two equal halves.

| File | Size in bytes |
| --- | --- |
| `gemma-4-E2B-it.litertlm.part1` | 1,294,073,856 |
| `gemma-4-E2B-it.litertlm.part2` | 1,294,073,856 |

The joined file, `gemma-4-E2B-it.litertlm`, is 2,588,147,712 bytes. Its SHA-256 is:

```
181938105e0eefd105961417e8da75903eacda102c4fce9ce90f50b97139a63c
```

To put the parts together by hand, on Mac or Linux:

```
cat gemma-4-E2B-it.litertlm.part1 gemma-4-E2B-it.litertlm.part2 > gemma-4-E2B-it.litertlm
sha256sum gemma-4-E2B-it.litertlm
```

On Windows:

```
copy /b gemma-4-E2B-it.litertlm.part1+gemma-4-E2B-it.litertlm.part2 gemma-4-E2B-it.litertlm
certutil -hashfile gemma-4-E2B-it.litertlm SHA256
```

The hash printed must match the one above.

- Model: Gemma 4 E2B by Google ([google/gemma-4-E2B-it](https://huggingface.co/google/gemma-4-E2B-it)).
- This file: the LiteRT-LM build by litert-community ([litert-community/gemma-4-E2B-it-litert-lm](https://huggingface.co/litert-community/gemma-4-E2B-it-litert-lm)).
- Licence: **Apache License 2.0**, as stated on both pages above. The full text is in [`LICENSE`](LICENSE).

---

## Gemma 3 1B

| File | Size in bytes |
| --- | --- |
| `gemma3-1b-it-int4.litertlm` | 584,417,280 |

Its SHA-256 is:

```
1325ae366d31950f137c9c357b9fa89448b176d76998180c08ceaca78bba98be
```

- Model: Gemma 3 1B IT by Google ([google/Gemma-3-1B-IT](https://huggingface.co/google/Gemma-3-1B-IT)).
- This file: the LiteRT-LM build by litert-community ([litert-community/Gemma3-1B-IT](https://huggingface.co/litert-community/Gemma3-1B-IT)).
- Licence: the **Gemma Terms of Use**, https://ai.google.dev/gemma/terms. A copy is in [`GEMMA_TERMS.md`](GEMMA_TERMS.md).

**Gemma is provided under and subject to the Gemma Terms of Use found at ai.google.dev/gemma/terms.**

Anyone who uses or passes on this file is bound by the terms and by the [Gemma Prohibited Use Policy](https://ai.google.dev/gemma/prohibited_use_policy). Among other things, they must not use Gemma for the uses the policy forbids, and they must pass those restrictions on to anyone they give the model to. Read both documents before using the file outside the app.

---

## About these files

Every file here is byte for byte the one published on Hugging Face. The Gemma 4 file was only cut in two. Nothing in any file was changed.

These files are provided as they are, with no warranty. This repository is not affiliated with or endorsed by Google.
