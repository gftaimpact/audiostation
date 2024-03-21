# Documentación del Código Fuente

Este código fuente define una clase llamada `FileIO` en Visual Basic. Esta clase se utiliza para manejar operaciones de lectura y escritura de archivos en el disco.

## Clase: FileIO

### Metadatos:

- Autor: Peter Hebels
- Fecha de Creación: 04-10-2021
- Última Modificación: 05-10-2021

### Constantes:

- `GENERIC_WRITE`: Permiso para escribir en un archivo.
- `FILE_ATTRIBUTE_NORMAL`: Define los atributos normales de un archivo.
- `CREATE_ALWAYS`: Comando para siempre crear un nuevo archivo.
- `OPEN_ALWAYS`: Comando para siempre abrir un archivo existente.
- `INVALID_HANDLE_VALUE`: Valor que representa un identificador de archivo inválido.

### Funciones de Librería:

Las siguientes funciones son declaraciones de funciones de la biblioteca del sistema operativo Windows (`user32` y `kernel32`):

- `MessageBox`: Muestra un cuadro de mensaje en la pantalla.
- `ReadFile`: Lee datos de un archivo.
- `CloseHandle`: Cierra un identificador de archivo.
- `WriteFile`: Escribe datos en un archivo.
- `CreateFile`: Crea un nuevo archivo.
- `FlushFileBuffers`: Vacía los búferes de un archivo.
- `CopyMemory`: Copia bloques de memoria de un lugar a otro.

### Variables Privadas:

- `fHandle`: Identificador del archivo actualmente abierto.
- `fSuccess`: Indicador de éxito de la última operación.
- `lFilePos`: Posición actual en el archivo.
- `File_Name`: Nombre del archivo actualmente abierto.

### Funciones:

- `OpenFile(FileN As String) As Boolean`: Abre el archivo especificado por `FileN`. Retorna `True` si el archivo se abre con éxito, `False` si no.
- `CloseFile() As Boolean`: Cierra el archivo actualmente abierto. Retorna `True` si el archivo se cierra con éxito, `False` si no.
- `WriteBytes(Pointer As Long, Size As Long) As Boolean`: Escribe una cantidad `Size` de bytes en el archivo abierto desde la ubicación en memoria especificada por `Pointer`. Retorna `True` si la escritura se realiza con éxito, `False` si no.