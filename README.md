# util_commands_ffmpeg

- [Documentacion ffmpeg](https://ffmpeg.org/documentation.html)

## Convertir MKV a MP4

**Sin perder el original**

```bash
ffmpeg -i file.mkv -codec copy file.mp4
```

>  La opción `-i` indicamos la ruta del fichero de vídeo que queremos procesar

## Recortar video

```bash
ffmpeg -i file.mkv -map 0 -default_mode infer_no_subs -ss 02:00:00 -to 02:30:00 -c copy file_short.mvk
```

> La opcion `-ss` indica el inicio del corte. Acepta varios formatos, mi recomendacion es usar HH:MM:SS. El valor `00:01:00` es 1 minuto.

> La opcion `-to` inica el final del corte. El formato es igual al anterior.

> `-c copy` indica que se copien todas las pistas de audio, video y subtitulos sin transcodificar.
