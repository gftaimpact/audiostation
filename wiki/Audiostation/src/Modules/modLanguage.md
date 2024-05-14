# Documentação do arquivo ModLanguage

## Introdução

Este arquivo contém funções para aplicações multi-idioma. O módulo foi criado por Alex van den Berg da Sibra-Soft e foi modificado pela última vez em 25-10-2021.

## Dependências

Dependências do arquivo não são explicitamente mencionadas no código.

## Estrutura

O arquivo contém duas funções principais: `SetLanguage` e `GetLanguage`.

## Variáveis

`ControlCount`: Usada para contar o número total de controles no formulário.

`ControlTranslateCount`: Usada para contar o número de controles traduzidos.

`ControlMenuTranslateCount`: Usada para contar o número de itens de menu traduzidos.

`CurrentControl`: Usada para iterar sobre todos os controles no formulário.

## Métodos

`SetLanguage(Frm as Form)`: Esta função é usada para definir o idioma de um determinado formulário. Ela percorre todos os controles no formulário e, se a tag do controle não for nula, traduz o controle usando a função `GetLanguage`. Além disso, traduz os itens de menu se `HelpContextID` não for 0.

`GetLanguage(TextID as Integer) as String`: Esta função obtém o texto traduzido para um determinado `TextID` do arquivo de idioma correspondente. 

## Exemplo de uso

Para definir o idioma de um formulário:

```vba
SetLanguage(Me)
```

Para obter o texto traduzido para um determinado `TextID`:

```vba
translatedText = GetLanguage(TextID)
```

## Diagrama de dependências

Diagrama de dependências não é aplicável neste caso, pois o arquivo contém apenas duas funções e nenhuma classe.

## Notas

Este módulo é usado para traduzir o texto de controles e itens de menu em um formulário para diferentes idiomas.

## Vulnerabilidades

Vulnerabilidades do arquivo não são mencionadas explicitamente. No entanto, a função `GetLanguage` usa a função `INIRead` que não está definida neste módulo, então é necessário garantir que essa função esteja disponível no escopo onde este módulo está sendo usado. Além disso, a função `SetLanguage` usa a propriedade `Tag` dos controles para determinar se o controle deve ser traduzido ou não. Portanto, é importante definir corretamente a propriedade `Tag` dos controles.