# Documentación del Código Fuente

## Módulo: ModBassNetRadio

Este módulo es responsable de la funcionalidad de la radio por Internet en la aplicación.

```vb
Attribute VB_Name = "ModBassNetRadio"
Option Explicit
```

Aquí se declaran las variables públicas utilizadas en todo el módulo.

```vb
Public Url As Variant
Public TmpNameHold As String
Public TmpNameHold2 As String
Public proxy(100) As Byte ' proxy server
```

Se define un objeto FileIO para guardar una copia local del stream de audio.

```vb
' SAVE LOCAL COPY
Public WriteFile As New FileIO
Public FileIsOpen As Boolean, GotHeader As Boolean
Public DownloadStarted As Boolean, DoDownload As Boolean
Public DlOutput As String, SongNameUpdate As Boolean
```

Se utilizan funciones para la creación de hilos y el manejo de cajas de mensajes.

```vb
' THREADING
Public cthread As Long
Public Declare Function CreateThread Lib "kernel32" (lpThreadAttributes As Any, ByVal dwStackSize As Long, ByVal lpStartAddress As Long, ByVal lpParameter As String, ByVal dwCreationFlags As Long, lpThreadID As Long) As Long
Private Declare Function CloseHandle Lib "kernel32" (ByVal hObject As Long) As Long

' MESSAGE BOX
Public Declare Function MessageBox Lib "user32" Alias "MessageBoxA" (ByVal hwnd As Long, ByVal lpText As String, ByVal lpCaption As String, ByVal wType As Long) As Long
Public Declare Sub Sleep Lib "kernel32" (ByVal dwMilliseconds As Long)
```

Las subs `DoMeta`, `MetaSync` y `EndSync` se utilizan para manejar los metadatos de la transmisión de audio.

```vb
Sub DoMeta()
...
End Sub

Sub MetaSync(ByVal handle As Long, ByVal channel As Long, ByVal data As Long, ByVal user As Long)
...
End Sub

Sub EndSync(ByVal handle As Long, ByVal channel As Long, ByVal data As Long, ByVal user As Long)
...
End Sub
```

La sub `SUBDOWNLOADPROC` es utilizada para manejar la descarga del audio.

```vb
Public Sub SUBDOWNLOADPROC(ByVal buffer As Long, ByVal length As Long, ByVal user As Long)
...
End Sub
```

La función `RemoveSpecialChar` se utiliza para limpiar el nombre del archivo del audio descargado.

```vb
Public Function RemoveSpecialChar(strFilename As String)
...
End Function
```