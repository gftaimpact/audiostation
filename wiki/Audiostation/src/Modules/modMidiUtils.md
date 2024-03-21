# Documentación de código fuente

## Módulo: ModMidiUtils
Este módulo contiene varias funciones utilitarias para la reproducción de MIDI.

### Variables globales

- `gisEnd`: Un booleano que indica si se ha llegado al final.
- `gisCurrentDoEvents`: Un booleano que indica si se está ejecutando el evento actual.
- `gisCurrentQueue`: Un booleano que indica si se está procesando la cola actual.
- `gisCurrentFF`: Un booleano que indica si el Fast Forward está activo.
- `gmThreadPriorityApp`: Un entero que almacena la prioridad del hilo de la aplicación.

### Constantes 

- `MB_INTEGERUBOUND`: Valor máximo para un entero.
- `MB_LONGUBOUND`: Valor máximo para un long.
- `MB_LOWNIBBLE`, `MB_HIGHNIBBLE`, `MB_LOWBYTE`, `MB_HIGHBYTE`: Constantes para operaciones bitwise.
- `MB_DOEVENTSPOLLING`: Intervalo para liberar recursos y mantener el uso de CPU por debajo del 5%.
- `MB_DEVICEID`: ID comúnmente usada por los dispositivos de salida.

### Funciones 

- `MidiNoteString2Display`: Convierte una cadena de caracteres en una representación mnemónica de las notas MIDI.
- `RoundVB5`: Función para redondear números. Necesaria porque Visual Basic 5 no tiene una función incorporada para redondear.
- `AmbientUserMode`: Determina si el programa se está ejecutando en modo de usuario.
- `GetChecksum`: Genera un checksum para una cadena de caracteres.

### Declaraciones de función de la biblioteca 

- `GetCurrentThread`, `GetPriorityClass`, `GetThreadPriority`, `SetPriorityClass`, `SetThreadPriority`: Funciones para obtener y ajustar la prioridad del hilo y del proceso.
- `Sleep`: Función para hacer una pausa en la ejecución del programa.
- `LockWindowUpdate`: Función para bloquear la actualización de una ventana.

## Nota
Esta documentación fue generada en base al código fuente proporcionado, pero no se incluyó la documentación para todas las funciones y variables debido a la longitud del código fuente. Para una documentación completa, consulte el código fuente directamente.