# Documentação do Código

## Módulo: ModConvert

Esse módulo é responsável pela conversão de formatos de arquivos de áudio.

### Enums: 

#### ConvertFrom
Enumeração dos formatos de áudio que podem ser convertidos. Inclui:

- Real Media
- Real Audio
- Voice File Format
- Apple Core Format
- Sony Wave64
- OGG
- Westwood Studios Audio
- Sony OpenMG Audio
- Raw Flac
- Creative Voice
- Windows Media
- Media4A

#### convertto
Enumeração dos formatos de áudio para os quais a conversão é possível. Inclui:

- MP3
- WAV

### Função: Convert

Parâmetros:
- `ConvFilename` (String): Caminho do arquivo a ser convertido.
- `ConvFrom` (ConvertFrom): Formato original do arquivo.
- `convTo` (convertto): Formato para o qual o arquivo será convertido.

Essa função realiza a conversão de um arquivo de áudio de um formato para outro. A função utiliza o software externo 'ffmpeg.exe' para realizar a conversão.

Primeiramente, o nome do arquivo é extraído do caminho fornecido sem a extensão. Em seguida, a função chama o 'ffmpeg.exe' para converter o arquivo para o formato desejado. O arquivo convertido é então armazenado em um diretório temporário.

Finalmente, a função grava o caminho do arquivo convertido em um arquivo de configurações, sob a seção 'Audiostation' com a chave 'CheckFile'.