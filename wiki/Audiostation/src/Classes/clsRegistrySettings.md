# Documentação do Código

Este código é uma implementação em VBA (Visual Basic for Applications) para interagir com o Registro do Windows. O código permite a leitura e gravação de valores de configuração no Registro.

A classe `RegistrySettings` contém duas funções principais: `WriteSetting` e `ReadSetting`. 

## Constantes

As constantes são utilizadas para definir valores fixos que são usados em várias partes do código, como códigos de erro, chaves de registro e permissões de acesso.

## Funções de API do Windows

São declaradas várias funções da API do Windows para interagir com o Registro, incluindo `RegCloseKey`, `RegCreateKeyEx`, `RegOpenKeyEx`, `RegQueryValueExString`, `RegQueryValueExNULL` e `RegSetValueExString`.

## Função WriteSetting

A função `WriteSetting` é utilizada para escrever uma configuração no Registro do Windows. Ela recebe quatro parâmetros: `sCompanyName`, `sAppName`, `sKey` e `sSetting`, que representam respectivamente a empresa, o aplicativo, a chave e o valor da configuração a serem escritos no Registro.

## Função ReadSetting

A função `ReadSetting` é utilizada para ler uma configuração do Registro do Windows. Ela recebe quatro parâmetros: `sCompanyName`, `sAppName`, `sKey` e `sDefault`. Os três primeiros parâmetros são semelhantes aos da função `WriteSetting`, enquanto o último parâmetro representa o valor padrão a ser retornado caso a chave de configuração especificada não exista no Registro.

## Manipulação de Erros

Ambas as funções utilizam uma manipulação de erros robusta para garantir que os erros sejam capturados e tratados de forma adequada, levantando erros personalizados quando os argumentos passados são inválidos ou ocorrem problemas ao interagir com o Registro.

## Encerramento

No final de ambas as funções, a chave do registro é fechada usando `RegCloseKey`, e qualquer erro que ocorreu é levantado para o chamador tratar.
