# Documentación del Código

En este archivo de código, tenemos varias enumeraciones públicas (public enums) que se utilizan para definir ciertos estados y modos de operación en un reproductor de música.

## Enumeraciones

1. `enumFormTypes`: Esta enumeración determina el tipo de reproductor de música.

   - `[MidiPlayer]`: Esta es una opción para un reproductor de música MIDI.
   - `[Mp3Player]`: Esta es una opción para un reproductor de música MP3.

2. `enumCDMode`: Esta enumeración determina el modo de reproducción para un CD.

   - `[RandomMode]`: Este modo reproduce las canciones del CD en un orden aleatorio.
   - `[LoopMode]`: Este modo reproduce las canciones del CD en un ciclo continuo.

3. `enumPlayStates`: Esta enumeración determina el estado de reproducción actual.

   - `Paused`: Este estado indica que la reproducción está pausada.
   - `Stopped`: Este estado indica que la reproducción está detenida.
   - `Playing`: Este estado indica que una canción se está reproduciendo.
   - `MediaEnded`: Este estado indica que la reproducción ha llegado al final de la canción o lista de reproducción.

4. `enumPlayMode`: Esta enumeración determina el modo de reproducción de las canciones.

   - `[PlaySingleTrack]`: Este modo reproduce una sola canción y luego se detiene.
   - `[AutoNextTrack]`: Este modo reproduce automáticamente la siguiente canción en la lista de reproducción.
   - `[Shuffle]`: Este modo reproduce las canciones en un orden aleatorio.

5. `enumPlaylistMode`: Esta enumeración determina cómo se maneja la repetición en una lista de reproducción.

   - `[RepeatPlaylist]`: Este modo repite toda la lista de reproducción.
   - `[RepeatSingleTrack]`: Este modo repite una única canción.

6. `enumMediaMode`: Esta enumeración determina el tipo de medio que se está reproduciendo.

   - `[MidiMediaMode]`: Este modo es para la reproducción de archivos MIDI.
   - `[MP3MediaMode]`: Este modo es para la reproducción de archivos MP3.
   - `[CDMediaMode]`: Este modo es para la reproducción de CDs de música.
   - `[SidMediaMode]`: Este modo es para la reproducción de archivos SID.
   - `[MusMediaMode]`: Este modo es para la reproducción de archivos MUS.