# Documentação do código

Este é um módulo Visual Basic chamado "modBassMix". Ele faz parte da biblioteca BASSmix 2.4, que é uma extensão para a biblioteca de áudio BASS. Esta extensão permite a mixagem de canais de áudio e a divisão de fluxos de áudio.

### Constantes Globais

As constantes globais definidas neste módulo são usadas para configurar as opções BASS, especificar os atributos do mixer, definir os tipos de envelope, especificar os tipos de sincronização, definir os valores de retorno para BASS_Mixer_ChannelIsActive, entre outros.

### Funções

As funções definidas neste módulo são principalmente para criar, adicionar, remover e gerenciar canais em um fluxo de mixagem, criar e gerenciar divisores de fluxo, e definir e obter a posição e o nível de um canal.

### Estruturas

Uma estrutura chamada BASS_MIXER_NODE é definida neste módulo. Ela é usada para definir um nó de envelope, que é um ponto em um envelope (uma curva que representa uma mudança de valor ao longo do tempo).

### Wrappers de função

Existem quatro wrappers de função no final do módulo. Eles são usados para chamar funções de 64 bits da biblioteca BASS com argumentos de 32 bits.