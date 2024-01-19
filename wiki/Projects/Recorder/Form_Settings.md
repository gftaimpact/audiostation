# Documentação do Código

Este script é usado para criar e gerenciar as configurações de um gravador de áudio.

## Estrutura da Interface do Usuário

A interface do usuário consiste em um formulário chamado `Form_Settings` que inclui os seguintes componentes:

- Um botão chamado `Button_Save` que, quando clicado, salva as configurações atuais.
- Um botão chamado `Button_Cancel` que, quando clicado, descarta qualquer alteração feita e fecha o formulário.
- Um quadro `Frame1` que inclui:
    - Duas opções de botão `Option_Mp3File` e `Option_WaveFile` para selecionar o formato de saída do arquivo de áudio.
    - Duas caixas de combinação `Combox_Rate` e `Combox_InputDevice` para selecionar a taxa de gravação e o dispositivo de entrada, respectivamente.
    - Três rótulos `Label1`, `Label2` e `Label3` para indicar a seleção do dispositivo de entrada, a taxa de gravação e o formato de saída, respectivamente.

## Funcionalidades

Quando o formulário é carregado (`Form_Load`), uma lista de taxas de gravação é adicionada à `Combox_Rate` e a taxa de gravação salva é selecionada por padrão. Além disso, uma lista de dispositivos de entrada disponíveis é adicionada à `Combox_InputDevice` e o dispositivo de entrada padrão ou salvo é selecionado.

Quando o botão `Button_Save` é clicado, o índice do dispositivo de entrada selecionado e o identificador do dispositivo de entrada são salvos. Além disso, a taxa de gravação selecionada também é salva.

Quando o botão `Button_Cancel` é clicado, o formulário é descarregado sem salvar nenhuma alteração.

## Observações

Este código usa a API BASS para obter informações sobre os dispositivos de entrada disponíveis. Além disso, as configurações são salvas usando a função `WriteSetting` da classe `Settings`. As configurações são lidas usando a função `ReadSetting` da mesma classe.