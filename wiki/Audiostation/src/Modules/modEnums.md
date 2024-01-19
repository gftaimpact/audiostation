# Documentação do Código

## Arquivo: ModEnums

Este arquivo define várias enumerações utilizadas em todo o projeto. As enumerações são um tipo especial de dados que consistem em um conjunto de valores nomeados. Eles são usados quando se quer que uma variável possa ter um (e apenas um) de um pequeno grupo de valores possíveis.

## Enumerações

### enumFormTypes

A enumeração `enumFormTypes` é usada para identificar os tipos de formulários que existem no sistema. Os valores possíveis são:

- `MidiPlayer`: Representa um formulário do tipo Midi Player.
- `Mp3Player`: Representa um formulário do tipo Mp3 Player.

### enumCDMode

A enumeração `enumCDMode` é usada para identificar os modos de reprodução de um CD. Os valores possíveis são:

- `RandomMode`: Modo de reprodução aleatório.
- `LoopMode`: Modo de reprodução em loop.

### enumPlayStates

A enumeração `enumPlayStates` é usada para identificar os estados de reprodução. Os valores possíveis são:

- `Paused`: Estado de pausa.
- `Stopped`: Estado de parada.
- `Playing`: Estado de reprodução.
- `MediaEnded`: Estado de final de mídia.

### enumPlayMode

A enumeração `enumPlayMode` é usada para identificar os modos de reprodução. Os valores possíveis são:

- `PlaySingleTrack`: Modo de reproduzir uma única faixa.
- `AutoNextTrack`: Modo de reproduzir automaticamente a próxima faixa.
- `Shuffle`: Modo de reprodução aleatória.

### enumPlaylistMode

A enumeração `enumPlaylistMode` é usada para identificar os modos de uma playlist. Os valores possíveis são:

- `RepeatPlaylist`: Modo de repetir a playlist.
- `RepeatSingleTrack`: Modo de repetir uma única faixa.

### enumMediaMode

A enumeração `enumMediaMode` é usada para identificar os tipos de mídia suportados. Os valores possíveis são:

- `MidiMediaMode`: Modo de mídia Midi.
- `MP3MediaMode`: Modo de mídia MP3.
- `CDMediaMode`: Modo de mídia CD.
- `SidMediaMode`: Modo de mídia Sid.
- `MusMediaMode`: Modo de mídia Mus.
