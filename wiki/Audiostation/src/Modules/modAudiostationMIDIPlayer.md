# Documentación del Código

```vba
Attribute VB_Name = "AudiostationMIDIPlayer"
Option Explicit
```
El módulo `AudiostationMIDIPlayer` proporciona funcionalidad de reproductor MIDI. Fue creado por Alex van den Berg de Sibra-Soft el 04-10-2021 y fue modificado por última vez el 25-10-2021.

Declara varias funciones y constantes utilizadas para interactuar con una ventana de consola y enviar mensajes a la misma.

## Variables
* `MidiFilename` (Público): Almacena el nombre del archivo MIDI que se está reproduciendo.
* `MidiTrackNr` (Público): Almacena el número de pista MIDI actual.
* `MidiPlaystate` (Público): Almacena el estado actual de la reproducción MIDI.
* `MidiPlaylist` (Público): Almacena la lista de reproducción MIDI actual.
* `ConsoleWindow` (Público): Almacena el identificador de la ventana de la consola.

## Métodos

* `StartMidiPlayback()`: Inicia la reproducción MIDI. Detiene cualquier otra reproducción de medios antes de iniciar la reproducción MIDI. También maneja la lógica para la reproducción de diferentes tipos de archivos de medios.
* `StopMidiPlayback()`: Detiene la reproducción MIDI. Si el medio actual es de tipo SID, envía un mensaje WM_CLOSE a la ventana de la consola.
* `PauseMidiPlayback()`: Pausa la reproducción MIDI y actualiza el estado de reproducción a "Pausado".
* `NextMidiTrack()`: Avanza a la siguiente pista en la lista de reproducción MIDI y comienza a reproducirla.
* `PreviousMidiTrack()`: Retrocede a la pista anterior en la lista de reproducción MIDI y comienza a reproducirla.
* `ForwardMidi10Seconds()`: Avanza la reproducción MIDI en 10 segundos.
* `RewindMidi10Seconds()`: Retrocede la reproducción MIDI en 10 segundos.