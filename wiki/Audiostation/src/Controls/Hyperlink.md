# Documentação do Código

Este código é uma implementação de um controle de usuário VB (Visual Basic) chamado "Hyperlink". O controle se comporta como um link de hiperlink que é comumente usado em páginas da web. Quando clicado, ele pode abrir uma URL ou disparar um evento de clique.

## Estrutura do código

O código começa com a inicialização do controle do usuário com as propriedades como altura, largura, posição e outros atributos do controle.

Em seguida, ele define uma série de constantes e tipos que são usados posteriormente no código.

Depois disso, uma série de funções do Windows API são declaradas. Estas são usadas para obter a posição do cursor do mouse e para abrir a URL.

Os eventos e propriedades que este controle do usuário irá fornecer são então definidos. Estes incluem eventos de clique e abertura de URL, e propriedades como a URL para abrir, a resposta ao clique e a cor do link.

No restante do código, os métodos para lidar com os eventos do mouse (clicar, mover, soltar) são definidos, assim como os métodos para lidar com a inicialização do controle do usuário e a alteração do estado do controle.

## Detalhes do código

A maior parte do comportamento deste controle é definida nos métodos que lidam com os eventos do mouse.

- No método `lblText_Click`, o controle verifica se deve abrir uma URL ou disparar um evento de clique quando o usuário clica no link.

- Nos métodos `lblText_MouseDown`, `lblText_MouseMove` e `lblText_MouseUp`, o controle muda a cor do link para indicar se o mouse está sobre o link e se o botão do mouse está pressionado.

O controle também fornece uma série de propriedades que permitem ao usuário do controle personalizar seu comportamento e aparência, como a URL a ser aberta, a cor do link, e se deve sublinhar o link quando o mouse passa sobre ele.

## Autor

Este controle foi criado por Faraz Azhar.