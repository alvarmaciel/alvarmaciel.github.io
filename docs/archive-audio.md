# Audio desde Archive.org en Hugo

Esta guía documenta cómo publicar un post/episodio con audio alojado en Archive.org y que también funcione bien en el RSS de podcast.

## 1. ID de Archive.org

Si la URL es:

```txt
https://archive.org/details/mi-audio-2026
```

El ID es:

```txt
mi-audio-2026
```

La metadata está en:

```txt
https://archive.org/metadata/mi-audio-2026
```

## 2. Usar el script helper

Desde la raíz del repo:

```bash
python3 scripts/archive_metadata.py mi-audio-2026
```

También podés pasarle un Markdown que ya tenga `archive.id`:

```bash
python3 scripts/archive_metadata.py content/media/lento_es_normal/mi-episodio/index.md
```

El script imprime YAML listo para copiar al front matter:

- `image`
- `archive`
- `duration`
- `audio`
- `enclosures`
- `tags`
- shortcode para el reproductor

## 3. Front matter recomendado

```yaml
---
title: "Título del episodio"
date: 2026-07-17T18:00:00-03:00
description: "Descripción visible."
rss_description: "Descripción para RSS."
draft: false
duration: "51:26"
image: "https://archive.org/download/ID/imagen.jpg"
archive:
  id: "ID"
  url: "https://archive.org/details/ID"
  image: "https://archive.org/download/ID/imagen.jpg"
audio:
  - "https://archive.org/download/ID/audio.mp3"
enclosures:
  - url: "https://archive.org/download/ID/audio.mp3"
    type: "audio/mpeg"
    length: 123456789
tags:
  - "tecnología"
  - "radio"
---

{{< archiveaudio id="ID" >}}
```

## 4. Diferencia entre `audio`, `enclosures` y `duration`

### `audio`

Debe ser una lista simple de URLs:

```yaml
audio:
  - "https://archive.org/download/ID/audio.mp3"
```

No usar objetos dentro de `audio`, porque algunos temas Hugo usan `.Params.audio` para OpenGraph y esperan strings.

Evitar:

```yaml
audio:
  - url: "https://archive.org/download/ID/audio.mp3"
    type: "audio/mpeg"
```

### `enclosures`

Contiene metadata para RSS/podcast:

```yaml
enclosures:
  - url: "https://archive.org/download/ID/audio.mp3"
    type: "audio/mpeg"
    length: 123456789
```

`length` es el tamaño del archivo en bytes.

En Archive.org sale de:

```txt
files[].size
```

### `duration`

Es la duración del episodio:

```yaml
duration: "51:26"
```

En Archive.org sale de:

```txt
files[].length
```

Ese valor está en segundos y el script lo convierte a `MM:SS` o `H:MM:SS`.

## 5. Reproductor embebido

Para mostrar el reproductor de Archive.org dentro del post:

```md
{{< archiveaudio id="ID" >}}
```

También se puede ajustar altura:

```md
{{< archiveaudio id="ID" height="80" >}}
```

## 6. RSS de Lento es normal

El RSS custom está en:

```txt
layouts/media/lento_es_normal/rss.xml
```

El template usa preferentemente:

```yaml
enclosures:
```

Si no existe, usa como fallback:

```yaml
audio:
```

Esto permite que episodios viejos sigan funcionando y que episodios nuevos tengan `length` y `type` correctos para podcast clients.
