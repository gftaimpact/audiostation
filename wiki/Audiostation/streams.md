# Documentação do arquivo de links de rádio

## Introdução

Este arquivo contém uma lista de links para diferentes estações de rádio. Cada linha contém o nome da estação de rádio e o URL correspondente. Os URLs apontam para os fluxos ao vivo das estações de rádio.

## Estrutura

O arquivo é estruturado como uma lista de pares nome-URL, separados por um ponto e vírgula. Cada par é representado em uma linha separada.

## Exemplo

Um exemplo de uma linha no arquivo é:

```
NPO Radio 1 ; https://icecast.omroep.nl/radio1-bb-mp3
```

Neste exemplo, "NPO Radio 1" é o nome da estação de rádio e "https://icecast.omroep.nl/radio1-bb-mp3" é o URL do fluxo ao vivo da estação.

## Uso

Para ouvir uma estação de rádio, você pode abrir o URL correspondente em um player de mídia que suporta streaming de áudio. 

## Notas

Os URLs apontam diretamente para os fluxos de áudio das estações de rádio, portanto, eles podem não abrir corretamente em um navegador da web. Em vez disso, eles devem ser abertos em um player de mídia que suporta streaming de áudio.

## Diagrama de dependências

```
+----------------+        +-----------------+
| Nome da estação|  ----> | URL da estação  |
+----------------+        +-----------------+
```

Neste diagrama, o nome da estação de rádio aponta para o URL correspondente. Não há dependências adicionais.