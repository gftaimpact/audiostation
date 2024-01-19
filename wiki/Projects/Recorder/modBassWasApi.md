# Documentação do Módulo modBassWasApi

Esse módulo é uma parte do BASSWASAPI 2.4, um módulo Visual Basic desenvolvido por Un4seen Developments Ltd. Fornece uma interface para o WASAPI (Windows Audio Session API), permitindo a reprodução e gravação de áudio sem a necessidade de um mixer de som.

## Constantes Globais

O módulo define várias constantes para representar diferentes tipos de dispositivos, erros, formatos de áudio, entre outros. Por exemplo, `BASS_ERROR_WASAPI = 5000` é usado para indicar que o WASAPI não está disponível, enquanto `BASS_WASAPI_TYPE_SPEAKERS = 1` representa um dispositivo do tipo alto-falantes.

## Estruturas de Dados

O módulo usa duas estruturas de dados principais, `BASS_WASAPI_DEVICEINFO` e `BASS_WASAPI_INFO`, para armazenar informações sobre dispositivos WASAPI e sessões WASAPI, respectivamente.

## Funções Globais

O módulo fornece várias funções para interagir com a API WASAPI, incluindo `BASS_WASAPI_GetVersion`, que retorna a versão da API WASAPI, e `BASS_WASAPI_SetNotify`, que define uma função de retorno de chamada para receber notificações de dispositivos WASAPI.

## Funções de Retorno de Chamada (Callback)

O módulo inclui duas funções de retorno de chamada, `WASAPIPROC` e `WASAPINOTIFYPROC`. `WASAPIPROC` é chamada pelo WASAPI para preencher um buffer com dados de áudio ou para processar dados de áudio de um buffer. `WASAPINOTIFYPROC` é chamada quando um evento do dispositivo WASAPI ocorre, como um dispositivo sendo habilitado ou desabilitado.