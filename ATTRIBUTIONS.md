# Atribuciones de datos

Los packs de diccionario son datos separados del ejecutable, cada uno con su licencia en `meta` (`license`, `source`, `frequency_source`).

## Packs de diccionario (`pack-<origen>-<destino>.db`)

Cada par se arma igual: el Wiktionary en inglés aporta definiciones, formas, IPA, ejemplos y traducciones; el Wiktionary del idioma de destino (si existe el extracto en kaikki.org) aporta definiciones y ejemplos en ese idioma. Pares publicados: EN→ES y EN→FR (Wiktionary en francés, `fr-extract`). El detalle de abajo describe el pack EN→ES y vale igual para los demás.

| Contenido | Fuente | Licencia |
|---|---|---|
| Definiciones, formas, IPA, traducciones y ejemplos en inglés | Wiktionary en inglés, extraído por [kaikki.org](https://kaikki.org) (wiktextract) | CC BY-SA 4.0 y GFDL |
| Definiciones y ejemplos en español | Wiktionary en español, extraído por kaikki.org | CC BY-SA 4.0 y GFDL |
| Orden por frecuencia | FrequencyWords de Hermit Dave, derivada de OpenSubtitles | CC BY-SA 4.0 (contenido) |

El pack es una obra derivada de esas fuentes y se distribuye bajo **CC BY-SA 4.0**: quien lo redistribuya con cambios debe mantener la misma licencia y esta atribución.
El texto de las entradas pertenece a los colaboradores de Wiktionary; el historial de cada entrada está en el sitio de origen.

Pendiente de revisión legal del titular: la lista de frecuencias procede de subtítulos de OpenSubtitles; solo se usa el orden de las palabras (un número por palabra), no el texto de los subtítulos.

## Pack del traductor local (`mt-<origen>-<destino>/` y `peeklingo-mt.exe`)

| Contenido | Fuente | Licencia |
|---|---|---|
| Modelo de traducción por par (EN→ES, EN→FR) | `Helsinki-NLP/opus-mt-en-es` y `opus-mt-en-fr` (Universidad de Helsinki), convertidos por nosotros a int8 con `ct2-transformers-converter` | Apache-2.0 |
| Datos de entrenamiento del modelo | OPUS ([opus.nlpl.eu](https://opus.nlpl.eu)) | licencias mixtas por corpus; el modelo se redistribuye bajo la licencia que declara su autor |
| Motor de inferencia | CTranslate2 (MIT), oneDNN (Apache-2.0), SentencePiece (Apache-2.0) | ver `THIRD_PARTY.md` |

La calidad es de ayuda para aprender, no de traducción profesional (`docs/spikes/s6-mt-local.md`).
