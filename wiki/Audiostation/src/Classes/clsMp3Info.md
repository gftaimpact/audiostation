# Documentação do arquivo Mp3Info

## Introdução

Esta classe representa um arquivo MP3 e fornece funcionalidades para ler e manipular informações sobre o arquivo, como bitrate, frequência, tempo de música, número de quadros e outros detalhes do cabeçalho MP3.

## Dependências

Esta classe não tem dependências externas.

## Estrutura

A classe possui vários métodos e variáveis privadas para armazenar e manipular informações sobre o arquivo MP3.

## Imports

Esta classe não importa nenhum módulo ou biblioteca externa.

## Variáveis

A classe tem várias variáveis privadas que armazenam informações sobre o arquivo MP3, como bitrate, frequência, tempo de música, número de quadros, etc.

## Métodos

A classe possui vários métodos privados para ler e manipular informações do arquivo MP3. Além disso, possui um método público `ReadMp3Binary` que inicia a leitura do arquivo MP3.

## Exemplo

```vba
Dim mp3Info As New Mp3Info
mp3Info.Filename = "path_to_your_mp3_file"
mp3Info.ReadMp3Binary
```

## Diagrama de dependências

```mermaid
classDiagram
    Mp3Info --|> Mp3Info: Inherits
    class Mp3Info{
        -m_MPEGVer As Single
        -m_VerStr As String
        -m_Layers As Long
        -m_Protected As Boolean
        -m_BitRate As Long
        -m_Frequency As Long
        -m_ChannelMode As String
        -m_CopyRighted As Boolean
        -m_Original As Boolean
        -m_Emphasis As String
        -m_Padding As Byte
        -m_ValidMP3 As Boolean
        -m_FileName As String
        -m_FileSize As Long
        -m_SongLength As Long
        -m_NumFrames As Long
        -m_FrameLength As Long
        -m_VBR As Boolean
        -m_HeaderOffset As Long
        -m_ActSize As Long
        +ReadMp3Binary()
        -ReadFileBinary(sFilePath As String) As Byte()
        -StringToSizeBin(Arr() As Byte, IsHeaderSize As Boolean) As Double
        -GetReadPos(RP As Long)
        -IsHeader(inArr() As Byte) As Boolean
        -ValidHeader(inArr() As Byte, ReadPos As Long) As Boolean
        -ClearInfo()
        -GetID3v1Tags()
        -GetID3v2Tags(Tag2 As String) As Boolean
    }
```

## Notas

A classe foi escrita em VBA e pode não ser compatível com todas as versões do Microsoft Office.

## Vulnerabilidades

A classe não valida o caminho do arquivo passado para o método `ReadMp3Binary`, portanto, deve-se ter cuidado ao passar argumentos para esse método. Além disso, a classe não lida com exceções que podem ocorrer durante a leitura do arquivo.