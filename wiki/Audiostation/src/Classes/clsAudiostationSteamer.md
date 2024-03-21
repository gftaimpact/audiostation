# Documentación de Código

## Clase: AudiostationStreamer

Esta clase agrega funcionalidad de transmisión al programa Audiostation.

### Metadatos
* **Versión:** 1.0
* **Cambio reciente:** 05-10-2021
* **Fecha de Creación:** 04-10-2021
* **Autor:** Sibra-Soft - Alex van den Berg

### Atributos Públicos
* `MetaTitle`: String - Título de metadatos
* `Status`: String - Estado actual de la transmisión
* `Url`: String - URL de la transmisión
* `Name`: String - Nombre de la transmisión
* `Error`: Boolean - Indica si hay un error en la transmisión

### Métodos Públicos

#### `Public Function OpenStream(Url As String, Optional Name As String = vbNullString) As Boolean`

Este método intenta abrir una transmisión de audio desde la URL proporcionada.

**Parámetros:**

* `Url`: String - La URL de la transmisión.
* `Name`: String (opcional) - El nombre de la transmisión.

**Retorno:**

* Boolean: Retorna `True` si la transmisión se abre correctamente, `False` en caso contrario. 

**Flujo de funcionamiento:**

1. Configura el proxy de la red y libera cualquier canal de transmisión anterior.
2. Intenta crear un nuevo canal de transmisión con la URL proporcionada.
3. Si no se puede crear el canal de transmisión, muestra un mensaje de error y retorna `False`.
4. Si se crea el canal de transmisión correctamente, asigna la URL y el Nombre a los atributos correspondientes y retorna `True`.

**Manejo de errores:**

En caso de que no se pueda abrir la transmisión, el método establece el atributo `Error` a `True` y `Status` a "No se está reproduciendo".