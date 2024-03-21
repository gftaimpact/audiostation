# Documentación de Código

## Versión 1.0 CLASE

### Atributos de la Clase
- MultiUse: -1 (Verdadero). Indica que el objeto puede ser utilizado de manera múltiple.
- Persistable: 0 (No Persistente). Indica que el objeto no es persistente.
- DataBindingBehavior: 0 (vbNone). Indica que no hay comportamiento de vinculación de datos.
- DataSourceBehavior: 0 (vbNone). Indica que no hay comportamiento de fuente de datos.
- MTSTransactionMode: 0 (No es un objeto MTS). Indica que no hay modo de transacción MTS.

Los atributos de VB son los siguientes:

- VB_Name: "AudiostationRecorder". Es el nombre del objeto en Visual Basic.
- VB_GlobalNameSpace: Falso. Indica que el objeto no se encuentra en el espacio de nombres global.
- VB_Creatable: Verdadero. Indica que se puede crear una instancia del objeto.
- VB_PredeclaredId: Falso. Indica que el objeto no tiene un ID predeclarado.
- VB_Exposed: Falso. Indica que el objeto no está expuesto.

## Funciones Públicas

### StartRecorder()
Esta función activa el botón de grabación en el formulario principal (Form_Main).

### StopRecorder()
Esta función desactiva el botón de grabación en el formulario principal (Form_Main).

### SaveRecording()
Esta función activa el botón de guardar en el formulario principal (Form_Main), permitiendo al usuario guardar la grabación.

### Settings()
Esta función muestra el formulario de configuración (Form_Settings) en modo modal, lo que significa que el usuario debe interactuar con él antes de poder volver al formulario principal.