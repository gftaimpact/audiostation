# Documentación del Módulo: AudiostationMP3Player

```vba
Attribute VB_Name = "AudiostationMP3Player"
Option Explicit
```

Este módulo agrega funcionalidad del reproductor MP3. Creado por Sibra-Soft (Alex van den Berg) el 04-10-2021 y la última modificación fue el 29-03-2022.

## Variables Públicas

```vba
Public MediaPlaylistMode As enumPlaylistMode
Public MediaPlayMode As enumPlayMode
Public MediaPlaystate As enumPlayStates

Public MediaPlaylist As New LocalStorage

Public ShowElapsedTime As Boolean
Public CurrentMediaFilename As String
Public CurrentTrackNumber As Integer
```

Estas variables representan el estado actual del reproductor MP3, incluyendo el modo de reproducción, el estado de reproducción, la lista de reproducción actual, si se muestra el tiempo transcurrido, el nombre del archivo de medios actual y el número de pista actual.

## Métodos Públicos

### Init

```vba
Public Sub Init()
MediaPlaystate = Stopped
MediaPlaylistMode = RepeatPlaylist
MediaPlayMode = PlaySingleTrack
AudiostationMP3Player.ShowElapsedTime = True
End Sub
```

Este método inicializa el reproductor MP3 con valores predeterminados.

### Rewind

```vba
Public Sub Rewind()
Dim pos As Long

pos = BASS_ChannelBytes2Seconds(chan, BASS_ChannelGetPosition(chan, BASS_POS_BYTE))

Call BASS_ChannelSetPosition(chan, BASS_ChannelSeconds2Bytes(chan, pos + 5), BASS_POS_BYTE)
End Sub
```

Este método rebobina la pista actual en 5 segundos.

### Forward

```vba
Public Sub Forward()
Dim pos As Long

pos = BASS_ChannelBytes2Seconds(chan, BASS_ChannelGetPosition(chan, BASS_POS_BYTE))

Call BASS_ChannelSetPosition(chan, BASS_ChannelSeconds2Bytes(chan, pos - 5), BASS_POS_BYTE)
End Sub
```

Este método adelanta la pista actual en 5 segundos.

### Pause

```vba
Public Sub Pause()
Call BASS_ChannelPause(chan)
MediaPlaystate = Paused
End Sub
```

Este método pausa la reproducción actual.

### StartPlay

```vba
Public Sub StartPlay()
//...
End Sub
```

Este método comienza la reproducción de la pista actual. Si la pista está en pausa, la reanuda. Si no hay pista actual, comienza a reproducir la primera pista en la lista de reproducción.

### StopPlay

```vba
Public Sub StopPlay()
Call BASS_ChannelStop(chan)
MediaPlaystate = Stopped
End Sub
```

Este método detiene la reproducción actual.

### NextTrack

```vba
Public Sub NextTrack(Optional TrackNumber As Integer, Optional Force = False)
//...
End Sub
```

Este método avanza a la siguiente pista en la lista de reproducción. Se puede especificar un número de pista opcional para saltar directamente a esa pista.

### PreviousTrack

```vba
Public Sub PreviousTrack()
//...
End Sub
```

Este método retrocede a la pista anterior en la lista de reproducción.