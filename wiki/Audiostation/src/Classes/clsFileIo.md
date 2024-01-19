# Documentação de Código

## Versão: 1.0

### Classe: FileIO

Esta classe é responsável por ler e escrever arquivos no disco.

#### Detalhes

- Autor: Peter Hebels
- Data de Criação: 04-10-2021
- Data de Alteração: 05-10-2021

#### Constantes

- `GENERIC_WRITE`: Permissão para escrita.
- `FILE_ATTRIBUTE_NORMAL`: Atributo de arquivo normal.
- `CREATE_ALWAYS`: Cria um novo arquivo sempre.
- `OPEN_ALWAYS`: Abre um arquivo existente ou cria um novo.
- `INVALID_HANDLE_VALUE`: Valor de identificador inválido.

#### Funções

- `OpenFile(FileN As String) As Boolean`: Esta função tenta criar um novo arquivo com o nome fornecido. Retorna `True` se o arquivo for criado com sucesso, `False` caso contrário.
- `CloseFile() As Boolean`: Esta função tenta fechar o arquivo aberto. Retorna `True` se o arquivo for fechado com sucesso, `False` caso contrário.
- `WriteBytes(Pointer As Long, Size As Long) As Boolean`: Esta função escreve bytes em um arquivo aberto. Retorna `True` se a operação for bem-sucedida, `False` caso contrário.

#### Declarações Privadas

- `Private Declare Function`: Estas declarações importam funções de bibliotecas do sistema operacional para leitura, escrita e manipulação de arquivos.
- `Private fHandle As Long`: Este é o identificador do arquivo aberto.
- `Private fSuccess As Long`: Este é o status da última operação realizada.
- `Private lFilePos As Long`: Esta é a posição atual do ponteiro do arquivo.
- `Private File_Name As String`: Este é o nome do arquivo aberto.