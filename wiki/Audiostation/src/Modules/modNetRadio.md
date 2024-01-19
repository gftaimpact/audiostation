# Documentação do Código

Este módulo é chamado de "ModBassNetRadio" e é responsável por gerenciar o fluxo de dados de uma estação de rádio via internet.

As principais variáveis públicas são:

- `Url`: Variável para guardar o URL da estação de rádio.
- `TmpNameHold` e `TmpNameHold2`: Variáveis temporárias para guardar o nome da música que está sendo reproduzida.
- `proxy(100)`: Array para armazenar os dados de um servidor proxy, se necessário.
- `WriteFile`: Objeto da classe FileIO, usado para escrever os dados do fluxo de rádio em um arquivo local.
- `FileIsOpen`, `GotHeader`, `DownloadStarted`, `DoDownload`, `DlOutput`, `SongNameUpdate`: Variáveis de controle usadas durante o download do fluxo de rádio.
- `cthread`: Variável para armazenar o identificador de um thread.

O módulo utiliza duas funções do Windows API para gerenciar threads e exibir mensagens para o usuário:

- `CreateThread`: Função para criar um novo thread.
- `CloseHandle`: Função para fechar um identificador de objeto.
- `MessageBox`: Função para exibir uma caixa de mensagem para o usuário.
- `Sleep`: Função para pausar a execução do thread por um período de tempo especificado.

O módulo possui quatro sub-rotinas principais:

- `DoMeta`: Esta sub-rotina é chamada para obter os metadados do fluxo de rádio, como o título da música que está sendo reproduzida.
- `MetaSync`: Sub-rotina chamada quando os metadados do fluxo são alterados.
- `EndSync`: Sub-rotina chamada quando o fluxo de rádio termina.
- `SUBDOWNLOADPROC`: Esta sub-rotina é chamada para gerenciar o download do fluxo de rádio.

Além disso, o módulo possui uma função `RemoveSpecialChar` que é usada para remover caracteres especiais do nome da música que está sendo reproduzida. Esta função é necessária porque os nomes de arquivo no Windows não podem conter caracteres especiais.