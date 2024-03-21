# Documentación de Código

El módulo `ModConstMidi` contiene constantes usadas en la manipulación de archivos MIDI y en la interacción con dispositivos MIDI. Aquí está la documentación detallada de las constantes declaradas en este módulo.

## Estados de MIDI

- `MIDISTATE_CLOSED`: Estado cuando el archivo MIDI está cerrado.
- `MIDISTATE_OPENED`: Estado cuando el archivo MIDI está abierto.
- `MIDISTATE_STARTED`: Estado cuando el archivo MIDI está iniciado.
- `MIDISTATE_STOPPED`: Estado cuando el archivo MIDI está detenido.
- `MIDISTATE_PAUSED`: Estado cuando el archivo MIDI está en pausa.
- `MIDISTATE_OPEN`: Igual a `MIDISTATE_OPENED`, para compatibilidad con versiones anteriores.

## Acciones de MidiIn

Son acciones de entrada MIDI, que incluyen abrir, cerrar, reiniciar, iniciar, detener, eliminar, hacer cola y clasificar.

## Acciones de MidiOut

Son acciones de salida MIDI, que incluyen abrir, cerrar, reiniciar, iniciar, detener, hacer cola, enviar, temporizador, pausa, eliminar y leer.

## Estados de Mensajes MIDI

Estos estados definen si un mensaje MIDI está habilitado, deshabilitado o en un estado predeterminado (ninguno).

## Puntero de Mensajes MIDI

Estos son los índices utilizados para acceder a diferentes partes de un mensaje MIDI.

## Tipos de dispositivos MidiOut

Estos son los tipos de dispositivos de salida MIDI que se pueden utilizar. Los tipos varían dependiendo del sistema operativo y la tarjeta de sonido.

## Acciones SendNoteOff

Estas son las acciones que se pueden realizar al enviar un mensaje de 'NoteOff'.

## Acciones de MidiFile

Estas son las acciones que se pueden realizar en un archivo MIDI.

## Eventos Meta de Archivos MIDI Estándar

Estas son las constantes utilizadas para los eventos meta en un archivo MIDI estándar.

## Mensajes de estado MIDI estándar

Estos son los códigos de estado para los mensajes MIDI estándar.

## Números de Controlador MIDI, CONTROLLER_CHANGE

Estas son las constantes para los números de controlador MIDI.

## Constantes de Propiedad de Filtro MIDI

Estas constantes se utilizan para filtrar diferentes mensajes MIDI.

## Constantes Comunes

Estas son constantes comunes utilizadas en todo el módulo.

Por favor, consulte la documentación relevante para cada constante para obtener más detalles sobre su uso y propósito.