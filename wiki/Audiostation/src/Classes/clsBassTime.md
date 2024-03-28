# Documentação do arquivo BaseTime

## Introdução

Este arquivo contém uma classe chamada BaseTime que fornece várias funções para manipular e obter informações sobre arquivos de áudio.

## Dependências

Este arquivo depende da biblioteca BASS, que é usada para manipular arquivos de áudio.

## Estrutura

Este arquivo contém uma única classe chamada BaseTime que fornece várias funções que podem ser usadas para obter informações sobre um arquivo de áudio.

## Imports

Este arquivo não importa nenhum outro arquivo ou módulo.

## Variáveis

Este arquivo contém uma variável chamada `info` do tipo BASS_CHANNELINFO que é usada para armazenar informações sobre um canal de áudio.

## Métodos

Este arquivo contém os seguintes métodos:

- `GetTime(seconds: Long) -> String`: Retorna a duração total de segundos como formato de tempo: HH:MM:SS
- `GetPlayingPos(handle: Long) -> Single`: Retorna a posição de reprodução em segundos
- `GetDuration(handle: Long) -> Single`: Retorna a duração total em segundos
- `GetBytesPerSecond(handle: Long) -> Long`: Retorna Bytes Por Segundo
- `GetBitsPerSecond(handle: Long, FileLength: Long) -> Long`: Retorna Kilo Bits Por Segundo
- `GetMode(handle: Long) -> String`: Retorna 'Stereo'/'Mono' ou 'MultiChannel'
- `GetBits(handle: Long) -> Byte`: Retorna 8/16/32-float bits
- `GetFrequency(handle: Long) -> Long`: Retorna a Taxa de Amostra [Frequência]
- `GetDXver() -> Byte`: Retorna a versão do DirectX

## Exemplo

Para usar esta classe, você criaria um objeto da classe BaseTime e então chamaria os métodos apropriados. Aqui está um exemplo de como você poderia obter a duração de um arquivo de áudio:

```vba
Dim bt As New BaseTime
Dim duration As Single
duration = bt.GetDuration(handle)
```

## Diagrama de dependências

```
graph LR
BaseTime --> BASS_CHANNELINFO
BaseTime --> BASS_ChannelBytes2Seconds
BaseTime --> BASS_ChannelGetPosition
BaseTime --> BASS_ChannelGetLength
BaseTime --> BASS_ChannelGetInfo
BaseTime --> BASS_SAMPLE_8BITS
BaseTime --> BASS_SAMPLE_FLOAT
BaseTime --> BASS_ChannelGetAttribute
BaseTime --> BASS_ATTRIB_FREQ
BaseTime --> BASS_GetInfo
```

## Notas

Este arquivo é compatível com a versão 1.0.

## Vulnerabilidades

Não foram identificadas vulnerabilidades neste arquivo.