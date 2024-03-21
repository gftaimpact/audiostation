# Documentación del Código

## Clase: Nest

Esta clase es una extensión de la clase de diccionario incorporada.

- **Versión:** 1.0
- **Fecha de Creación:** 15-11-2020
- **Fecha de Modificación:** 05-10-2021
- **Autor:** Sibra-Soft - Alex van den Berg

### Propiedades

- **MultiUse:** -1 (Verdadero)
- **Persistable:** 0 (No Persistente)
- **DataBindingBehavior:** 0 (vbNone)
- **DataSourceBehavior:** 0 (vbNone)
- **MTSTransactionMode:** 0 (No es un objeto MTS)

### Métodos

- **Clear():** Borra la colección actual.
- **Exists(sItem As String, sKey As String) As Boolean:** Verifica si un elemento o una clave existen en la colección. 
  - **sItem:** El elemento a buscar.
  - **sKey:** La clave a buscar.
- **Add(Item As Variant, Optional sKey As String, Optional Before As Variant, Optional After As Variant):** Añade un nuevo elemento a la colección. 
  - **Item:** El elemento a añadir.
  - **sKey:** La clave del elemento.
  - **Before:** (Opcional) Añade el nuevo elemento antes de este elemento.
  - **After:** (Opcional) Añade el nuevo elemento después de este elemento.
- **Item(vntIndexKey As Variant) As Variant:** Devuelve el elemento correspondiente al índice o clave proporcionado.
- **ItemKey(vntIndexKey As Variant) As String:** Devuelve la clave del elemento correspondiente al índice o clave proporcionado.
- **count() As Long:** Devuelve el número de elementos en la colección.
- **Remove(vntIndexKey As Variant):** Elimina un elemento de la colección usando su índice o clave.

### Eventos

- **Class_Initialize():** Crea la colección cuando se crea esta clase.
- **Class_Terminate():** Destruye la colección cuando esta clase se termina.