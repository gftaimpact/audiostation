# Documentação do Código

Este código é parte do projeto Audiostation, um programa de reprodução de arquivos de música. Ele suporta todos os tipos comuns de arquivos de mídia, como .mp3, .wav, .mid e outros.

## Formulário Sobre (Form_About)

O formulário "Sobre" oferece informações sobre o programa Audiostation.

### Propriedades

- Cor de fundo: Cinza (C0C0C0)
- Estilo de borda: Diálogo fixo
- Título: "Sobre Audiostation"
- Altura, Largura, Topo, Esquerda: Define a posição e o tamanho do formulário na tela
- Ícone: Arquivo Form_About.frx
- Pré-visualização da tecla: Verdadeiro
- LinkTopic: Form1
- Botões Max e Min: Falso
- Mostrar na barra de tarefas: Falso
- Posição de inicialização: Centro da tela

### Controles

O formulário contém várias imagens, rótulos e botões, incluindo:

- Picture2, Image1, Label1 e Label2: Exibe o logotipo e o nome do Audiostation.
- Picture1: Contém vários rótulos que fornecem informações sobre o programa e sua versão atual, designer, programador e direitos autorais.
- lnkWebsite: Um link clicável para o site do Audiostation.
- cmdClose: Um botão que fecha o formulário quando clicado.
- cmdThanks: Um botão que exibe uma caixa de mensagem com agradecimentos a várias pessoas e organizações quando clicado.

### Procedimentos de Evento

- cmdClose_Click(): Descarrega o formulário quando o botão "Fechar" é clicado.
- cmdThanks_Click(): Exibe uma caixa de mensagem com agradecimentos quando o botão "Agradecimentos" é clicado.
- Form_Load(): Define a legenda do rótulo da versão com a versão atual do aplicativo quando o formulário é carregado.