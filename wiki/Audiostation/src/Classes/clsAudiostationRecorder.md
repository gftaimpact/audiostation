# Documentação de Código

## Classe: AudiostationRecorder

A classe `AudiostationRecorder` adiciona funcionalidades de gravação ao programa Audiostation.

### Propriedades

- `Recording`: Um booleano que indica se a gravação está ocorrendo. Se verdadeiro, a gravação está em andamento. Se falso, a gravação está parada.

### Métodos

- `Settings()`: Este método executa o arquivo `recorder.exe` com a opção `-settings`. Isso abre as configurações do gravador.

- `StartRecorder()`: Este método inicia a gravação. Ele executa o arquivo `recorder.exe` com a opção `-record` e define a propriedade `Recording` como verdadeira.

- `StopRecorder()`: Este método para a gravação. Ele executa o arquivo `recorder.exe` com a opção `-stop` e define a propriedade `Recording` como falsa.

- `SaveRecording()`: Este método salva a gravação. Ele primeiro para a gravação chamando o método `StopRecorder()`, então executa o arquivo `recorder.exe` com a opção `-save`.

### Histórico

- Data de Criação: 25-06-2022
- Data de Última Modificação: 25-06-2022
- Autor: Sibra-Soft - Alex van den Berg

### Detalhes Adicionais

A classe `AudiostationRecorder` é parte do namespace global e não é persistente, não possui comportamento de vinculação de dados ou comportamento de fonte de dados, e não é um objeto MTS. A classe não está pré-declarada e não é exposta.
