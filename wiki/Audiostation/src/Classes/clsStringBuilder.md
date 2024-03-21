# Documentación del código

## Clase: StringBuilder

La clase StringBuilder se asemeja a la clase StringBuilder en .NetFramework.

### Propiedades

- `length`: Devuelve la longitud de la cadena en la memoria.
- `Capacity`: Devuelve la capacidad actual de la cadena.
- `ChunkSize`: Establece o devuelve el tamaño de los trozos de cadena almacenados.
- `toString`: Devuelve la cadena almacenada en el objeto StringBuilder.
- `TheString`: Establece la cadena almacenada en el objeto StringBuilder.

### Métodos

- `Clear()`: Limpia la cadena almacenada en el objeto StringBuilder.
- `AppendNL(sThis As String)`: Añade una cadena y una nueva línea al final de la cadena existente.
- `Append(sThis As String)`: Añade una cadena al final de la cadena existente.
- `AppendByVal(sThis As String)`: Añade una cadena al final de la cadena existente. La cadena se pasa por valor.
- `Insert(iIndex As Long, sThis As String)`: Inserta una cadena en un índice específico de la cadena existente.
- `InsertByVal(iIndex As Long, sThis As String)`: Inserta una cadena en un índice específico de la cadena existente. La cadena y el índice se pasan por valor.
- `Remove(iIndex As Long, lLen As Long)`: Elimina un segmento de la cadena existente a partir de un índice específico y con una longitud específica.
- `Find(sToFind As String, Optional lStartIndex As Long = 1, Optional compare As VbCompareMethod = vbTextCompare)`: Busca una cadena en la cadena existente y devuelve el índice de la primera aparición.
- `HeapMinimize()`: Reduce el tamaño de la cadena para que sólo se asignen los trozos mínimos.

### Eventos

- `Class_Initialize()`: Este evento se dispara cuando se crea una nueva instancia de la clase StringBuilder. Establece el tamaño predeterminado del trozo de cadena a 8192 caracteres.

### Funciones Privadas

- `UnsignedAdd(start As Long, Incr As Long) As Long`: Esta función es útil para realizar aritmética de punteros, pero sólo funciona para valores positivos de Incr.

Este código fue creado por Sibra-Soft - Alex van den Berg el 22-09-2021 y fue modificado por última vez el 05-10-2021.