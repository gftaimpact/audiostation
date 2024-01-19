# Documentação do Código

## Classe: LocalStorage

A classe LocalStorage é usada para armazenar coleções de dados, como listas de reprodução, etc.

#### Propriedades

- **IsFilterd**: Variável booleana que indica se o armazenamento está filtrado.
- **StorageContainer**: Objeto do tipo Nest que funciona como o contêiner principal de armazenamento.
- **StorageContainerTemp**: Objeto do tipo Nest que funciona como um contêiner temporário de armazenamento.

#### Métodos

- **ClearFilter()**: Este método limpa qualquer filtro aplicado ao StorageContainer, restaurando-o ao estado do StorageContainerTemp.
- **Filter(FilterString As String)**: Este método filtra o StorageContainer com base em uma string de filtro fornecida. Ele primeiro copia os itens atuais para o StorageContainerTemp, limpa o StorageContainer e, em seguida, adiciona os itens que correspondem ao filtro do StorageContainerTemp de volta ao StorageContainer.
- **IsExistingItem(KeyToFind As String) As Integer**: Este método verifica se um item com uma chave específica existe no StorageContainer. Ele retorna o índice do item ou 0 se o item não for encontrado.
- **ListviewToStorage(TargetListview As ListView, KeyColumn As Integer)**: Este método adiciona os itens de um ListView fornecido ao StorageContainer. A chave de cada item é determinada pela coluna especificada no ListView.
- **ClearStorage()**: Este método limpa o StorageContainer.
- **AddToStorage(key As String, value As String)**: Este método adiciona um item ao StorageContainer com uma chave e valor fornecidos.
- **GetItemByKey(key As String, Column As Integer) As String**: Este método retorna um item do StorageContainer com base em uma chave fornecida. O valor retornado é determinado pela coluna especificada.
- **GetItemByIndex(index As Integer, Column As Integer) As String**: Este método retorna um item do StorageContainer com base em um índice fornecido. O valor retornado é determinado pela coluna especificada.

Por favor, note que este código foi atualizado pela última vez em 05-10-2021 e foi criado inicialmente em 23-12-2018 pelo autor Alex van den Berg da Sibra-Soft.