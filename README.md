# Roman Urdu Keyboard: model files

This repository holds the model files that the [Roman Urdu Keyboard](https://github.com/pauldeggington/roman-urdu-keyboard) Android app downloads. **You do not need to use them by hand**: the app fetches both parts, puts them together and checks the result.

The model is **Gemma 4 E2B**, in the LiteRT-LM format that runs on a phone. GitHub allows at most 2 GB per release file and the model is about 2.6 GB, so it is published as two equal halves.

## Files

They are attached to the [`gemma-4-e2b` release](../../releases/tag/gemma-4-e2b), not stored in the repository itself.

| File | Size in bytes |
| --- | --- |
| `gemma-4-E2B-it.litertlm.part1` | 1,294,073,856 |
| `gemma-4-E2B-it.litertlm.part2` | 1,294,073,856 |

The joined file, `gemma-4-E2B-it.litertlm`, is 2,588,147,712 bytes. Its SHA-256 is:

```
181938105e0eefd105961417e8da75903eacda102c4fce9ce90f50b97139a63c
```

## Putting the parts together by hand

On Mac or Linux:

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

## Where the model comes from

- Model: Gemma 4 E2B by Google ([google/gemma-4-E2B-it](https://huggingface.co/google/gemma-4-E2B-it)).
- This file: the LiteRT-LM build by litert-community ([litert-community/gemma-4-E2B-it-litert-lm](https://huggingface.co/litert-community/gemma-4-E2B-it-litert-lm)).
- The file is byte for byte the one published there. It was only cut in two. Nothing in it was changed.

## Licence

The model is released under the **Apache License 2.0**, as stated on both Hugging Face pages above. The full text is in [`LICENSE`](LICENSE). It applies to the model files in this repository's releases.

These files are provided as they are, with no warranty. This repository is not affiliated with or endorsed by Google.
