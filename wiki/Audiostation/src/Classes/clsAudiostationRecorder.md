# Documentación del código

```vb
VERSION 1.0 CLASS
BEGIN
  MultiUse = -1  'True
  Persistable = 0  'NotPersistable
  DataBindingBehavior = 0  'vbNone
  DataSourceBehavior  = 0  'vbNone
  MTSTransactionMode  = 0  'NotAnMTSObject
END
Attribute VB_Name = "AudiostationRecorder"
Attribute VB_GlobalNameSpace = False
Attribute VB_Creatable = True
Attribute VB_PredeclaredId = False
Attribute VB_Exposed = False
Option Explicit
```

Este es el inicio de la clase `AudiostationRecorder`. Define que la clase puede ser usada varias veces (`MultiUse = -1`), no es persistente (`Persistable = 0`), y no tiene un comportamiento de enlace de datos (`DataBindingBehavior = 0`).

```vb
' /////////////////////////////////////////////////////////////////////////////////
' Class:            AudiostationRecorder
' Description:      Adds recorder functionality to the Audiostation program
'
' Date Changed:     25-06-2022
' Date Created:     25-06-2022
' Author:           Sibra-Soft - Alex van den Berg
' /////////////////////////////////////////////////////////////////////////////////
```

La clase `AudiostationRecorder` fue creada por Alex van den Berg de Sibra-Soft el 25-06-2022. Agrega funcionalidad de grabación al programa Audiostation.

```vb
Public Recording As Boolean
```

La variable `Recording` es una variable pública que guarda un valor booleano.

```vb
Public Sub Settings()
Call Shell(App.path & "\recorder.exe -settings", vbNormalFocus)
End Sub
```

El método `Settings` inicia el programa `recorder.exe` con la opción de configuración.

```vb
Public Sub StartRecorder()
Call Shell(App.path & "\recorder.exe -record", vbNormalFocus)
Recording = True
End Sub
```

El método `StartRecorder` inicia el programa `recorder.exe` con la opción de grabar y establece la variable `Recording` en True.

```vb
Public Sub StopRecorder()
Call Shell(App.path & "\recorder.exe -stop", vbNormalFocus)
Recording = False
End Sub
```

El método `StopRecorder` inicia el programa `recorder.exe` con la opción de detener y establece la variable `Recording` en False.

```vb
Public Sub SaveRecording()
StopRecorder
Call Shell(App.path & "\recorder.exe -save", vbNormalFocus)
End Sub
```

Finalmente, el método `SaveRecording` llama al método `StopRecorder` y luego inicia el programa `recorder.exe` con la opción de guardar.