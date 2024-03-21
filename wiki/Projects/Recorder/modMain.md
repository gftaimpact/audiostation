```markdown
# Documentación del código fuente del proyecto

## Módulo: modMain

Este módulo contiene la función principal (Main) del programa.

```vbnet
Attribute VB_Name = "modMain"
```

Esta línea asigna el nombre "modMain" al módulo.

```vbnet
Public Settings As New RegistrySettings
```
Declara una instancia pública de la clase `RegistrySettings` llamada `Settings`. Esta instancia permite acceder a los métodos y propiedades de la clase `RegistrySettings`.

### Subrutina: Main

```vbnet
Sub Main()
```
Esta es la subrutina principal del programa. Se ejecuta cuando se inicia el programa.

```vbnet
If App.PrevInstance Then
```

Esta línea comprueba si ya existe una instancia del programa. Si es así, el programa procede a la siguiente sección de código.

```vbnet
Select Case Trim(Command)
    Case "-stop": Call Settings.WriteSetting("Sibra-Soft", "Audiostation", "RecorderCommand", "stop")
    Case "-save": Call Settings.WriteSetting("Sibra-Soft", "Audiostation", "RecorderCommand", "save")
End Select
```

Si el comando de entrada es "-stop", el programa escribe la configuración "stop" en el registro. Si el comando es "-save", escribe la configuración "save" en el registro.

```vbnet
End
```

Esto termina el programa si ya existe una instancia del mismo.

```vbnet
Else
```

Si no existe una instancia previa del programa, procede a la siguiente sección de código.

```vbnet
Select Case Trim(Command)
    Case "-settings": Form_Settings.Show
    Case "-record":
        Form_Main.Hide
        Form_Main.btnRecord_Click
        
    Case Else
        End
        
End Select
```

Si el comando de entrada es "-settings", el programa mostrará el formulario de configuraciones. Si el comando es "-record", el programa ocultará el formulario principal y activará el botón de grabación. Si el comando es cualquier otra cosa, el programa terminará.

```vbnet
End If
End Sub
```

Esto marca el final de la subrutina `Main` y la finalización de la comprobación de la instancia previa.
```