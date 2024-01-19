# Documentação do Módulo ModLanguage

## Descrição
Este módulo contém funções diversas para aplicações multilíngues. O módulo foi criado por Alex van den Berg da Sibra-Soft em 04-10-2021 e foi modificado pela última vez em 25-10-2021.

## Funções

### SetLanguage(Frm As Form)
Esta função é utilizada para configurar o idioma de um formulário. Recebe como parâmetro um formulário (`Frm`) e realiza a tradução dos controles do formulário e dos itens de menu. A função utiliza a função `GetLanguage` para obter a tradução dos controles e itens de menu.

#### Parâmetros
- `Frm`: Formulário cujo idioma deve ser configurado.

#### Funcionamento
A função itera sobre todos os controles do formulário. Se o Tag do controle não for nulo, o Caption do controle é definido para a tradução do Tag. Se o HelpContextID do controle não for zero, o Caption do controle é definido para a tradução do HelpContextID.

Ao final da execução, a função imprime no console a quantidade de controles encontrados, a quantidade de controles traduzidos e a quantidade de itens de menu traduzidos.

### GetLanguage(TextID As Integer) As String
Esta função é utilizada para obter a tradução de um texto. Recebe como parâmetro o ID do texto (`TextID`) e retorna a tradução do texto.

#### Parâmetros
- `TextID`: ID do texto a ser traduzido.

#### Funcionamento
A função lê o arquivo de idioma, busca a tradução do texto com o ID fornecido e retorna a tradução. A função substitui todas as ocorrências de "\n" na tradução por uma quebra de linha.

#### Retorno
Retorna a tradução do texto com o ID fornecido. Se a tradução não for encontrada, retorna uma string vazia.