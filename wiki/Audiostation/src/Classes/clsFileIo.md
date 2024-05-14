# Documentação do arquivo FileIO

## Introdução

Este arquivo, chamado FileIO, é uma classe responsável por ler e escrever arquivos no disco.

## Dependências

O código não possui dependências explícitas.

## Estrutura

A estrutura do código é composta por uma classe principal chamada FileIO, que contém constantes, funções e métodos privados.

## Imports

O código importa várias funções da biblioteca do kernel32.dll e user32.dll do Windows.

## Variáveis

As variáveis privadas neste arquivo são: `fHandle`, `fSuccess`, `lFilePos` e `File_Name`. 

## Dependências

Este arquivo não tem dependências externas.

## Métodos

Os métodos públicos disponíveis nesta classe são `OpenFile`, `CloseFile` e `WriteBytes`. `OpenFile` é usado para abrir um arquivo, `CloseFile` é usado para fechar um arquivo e `WriteBytes` é usado para escrever bytes em um arquivo.

## Exemplo

Para usar essa classe, você criaria uma instância da classe `FileIO`, abriria um arquivo com `OpenFile`, escreveria no arquivo com `WriteBytes` e, finalmente, fecharia o arquivo com `CloseFile`.

## Diagrama de dependências

```
graph TD
A[FileIO] --> B[OpenFile]
A[FileIO] --> C[CloseFile]
A[FileIO] --> D[WriteBytes]
```

## Notas

O código foi criado por Peter Hebels em 04-10-2021 e modificado pela última vez em 05-10-2021.

## Vulnerabilidades

Nenhuma vulnerabilidade conhecida é associada a este arquivo.