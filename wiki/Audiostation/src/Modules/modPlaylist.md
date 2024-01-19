# Documentação do código

## Módulo ModPlaylist

O módulo `ModPlaylist` contém várias funções que tratam da manipulação de diferentes tipos de playlists.

### Função: OpenAplPlaylist(strPlaylistFile As String)

Esta função é usada para abrir uma playlist do tipo APL.

**Argumentos**

- strPlaylistFile: O caminho do arquivo de playlist APL a ser aberto.

**Comportamento**

A função lê o conteúdo do arquivo da playlist usando a função `FileGetContents` do módulo `Extensions`. Então, ela adiciona as músicas da playlist ao `Form_Playlist` usando a função `AddToPlaylist`.

### Função: OpenWplPlaylist(FileName As String)

Esta função é usada para abrir uma playlist do tipo WPL.

**Argumentos**

- FileName: O caminho do arquivo de playlist WPL a ser aberto.

**Comportamento**

A função lê o conteúdo do arquivo da playlist, divide o conteúdo em linhas e processa cada linha. Se a linha contém a tag `<media`, ela extrai o conteúdo da tag, faz algumas substituições de caracteres e acrescenta o resultado a uma string de arquivos. Finalmente, adiciona todas as músicas extraídas ao `Form_Playlist`.

### Função: OpenM3uPlaylist(strPlaylistFile As String, Optional TargetListbox As ListBox)

Esta função é usada para abrir uma playlist do tipo M3U.

**Argumentos**

- strPlaylistFile: O caminho do arquivo de playlist M3U a ser aberto.
- TargetListbox (opcional): O ListBox alvo onde a playlist será exibida.

**Comportamento**

A função lê o arquivo da playlist linha por linha. Ela ignora as linhas que começam com `#EXTM3U` ou `#EXTINF:` e adiciona todas as outras linhas ao `Form_Playlist`.

### Função: OpenPlsPlaylist(strPlaylistFile As String, Optional TargetListbox As ListBox)

Esta função é usada para abrir uma playlist do tipo PLS.

**Argumentos**

- strPlaylistFile: O caminho do arquivo de playlist PLS a ser aberto.
- TargetListbox (opcional): O ListBox alvo onde a playlist será exibida.

**Comportamento**

A função lê o número de entradas na playlist usando a função `INIRead` do módulo `Extensions`. Então, ela lê cada entrada da playlist e a adiciona ao `Form_Playlist`.