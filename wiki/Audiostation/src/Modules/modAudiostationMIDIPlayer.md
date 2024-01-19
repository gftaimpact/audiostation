# Documentação do Código - AudiostationMIDIPlayer

## Descrição

Este é um módulo de software que adiciona funcionalidade de player MIDI. Foi criado por Sibra-Soft - Alex van den Berg e a última atualização foi em 25/10/2021.

## Variáveis Globais

- `MidiFilename`: Armazena o nome do arquivo MIDI sendo reproduzido.
- `MidiTrackNr`: Armazena o número da faixa MIDI atualmente selecionada.
- `MidiPlaystate`: Armazena o estado atual de reprodução (Playing, Paused, Stopped).
- `MidiPlaylist`: Armazena a lista de reprodução MIDI atual.
- `ConsoleWindow`: Armazena a janela de console atual.

## Funções

- `StartMidiPlayback()`: Inicia a reprodução MIDI. Se a faixa estiver pausada, retoma a reprodução. Caso contrário, seleciona a faixa correta com base no número da faixa, determina o tipo de arquivo e inicia a reprodução apropriada.

- `StopMidiPlayback()`: Interrompe a reprodução MIDI. Se estiver no modo SidMedia, fecha a janela do console. Caso contrário, interrompe a reprodução e muda o estado de reprodução para 'Stopped'.

- `PauseMidiPlayback()`: Pausa a reprodução MIDI e muda o estado de reprodução para 'Paused'.

- `NextMidiTrack()`: Avança para a próxima faixa na lista de reprodução MIDI, se houver, e inicia a reprodução.

- `PreviousMidiTrack()`: Retrocede para a faixa anterior na lista de reprodução MIDI, se houver, e inicia a reprodução.

- `ForwardMidi10Seconds()`: Avança a reprodução MIDI em 10 segundos, se possível.

- `RewindMidi10Seconds()`: Retrocede a reprodução MIDI em 10 segundos, se possível.

## Uso

Este módulo é usado para controlar a reprodução de arquivos MIDI. Ele fornece uma interface para iniciar, parar, pausar a reprodução, bem como avançar e retroceder a reprodução. Ele também suporta a seleção de faixas em uma lista de reprodução.