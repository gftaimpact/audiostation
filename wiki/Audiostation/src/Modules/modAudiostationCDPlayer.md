# AudiostationCDPlayer

O módulo `AudiostationCDPlayer` adiciona funcionalidades de CD player ao programa Audiostation.

## Variáveis Públicas

- `CDPlaystate`: armazena o estado atual de reprodução do CD.
- `mode`: armazena o modo de reprodução do CD.
- `CurrentTrackCount`: armazena a contagem de faixas do CD atual.
- `CurrentTrackNr`: armazena o número da faixa que está sendo reproduzida no momento.

## Métodos Privados

### EndSync
O método `EndSync` é chamado ao final da sincronização. Ele verifica se existem mais faixas para serem reproduzidas no CD. Se existirem, ele chama o método `PlayTrackFromCD` para reproduzir a próxima faixa.

### PlayTrackFromCD
O método `PlayTrackFromCD` é responsável por reproduzir uma faixa específica do CD. Ele verifica se já existe um stream para a faixa. Se existir, ele apenas define a faixa para o stream. Se não existir, ele cria um novo stream para a faixa e define a sincronização de final para a faixa.

## Métodos Públicos

### StopPlay
O método `StopPlay` é usado para parar a reprodução do CD.

### CheckIfCDRomDriveExists
O método `CheckIfCDRomDriveExists` verifica se existe uma unidade de CD-ROM. Retorna verdadeiro se existir, caso contrário, retorna falso.

### Play
O método `Play` é responsável por iniciar a reprodução do CD.

### Pause
O método `Pause` é usado para pausar a reprodução do CD.

### Forward
O método `Forward` é usado para avançar a reprodução do CD em 5 segundos.

### Rewind
O método `Rewind` é usado para retroceder a reprodução do CD em 5 segundos.

### OpenOrCloseDriveDoor
O método `OpenOrCloseDriveDoor` é usado para abrir ou fechar a porta da unidade de CD-ROM.

### NextTrack
O método `NextTrack` é usado para pular para a próxima faixa do CD.

### PreviousTrack
O método `PreviousTrack` é usado para voltar para a faixa anterior do CD.