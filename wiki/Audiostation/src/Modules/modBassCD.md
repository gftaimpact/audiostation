# Documentação do Módulo ModBassCD

Esse módulo em Visual Basic é parte da biblioteca BASSCD 2.4, uma biblioteca de áudio proprietária. Ele foi desenvolvido pela Un4seen Developments Ltd. e permite a manipulação de CDs de áudio em seus projetos.

## Erros

O módulo define constantes globais que representam códigos de erro específicos retornados pela função `BASS_ErrorGetCode`. Estes incluem:

- `BASS_ERROR_NOCD`: Indica que não há CD na unidade.
- `BASS_ERROR_CDTRACK`: Indica que o número da faixa é inválido.
- `BASS_ERROR_NOTAUDIO`: Indica que a faixa não é de áudio.

## Configurações

O módulo também define constantes globais para opções de configuração adicionais para a função `BASS_SetConfig`. Estas incluem:

- `BASS_CONFIG_CD_FREEOLD`
- `BASS_CONFIG_CD_RETRY`
- `BASS_CONFIG_CD_AUTOSPEED`
- `BASS_CONFIG_CD_SKIPERROR`
- `BASS_CONFIG_CD_READ`
- `BASS_CONFIG_CD_TIMEOUT`

## Tipos de Dados

Um tipo de dados definido é `BASS_CD_INFO`, que contém informações sobre uma unidade de CD, como o fabricante, modelo, revisão, letra da unidade, capacidade de leitura/escrita, se a unidade suporta abrir/fechar o CD, se a unidade suporta bloquear/desbloquear o CD, velocidade máxima de leitura, tamanho do cache e se a unidade pode ler CD-TEXT.

## Funções

Existem várias funções declaradas neste módulo que permitem a manipulação de CDs de áudio. Alguns exemplos incluem:

- `BASS_CD_SetInterface`: Define a interface de CD.
- `BASS_CD_GetInfo`: Obtém informações sobre uma unidade de CD.
- `BASS_CD_Door`: Controla a abertura e fechamento da unidade de CD.
- `BASS_CD_DoorIsLocked`: Verifica se a unidade de CD está trancada.
- `BASS_CD_DoorIsOpen`: Verifica se a unidade de CD está aberta.
- `BASS_CD_IsReady`: Verifica se a unidade de CD está pronta.
- `BASS_CD_GetTracks`: Obtém o número de faixas no CD.
- `BASS_CD_GetTrackLength`: Obtém o comprimento de uma faixa específica no CD.

## Funções de Callback

O módulo também define uma função de retorno de chamada, `CDDATAPROC`, que é chamada durante a leitura do sub-canal/C2. Ela recebe vários parâmetros, incluindo o identificador do fluxo de CD, a posição dos dados, o tipo de dados, um buffer contendo os dados, o número de bytes no buffer e um valor de parâmetro do usuário.
