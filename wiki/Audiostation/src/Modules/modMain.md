# Documentación del Código Fuente

## Módulo: ModMain
**Descripción:** Módulo principal de la aplicación del programa

**Fecha de Modificación:** 25-06-2022

**Fecha de Creación:** 04-10-2021

**Autor:** Sibra-Soft - Alex van den Berg

---

## Variables Globales y Constantes

- `Public LanguageFile As String`: Almacena el archivo de idioma para la aplicación.
- `Public Const MAXDRIVES = 10`: Define el número máximo de unidades.
- `Public curdrive As Long`: Almacena la unidad actual.
- `Public stream(MAXDRIVES) As Long`: Almacena los flujos para cada unidad.
- `Public seeking As Long`: Almacena el valor de búsqueda en el flujo actual.
- `Public IsDebuggig As Boolean`: Almacena si la aplicación está en modo de depuración.
- `Public PlayStateMediaMode As enumMediaMode`: Almacena el estado de reproducción del medio actual.

---

## Objetos

- `Public Mp3Info As New Mp3Info`: Objeto para obtener información sobre un archivo MP3.
- `Public WebRequest As New WebClient`: Objeto para realizar solicitudes web.
- `Public Settings As New RegistrySettings`: Objeto para manejar la configuración del registro.
- `Public Extensions As New SibraSoft`: Objeto para manejar funciones de extensión.
- `Public AudioStaRecorder As New AudiostationRecorder`: Objeto para manejar la grabación de audio.
- `Public AudioStaStreamer As New AudiostationSteamer`: Objeto para manejar la transmisión de audio.

---

## Subrutinas

- `Public Sub Main()`: Subrutina principal que llama al constructor de la aplicación.
- `Public Sub OpenFile(MediaFile As String)`: Subrutina para abrir un archivo de medios. Esta subrutina maneja varios tipos de archivos de medios y determina la acción apropiada para cada uno.
- `Public Sub ApplicationConstructor()`: Subrutina para inicializar la aplicación. Se comprueba si el programa se está ejecutando en modo de depuración, se verifica la existencia de la carpeta temporal, se establece el idioma de la aplicación y se abre el archivo de medios cargado si existe.
- `Public Sub ApplicationDestructor()`: Subrutina para liberar recursos cuando la aplicación se cierra. Libera el canal y libera los recursos de BASS.
