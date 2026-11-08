# peeklingo-packs

Language packs that the PeekLingo desktop app downloads on demand: one dictionary and one local translation model per language pair.

Los packs de idioma que la app PeekLingo descarga a demanda: un diccionario y un modelo de traducción local por cada par de idiomas.

The files live in the [`packs` release](../../releases/tag/packs). `catalog.json` lists each file with its size and SHA-256; the app verifies every file before installing it.

## Pairs

| Pair | Dictionary | Translator |
|---|---|---|
| EN→ES | Wiktionary (en, es) via kaikki.org | Helsinki-NLP/opus-mt-en-es |
| EN→FR | Wiktionary (en, fr) via kaikki.org | Helsinki-NLP/opus-mt-en-fr |

## Licenses

- Dictionaries: **CC BY-SA 4.0 and GFDL** (Wiktionary contributors). They are derived works: keep the same license and the attribution in [ATTRIBUTIONS.md](ATTRIBUTIONS.md) if you redistribute them. The word order uses FrequencyWords by Hermit Dave (CC BY-SA 4.0).
- Translation models: **Apache-2.0** (Helsinki-NLP opus-mt, converted to int8 for CTranslate2). Their training data is OPUS, with mixed corpus licenses.
- `peeklingo-mt.exe`: the local translator process of PeekLingo (CTranslate2, MIT; oneDNN and SentencePiece, Apache-2.0).
