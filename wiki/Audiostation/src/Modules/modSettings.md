# Documentação do Código

O código é um módulo VB6 que fornece uma interface de programação para a leitura e gravação de chaves do Registro do Windows. Aqui está a documentação detalhada:

## Constantes

- As constantes `HKEY_CURRENT_USER`, `BASE_KEY`, `REG_SZ` e etc. são usadas para definir valores específicos necessários para as operações de registro, como o tipo de dados, chaves base e códigos de erro.

## Declarações de Função

- As funções `RegCloseKey`, `RegCreateKeyEx`, `RegOpenKeyEx`, `RegQueryValueExString`, `RegQueryValueExNULL` e `RegSetValueExString` são declarações de funções da API do Windows que permitem a manipulação do Registro do Windows.

## Subrotina `WriteSetting`

- Esta subrotina permite escrever uma configuração no Registro do Windows.
- Ela recebe quatro argumentos: `sAppName`, `sSection`, `sKey` e `sSetting` que representam o nome do aplicativo, a seção, a chave e o valor da configuração, respectivamente.
- A subrotina também inclui um manipulador de erros que retorna informações sobre quaisquer erros que possam ocorrer durante a execução.

## Função `ReadSetting`

- Esta função permite ler uma configuração do Registro do Windows.
- Ela recebe quatro argumentos: `sAppName`, `sSection`, `sKey` e `sDefault`. Os três primeiros são os mesmos que na subrotina `WriteSetting`. `sDefault` é o valor padrão que será retornado se a chave especificada não existir.
- A função também inclui um manipulador de erros que retorna informações sobre quaisquer erros que possam ocorrer durante a execução.

## Notas

- Este código está escrito em VB6, que é uma linguagem bastante antiga e não é mais suportada pela Microsoft. Se você estiver trabalhando em um novo projeto, é recomendável usar uma linguagem mais moderna, como C# ou VB.NET, que possuem suporte nativo para manipulação do Registro do Windows.