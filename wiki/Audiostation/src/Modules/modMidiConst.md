# Documentação do Módulo ModConstMidi

Este módulo define uma série de constantes públicas usadas para representar o estado e as ações possíveis para dispositivos MIDI, mensagens MIDI e propriedades de filtros MIDI.

## Constantes de Estado

- `MIDISTATE_CLOSED`: Estado do dispositivo quando está fechado.
- `MIDISTATE_OPENED`: Estado do dispositivo quando está aberto.
- `MIDISTATE_STARTED`: Estado do dispositivo quando está iniciado.
- `MIDISTATE_STOPPED`: Estado do dispositivo quando está parado.
- `MIDISTATE_PAUSED`: Estado do dispositivo quando está pausado.

## Ações MidiIn

- `MIDIIN_NONE`: Nenhuma ação MidiIn.
- `MIDIIN_OPEN`: Abertura do dispositivo MidiIn.
- `MIDIIN_CLOSE`: Fechamento do dispositivo MidiIn.
- `MIDIIN_RESET`: Reset do dispositivo MidiIn.
- `MIDIIN_START`: Iniciar o dispositivo MidiIn.
- `MIDIIN_STOP`: Parar o dispositivo MidiIn.
- `MIDIIN_REMOVE`: Remover o dispositivo MidiIn.
- `MIDIIN_QUEUE`: Enfileirar ação no dispositivo MidiIn.
- `MIDIIN_SORT`: Classificar ações no dispositivo MidiIn.

## Ações MidiOut

- `MIDIOUT_NONE`: Nenhuma ação MidiOut.
- `MIDIOUT_OPEN`: Abertura do dispositivo MidiOut.
- `MIDIOUT_CLOSE`: Fechamento do dispositivo MidiOut.
- `MIDIOUT_RESET`: Reset do dispositivo MidiOut.
- `MIDIOUT_START`: Iniciar o dispositivo MidiOut.
- `MIDIOUT_STOP`: Parar o dispositivo MidiOut.
- `MIDIOUT_QUEUE`: Enfileirar ação no dispositivo MidiOut.
- `MIDIOUT_SEND`: Enviar ação ao dispositivo MidiOut.
- `MIDIOUT_TIMER`: Ação de temporizador do dispositivo MidiOut.
- `MIDIOUT_PAUSE`: Pausar o dispositivo MidiOut.
- `MIDIOUT_REMOVE`: Remover o dispositivo MidiOut.
- `MIDIOUT_READ`: Ler o dispositivo MidiOut.

## Constantes de Mensagem MIDI

- `MIDIMESSAGESTATE_NONE`: Mensagem MIDI permanentemente desabilitada.
- `MIDIMESSAGESTATE_ENABLED`: Mensagem MIDI habilitada.
- `MIDIMESSAGESTATE_DISABLED`: Mensagem MIDI temporariamente desabilitada pelo usuário.
- `MIDIMESSAGESTATE_DISABLED2`: Reservado.
- `MIDIMESSAGESTATE_DISABLED3`: Reservado.

## Ponteiro da Mensagem MIDI

- `MIDIMP_MESSAGE`: Entrada/saída da mensagem.
- `MIDIMP_DATA1`: Primeiro dado de entrada/saída.
- `MIDIMP_DATA2`: Segundo dado de entrada/saída.
- `MIDIMP_TIME`: Tempo de entrada/saída.
- `MIDIMP_MESSAGETAG`: Tag de saída da mensagem.
- `MIDIMP_MESSAGESTATE`: Estado de saída da mensagem.
- `MIDIMP_TIMEOPEN`: Tempo de abertura de entrada/saída (somente leitura).
- `MIDIMP_DAYOPEN`: Dia de abertura de entrada/saída (somente leitura).
- `MIDIMP_TIMETEMPO`: Tempo de saída (somente leitura).
- `MIDIMP_TIMESTARTOPEN`: Tempo de início de abertura (somente leitura).
- `MIDIMP_TIMECURRENTOPEN`: Tempo atual de abertura (somente leitura).
- `MIDIMP_TIMEACTUALOPEN`: Tempo real de abertura (somente leitura).
- `MIDIMP_TIMERELTO2`: Tempo relativo 2 de entrada (somente leitura).
- `MIDIMP_TIMERELTO3`: Tempo relativo 3 de entrada (somente leitura).
- `MIDIMP_TIMERELTO4`: Tempo relativo 4 de entrada (somente leitura).
- `MIDIMP_ERROR`: Erro de entrada (somente leitura).
- `MIDIMP_ERRORLATE`: Erro de atraso de entrada (somente leitura).
- `MIDIMP_ERRORLONG`: Erro de longo prazo de entrada (somente leitura).
- `MIDIMP_ERRORCOUNT`: Contagem de erro de entrada (somente leitura).
- `MIDIMP_UBOUND`: Pode aumentar em versões futuras.

E muitas outras constantes...

Cada constante é usada em diferentes contextos dentro do projeto, permitindo um controle mais preciso sobre as operações MIDI.