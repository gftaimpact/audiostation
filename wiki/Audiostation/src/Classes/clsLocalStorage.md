# Documentación del Código

## Clase: LocalStorage

### Descripción:
Esta clase se utiliza para almacenar datos de colección, como listas de reproducción, etc.

### Métodos y Propiedades

#### Propiedad: IsFilterd
Un valor booleano que indica si el contenedor de almacenamiento ha sido filtrado.

#### Propiedad: StorageContainer
Una instancia de la clase Nest para almacenar datos.

#### Método: ClearFilter()
Este método restaura el contenedor de almacenamiento a su estado antes de ser filtrado.

#### Método: Filter(FilterString As String)
Este método filtra el contenedor de almacenamiento con base en la cadena de filtrado proporcionada. Los datos que coincidan con la cadena de filtrado se mantendrán en el contenedor de almacenamiento.

#### Método: IsExistingItem(KeyToFind As String) As Integer
Este método verifica si existe un elemento con la clave proporcionada en el contenedor de almacenamiento. Devuelve la posición del elemento en el contenedor de almacenamiento si existe, de lo contrario, devuelve 0.

#### Método: ListviewToStorage(TargetListview As ListView, KeyColumn As Integer)
Este método transfiere todos los elementos en una vista de lista dada al contenedor de almacenamiento. La columna que se utilizará como clave para los datos de almacenamiento se proporciona en el argumento KeyColumn.

#### Método: ClearStorage()
Este método borra todos los datos en el contenedor de almacenamiento.

#### Método: AddToStorage(key As String, value As String)
Este método agrega un nuevo elemento al contenedor de almacenamiento con la clave y el valor proporcionados.

#### Método: GetItemByKey(key As String, Column As Integer) As String
Este método recupera el valor de un elemento en el contenedor de almacenamiento utilizando la clave proporcionada. La columna del valor a recuperar se proporciona en el argumento Column.

#### Método: GetItemByIndex(index As Integer, Column As Integer) As String
Este método recupera el valor de un elemento en el contenedor de almacenamiento utilizando el índice proporcionado. La columna del valor a recuperar se proporciona en el argumento Column.

### Historia:
- Creado el: 23-12-2018
- Cambiado el: 05-10-2021
- Autor: Sibra-Soft - Alex van den Berg