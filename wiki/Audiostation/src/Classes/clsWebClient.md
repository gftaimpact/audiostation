# Documentação do Código

## Classe: WebClient

A classe `WebClient` é utilizada para fazer requisições web e obter informações da internet.

### Propriedades:
- `QuerystringParameters`: Esta propriedade é usada para armazenar os parâmetros da querystring.

### Métodos:

#### `GenerateQuerystring`

Esta função privada é usada para gerar uma string de querystring a partir dos parâmetros armazenados na propriedade `QuerystringParameters`. A função itera sobre todos os parâmetros armazenados e os concatena em uma única string, separando cada par com o caractere '&'.

#### `WebRequest(Url As String) As String`

Esta função pública é usada para realizar uma requisição web. Aceita uma URL como parâmetro e retorna a resposta como uma string. A função cria uma nova instância do objeto `MSXML2.XMLHTTP60` para realizar a requisição. Se houver parâmetros na propriedade `QuerystringParameters`, eles são adicionados à URL antes de a requisição ser enviada. A resposta da requisição é retornada como uma string.

### Detalhes da Implementação:
Esta classe foi criada por Alex van den Berg da Sibra-Soft. Foi criada em 16-08-2021 e a última alteração foi feita em 05-10-2021.

### Exemplo de Uso:
```vba
Dim client As New WebClient
client.QuerystringParameters.Add "param1", "value1"
client.QuerystringParameters.Add "param2", "value2"
Dim response As String
response = client.WebRequest("http://example.com")
```
Neste exemplo, um novo objeto `WebClient` é criado, dois parâmetros são adicionados à `QuerystringParameters` e uma requisição web é feita para "http://example.com". A resposta da requisição é armazenada na variável `response`.