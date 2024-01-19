# Documentação do Código

Este código é escrito em Visual Basic e define o comportamento de uma interface de usuário para abrir uma transmissão de áudio.

## Componentes da Interface

A interface do usuário é uma janela de diálogo fixa chamada "Open Stream". Ela contém um controle de guias com uma guia chamada "Existing". Dentro dessa guia, há uma lista de fluxos de áudio existentes e dois botões: "Open" e "Cancel".

### Botões

Os botões "Open" e "Cancel" estão definidos com a classe `Audiostation.ButtonBig`. Quando o botão "Cancel" é clicado, a janela de diálogo é fechada. Quando o botão "Open" é clicado, o fluxo de áudio selecionado na lista é aberto.

### Lista de Transmissões

A lista de transmissões é um controle `MSComctlLib.ListView`. Cada item na lista é um fluxo de áudio existente. Cada item da lista tem um ícone pequeno que indica o tipo de fluxo. Se o ícone for 1, o item é um fluxo de áudio. Se for 2, o item é uma pasta contendo mais fluxos.

## Fluxos de Áudio

A lista de fluxos de áudio é carregada de um arquivo chamado `streams.db`. Cada linha neste arquivo representa um fluxo de áudio. As linhas podem ser separadas por vírgulas para indicar diferentes níveis de diretórios de fluxos. Se uma linha contiver um ponto e vírgula, a primeira parte antes do ponto e vírgula será o nome do fluxo e a segunda parte será a URL do fluxo.

## Comportamento

Quando a janela de diálogo é carregada, o primeiro nível de fluxos é carregado na lista. Se um item na lista for clicado duas vezes, o comportamento depende do tipo de item. Se o item for um fluxo de áudio, o fluxo é aberto. Se o item for uma pasta, o próximo nível de fluxos é carregado na lista.