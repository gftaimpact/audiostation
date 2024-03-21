# Documentación del Código

Este archivo contiene el código fuente para el formulario `Form_OpenStream` en Visual Basic. Este formulario se utiliza para abrir una corriente (stream) de audio.

## Dependencias

El código hace uso de las siguientes bibliotecas:

- **MSCOMCTL.OCX**
- **TabCtl32.OCX**

## Formulario `Form_OpenStream`

Este formulario contiene los siguientes elementos:

- **TabDlg.SSTab Tab_Strip**: Una barra de pestañas con una única pestaña denominada "Existing".
- **MSComctlLib.ImageList Imagelist_Listview**: Una lista de imágenes para los elementos de la lista de streams.
- **MSComctlLib.ListView Listview_Streams**: Una lista de streams disponibles para abrir.
- **Audiostation.ButtonBig Button_Cancel**: Un botón para cancelar la operación.
- **Audiostation.ButtonBig Button_Open**: Un botón para abrir el stream seleccionado.

## Funciones y Procedimientos

### `CheckIfListviewExists`

Esta función recibe un valor y verifica si existe en la lista de streams (`Listview_Streams`).

### `OpenStreamDatabase`

Este procedimiento abre la base de datos de streams y llena la lista de streams (`Listview_Streams`) con los datos obtenidos.

### `Button_Cancel_Click`

Este procedimiento se ejecuta cuando se hace clic en el botón Cancelar. Se descarga el formulario.

### `Button_Open_Click`

Este procedimiento se ejecuta cuando se hace clic en el botón Abrir. Configura el nombre y la URL del stream seleccionado y luego descarga el formulario.

### `Form_Load`

Este procedimiento se ejecuta cuando se carga el formulario. Inicializa `CurrentRowIndex` a 0, desactiva el botón Abrir y llama a `OpenStreamDatabase`.

### `Listview_Streams_DblClick`

Este procedimiento se ejecuta cuando se hace doble clic en un ítem de la lista de streams. Si el ítem seleccionado es una carpeta, se abre la siguiente fila en la base de datos de streams. Si el ítem seleccionado es un stream, se configura el nombre y la URL del stream y se descarga el formulario.