# Documentação de Código: AudiostationStreamer

## Versão: 1.0

### Descrição Geral:

A classe AudiostationStreamer adiciona funcionalidade de streaming ao programa Audiostation.

- Autor: Sibra-Soft - Alex van den Berg
- Data de Criação: 04-10-2021
- Última alteração: 05-10-2021

Esta classe possui cinco variáveis públicas e uma função pública. 

## Variáveis:

- `MetaTitle` (String): Título meta da stream.
- `Status` (String): Status da stream.
- `Url` (String): Url da stream.
- `Name` (String): Nome da stream.
- `Error` (Boolean): Indica se ocorreu um erro.

## Função: OpenStream

```vba
Public Function OpenStream(Url As String, Optional Name As String = vbNullString) As Boolean
```

Esta função tenta abrir uma stream a partir de uma URL fornecida. Se um nome for fornecido, ele será armazenado na variável de instância `Name`.

### Parâmetros:

- `Url` (String): A URL da stream a ser aberta.
- `Name` (String, opcional): O nome da stream.

### Retorno:

- `Boolean`: Retorna `True` se a stream for aberta com sucesso. Se não for possível abrir a stream, retorna `False`.

### Comportamento:

1. Configura o proxy da rede.
2. Libera qualquer stream ou canal que já esteja em uso.
3. Tenta criar uma nova stream a partir da URL fornecida.
4. Se a stream não puder ser criada, exibe uma mensagem de erro e retorna `False`.
5. Se a stream for criada com sucesso, armazena a URL e o nome (se fornecido), e retorna `True`.