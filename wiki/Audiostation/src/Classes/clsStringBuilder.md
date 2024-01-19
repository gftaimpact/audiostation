# Documentação da Classe StringBuilder

## Descrição
A classe StringBuilder é uma implementação do padrão StringBuilder encontrado no .NetFramework. Foi criada por Alex van den Berg da Sibra-Soft em 22 de Setembro de 2021, com a última atualização em 05 de Outubro de 2021.

## Variáveis Privadas

- `m_sString`: Armazena a string atual.
- `m_iChunkSize`: Define o tamanho do bloco de caracteres.
- `m_iPos`: Posição atual na string.
- `m_iLen`: Comprimento atual da string.

## Propriedades

- `length()`: Retorna o comprimento atual da string.
- `Capacity()`: Retorna a capacidade atual da string.
- `ChunkSize()`: Retorna o tamanho do bloco de caracteres.
- `toString()`: Retorna a string atual.
- `TheString()`: Define a string atual.

## Métodos

- `Clear()`: Limpa a string atual.
- `AppendNL()`: Anexa uma nova linha à string atual.
- `Append()`: Anexa uma string à string atual.
- `AppendByVal()`: Anexa uma string passada por valor à string atual.
- `Insert()`: Insere uma string em um índice especificado na string atual.
- `InsertByVal()`: Insere uma string passada por valor em um índice especificado na string atual.
- `Remove()`: Remove uma parte da string a partir de um índice especificado e um comprimento determinado.
- `Find()`: Encontra uma string específica na string atual, com opções para definir um índice de início e um método de comparação.
- `HeapMinimize()`: Reduz o tamanho da string para que apenas os blocos mínimos sejam alocados.
- `UnsignedAdd()`: Função útil para aritmética de ponteiros, só funciona para valores positivos de incremento.
- `Class_Initialize()`: Inicializa a classe com um tamanho de bloco de caracteres padrão de 8192 caracteres.

## Uso
Essa classe é útil para manipulação eficiente de strings em aplicativos que realizam muitas operações de concatenação ou modificação de strings. A interface fornece métodos para anexar, inserir, remover e buscar strings, além de ajustar a capacidade da string subjacente.