# Documentación de código ModPlaylist

Este módulo de código, llamado "ModPlaylist", contiene varias funciones relacionadas con la manipulación de listas de reproducción de audio. Las funciones específicas y su descripción se detallan a continuación:

## Funciones

### OpenAplPlaylist(strPlaylistFile As String)

Esta función abre una lista de reproducción .apl. La lista de reproducción se pasa como un argumento de cadena `strPlaylistFile`. La lista de reproducción es luego leída y añadida a `Form_Playlist` utilizando la función `AddToPlaylist`.

### OpenWplPlaylist(FileName As String)

Esta función abre una lista de reproducción .wpl. La lista de reproducción es leída línea por línea y cualquier línea que contenga la etiqueta `<media` es procesada para extraer el nombre del archivo de medios. Estos archivos de medios se añaden luego a la lista de reproducción en `Form_Playlist`.

### OpenM3uPlaylist(strPlaylistFile As String, Optional TargetListbox As ListBox)

Esta función abre una lista de reproducción .m3u. Analiza la lista de reproducción línea por línea, y añade cada archivo a la lista de reproducción en `Form_Playlist`. Si una línea comienza con `#EXTM3U`, se imprime "Playlist Type: M3U". Si una línea comienza con `#EXTINF:`, se imprime la información de la línea.

### OpenPlsPlaylist(strPlaylistFile As String, Optional TargetListbox As ListBox)

Esta función abre una lista de reproducción .pls. Lee el número de entradas en la lista de reproducción del archivo .pls y luego añade cada archivo a la lista de reproducción en `Form_Playlist`.

Cada una de estas funciones utiliza la función `Extensions.FileGetContents` para leer el contenido del archivo de lista de reproducción y la función `Form_Playlist.AddToPlaylist` para añadir los archivos de medios a la lista de reproducción.

Todas estas funciones son públicas, lo que significa que pueden ser accedidas desde cualquier módulo de código en el proyecto.