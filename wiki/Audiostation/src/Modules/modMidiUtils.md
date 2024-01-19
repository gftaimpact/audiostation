# Documentação do código

```VBA
Attribute VB_Name = "ModMidiUtils"
Option Explicit
```

## Módulo: ModMidiUtils

Este módulo contém funções utilitárias para reprodução de MIDI (Musical Instrument Digital Interface).

Autor: Sibra-Soft - Alex van den Berg
Data de criação: 04-10-2021
Última modificação: 25-10-2021

### Variáveis Globais

- `gisEnd`: Variável booleana usada para sinalizar o fim de um processo.
- `gisCurrentDoEvents`: Variável booleana usada para rastrear o estado atual de 'DoEvents'.
- `gisCurrentQueue`: Variável booleana usada para rastrear o estado atual da fila.
- `gisCurrentFF`: Variável booleana usada para rastrear o estado atual de FF (Fast Forward).
- `gmThreadPriorityApp`: Variável inteira para o controle de prioridade de thread.

### Tipos definidos pelo usuário

- `MidiFFTracking`: Tipo que contém um campo de número de mensagem detectada (`nDetectedMessageNumber`).

### Constantes

- `MB_INTEGERUBOUND`, `MB_LONGUBOUND`, `MB_LOWNIBBLE`, `MB_HIGHNIBBLE`, `MB_LOWBYTE`, `MB_HIGHBYTE`, `MB_DOEVENTSPOLLING`, `MB_DEVICEID`: Constantes usadas em várias partes do código.

### Funções declaradas

As funções são declaradas para interagir com as bibliotecas do kernel32 e user32 do Windows. Essas funções permitem manipular a prioridade do thread, fazer a thread dormir e bloquear a atualização da janela.

### Funções 

- `MidiNoteString2Display`: Esta função recebe um buffer de nota como uma string e o converte em uma string de exibição mnemônica.
- `RoundVB5`: Esta função emula a função Round do VB6 no VB5, porque o VB5 não tem uma função Round.
- `AmbientUserMode`: Esta função verifica se o aplicativo está em modo de usuário.
- `GetChecksum`: Esta função calcula o checksum de uma string de mensagem.

Lembre-se de que todas as funções têm uma checagem de estado `gisEnd` no início para garantir que não sejam executadas depois que o processo for sinalizado para terminar.