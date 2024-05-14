# Documentação do arquivo RegistrySettings

## Introdução

O arquivo `RegistrySettings` é usado para manipular o registro do sistema. Ele contém métodos para ler e escrever configurações no registro.

## Dependências

Este arquivo não tem dependências externas.

## Estrutura

O arquivo é estruturado em constantes, declarações de função e dois métodos principais: `WriteSetting` e `ReadSetting`.

## Imports

Este arquivo não tem imports.

## Variáveis

Este arquivo define uma série de constantes usadas para manipular o registro do sistema. Isso inclui constantes para os tipos de valor do registro, as chaves do registro e os códigos de erro.

## Métodos

O arquivo contém dois métodos principais:

1. `WriteSetting`: Este método escreve uma configuração no registro do sistema. Ele aceita quatro argumentos: `sCompanyName`, `sAppName`, `sKey` e `sSetting`. Ele levanta erros se qualquer um dos três primeiros argumentos estiver vazio.

2. `ReadSetting`: Este método lê uma configuração do registro do sistema. Ele aceita quatro argumentos: `sCompanyName`, `sAppName`, `sKey` e `sDefault`. Ele levanta erros se qualquer um dos três primeiros argumentos estiver vazio. Se a chave especificada não existir no registro, o método retorna o valor padrão.

## Exemplo

Para escrever uma configuração no registro:

```vba
WriteSetting "MyCompany", "MyApp", "MyKey", "MySetting"
```

Para ler uma configuração do registro:

```vba
ReadSetting "MyCompany", "MyApp", "MyKey", "DefaultValue"
```

## Diagrama de dependências

```
graph TD;
  WriteSetting-->RegCreateKeyEx;
  WriteSetting-->RegSetValueExString;
  WriteSetting-->RegCloseKey;
  ReadSetting-->RegOpenKeyEx;
  ReadSetting-->RegQueryValueExNULL;
  ReadSetting-->RegQueryValueExString;
  ReadSetting-->RegCloseKey;
```

## Notas

Este arquivo usa a API do Windows para manipular o registro do sistema.

## Vulnerabilidades

Este arquivo não tem vulnerabilidades conhecidas. No entanto, é importante notar que a manipulação incorreta do registro do sistema pode causar problemas graves. Portanto, use este código com cuidado.