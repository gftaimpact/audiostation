# Documentação do arquivo LocalStorage

## Introdução

Este arquivo é uma implementação de uma classe chamada "LocalStorage". Ele é usado para armazenar coleções de dados, como listas de reprodução, entre outros. Foi criado pela Sibra-Soft, por Alex van den Berg.

## Dependências

Este arquivo depende da classe "Nest".

## Estrutura

A estrutura deste arquivo é de uma classe com vários métodos públicos e privados, além de algumas variáveis públicas.

## Imports

Nenhum import é necessário para este arquivo.

## Variáveis

Este arquivo contém as seguintes variáveis:

- IsFilterd (Pública, Boolean): Indica se a coleção atual está filtrada.
- StorageContainer (Pública, Nest): Armazena a coleção de dados.
- StorageContainerTemp (Privada, Nest): Armazena uma cópia temporária da coleção para operações de filtro.

## Métodos

Este arquivo contém os seguintes métodos:

- ClearFilter(): Limpa qualquer filtro aplicado à coleção.
- Filter(FilterString As String): Filtra a coleção com base na string de filtro fornecida.
- IsExistingItem(KeyToFind As String) As Integer: Verifica se um item existe na coleção, com base em sua chave.
- ListviewToStorage(TargetListview As ListView, KeyColumn As Integer): Converte uma lista de exibição em uma coleção armazenada.
- ClearStorage(): Limpa a coleção.
- AddToStorage(key As String, value As String): Adiciona um item à coleção.
- GetItemByKey(key As String, Column As Integer) As String: Obtém um item da coleção com base em sua chave.
- GetItemByIndex(index As Integer, Column As Integer) As String: Obtém um item da coleção com base em seu índice.

## Exemplo

Para usar esta classe, crie uma instância e utilize seus métodos para manipular a coleção. Por exemplo:

```vbscript
Dim storage As New LocalStorage
storage.AddToStorage "key1", "value1"
Dim value As String
value = storage.GetItemByKey("key1", 0)
```

## Diagrama de dependências

```
graph TD;
    LocalStorage --> Nest
```

## Notas

Este arquivo foi criado em 23-12-2018 e a última alteração foi feita em 05-10-2021.

## Vulnerabilidades

Não foram identificadas vulnerabilidades neste arquivo.
