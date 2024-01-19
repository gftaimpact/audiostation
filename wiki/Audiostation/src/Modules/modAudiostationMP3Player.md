# Documentação do Código

## Módulo: AudiostationMP3Player
Este módulo adiciona funcionalidade de reprodução de MP3.

### Variáveis Públicas:

1. `MediaPlaylistMode`: Esta variável é uma enumeração `enumPlaylistMode`, que define o modo de reprodução da lista de músicas.
2. `MediaPlayMode`: Esta variável é uma enumeração `enumPlayMode`, que define o modo de reprodução do media player.
3. `MediaPlaystate`: Esta variável é uma enumeração `enumPlayStates`, que define o estado de reprodução do media player.
4. `MediaPlaylist`: Este objeto é uma instância de `LocalStorage` que representa a lista de músicas a serem reproduzidas.
5. `ShowElapsedTime`: Esta variável booleana determina se o tempo decorrido da música atual deve ser exibido ou não.
6. `CurrentMediaFilename`: Esta variável armazena o nome do arquivo de mídia atual.
7. `CurrentTrackNumber`: Esta variável armazena o número da faixa atual.

### Sub-Rotinas:

1. `Init()`: Esta sub-rotina inicializa o media player com os valores padrão.
2. `Rewind()`: Esta sub-rotina retrocede a música atual em 5 segundos.
3. `Forward()`: Esta sub-rotina avança a música atual em 5 segundos.
4. `Pause()`: Esta sub-rotina pausa a reprodução da música atual.
5. `StartPlay()`: Esta sub-rotina inicia a reprodução da música. Se a música estiver em pausa, ela continuará a reprodução, caso contrário, começará a reprodução da música atual na lista de reprodução.
6. `StopPlay()`: Esta sub-rotina para a reprodução da música atual.
7. `NextTrack(Optional TrackNumber As Integer, Optional Force = False)`: Esta sub-rotina avança para a próxima música na lista de reprodução. Se o número da faixa for fornecido, ele reproduzirá a faixa especificada. Se a opção Force for verdadeira, ele forçará a reprodução da próxima faixa.
8. `PreviousTrack()`: Esta sub-rotina retrocede para a música anterior na lista de reprodução.

**Nota**: O módulo usa a biblioteca BASS para lidar com a reprodução de música.