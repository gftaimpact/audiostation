# Documentação de código

## Classe: BaseTime

Esta classe é usada para manipular e obter informações sobre arquivos de áudio.

### Propriedades:
- **info**: Uma instância da estrutura BASS_CHANNELINFO usada para obter informações do canal.

### Métodos:
- **GetTime(seconds As Long) As String**:

  Retorna a duração total a partir de segundos no formato de tempo: HH:MM:SS.

- **GetPlayingPos(handle As Long) As Single**:

  Retorna a posição de reprodução atual em segundos.

- **GetDuration(handle As Long) As Single**:

  Retorna a duração total em segundos.

- **GetBytesPerSecond(handle As Long) As Long**:

  Retorna a quantidade de bytes por segundo. Utiliza a estrutura BASS_CHANNELINFO para obter informações sobre o canal.

- **GetBitsPerSecond(handle As Long, FileLength As Long) As Long**:

  Retorna a quantidade de kilobits por segundo.

- **GetMode(handle As Long) As String**:

  Retorna o modo de reprodução do canal: 'Mono', 'Estéreo' ou 'Multicanal'.

- **GetBits(handle As Long) As Byte**:

  Retorna a profundidade de bits da amostra: 8, 16 ou 32 bits (float).

- **GetFrequency(handle As Long) As Long**:

  Retorna a taxa de amostragem (frequência) do canal.

- **GetDXver() As Byte**:

  Retorna a versão do DirectX utilizada.

## Observações:

Este código usa a biblioteca BASS, uma biblioteca de áudio para uso em software no Windows e OS X.

As funções BASS_ChannelGetInfo, BASS_ChannelBytes2Seconds, BASS_ChannelGetPosition, BASS_ChannelGetLength, BASS_ChannelGetAttribute e BASS_GetInfo são todas funções fornecidas pela biblioteca BASS e são usadas para obter diversas informações sobre o arquivo de áudio e o sistema.