# Documentação do Código

Versão: 1.0

## Classe AudiostationRecorder

Esta classe é responsável por controlar as funções de gravação de áudio.

### Atributos da Classe

- MultiUse: Define se o objeto pode ser instanciado várias vezes (valor -1 indica verdadeiro).
- Persistable: Define se o objeto é persistente (valor 0 indica não persistente).
- DataBindingBehavior e DataSourceBehavior: Estes atributos estão definidos para 0 ('vbNone'), o que significa que não possuem comportamento de vinculação de dados.
- MTSTransactionMode: Este atributo está definido como 0 ('NotAnMTSObject'), o que significa que não é um objeto MTS (Microsoft Transaction Server).
- VB_GlobalNameSpace: Define se a classe é global (valor False indica que não é global).
- VB_Creatable: Define se a classe é criável (valor True indica que é criável).
- VB_PredeclaredId: Define se um identificador foi predeclarado para a classe (valor False indica que não foi predeclarado).
- VB_Exposed: Define se a classe é exposta (valor False indica que não é exposta).

### Funções da Classe

- **StartRecorder()**: Esta função inicia a gravação. O botão de gravação do formulário principal é acionado ao chamar esta função.

- **StopRecorder()**: Esta função para a gravação. O botão de gravação do formulário principal é acionado novamente para parar a gravação ao chamar esta função.

- **SaveRecording()**: Esta função salva a gravação. O botão de salvar do formulário principal é acionado ao chamar esta função.

- **Settings()**: Esta função abre a janela de configurações em um modo modal, o que significa que o usuário deve fechar esta janela antes de poder interagir com qualquer outra janela do aplicativo.
