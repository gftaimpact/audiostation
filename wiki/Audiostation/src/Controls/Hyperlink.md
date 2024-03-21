# Hyperlink Control

Este control fue creado por Faraz Azhar. Su versión es la 5.00.

## Propiedades

- `Caption`: establece el texto del hipervínculo.
- `URL`: establece la URL a la que debe dirigir el hipervínculo.
- `ClickResponse`: indica qué acción se debe realizar cuando se hace clic en el hipervínculo.
- `BackColor`: establece el color de fondo del hipervínculo.
- `ColorNormal`: establece el color del hipervínculo.
- `ColorHot`: establece el color del hipervínculo cuando el cursor del ratón pasa por encima.
- `ColorDown`: establece el color del hipervínculo cuando se hace clic en él.
- `ToolTipText2`: establece el texto de la información sobre herramientas para el hipervínculo.
- `Font`: establece el tipo de letra del hipervínculo.
- `HoverUnderline`: indica si el texto del hipervínculo debe subrayarse cuando el cursor del ratón pasa por encima.

## Eventos

- `Click`: se activa cuando se hace clic en el hipervínculo.
- `OpeningURL`: se activa cuando se va a abrir una URL.

## Métodos

- `UserControl_Initialize()`: inicializa las propiedades del hipervínculo.
- `UserControl_ReadProperties(PropBag As PropertyBag)`: se utiliza para leer las propiedades del control desde el `PropertyBag`.
- `UserControl_WriteProperties(PropBag As PropertyBag)`: se utiliza para guardar las propiedades del control en el `PropertyBag`.

## Otros componentes

- `VB.Timer tmrMouse`: se utiliza para detectar la posición del cursor del ratón.
- `VB.Label lblText`: se utiliza para mostrar el texto del hipervínculo.

## Funciones de la biblioteca de Windows utilizadas

- `GetCursorPos`: obtiene la posición del cursor del ratón en la pantalla.
- `ScreenToClient`: convierte las coordenadas de la pantalla en coordenadas del cliente para la ventana especificada.
- `GetDesktopWindow`: recupera el control de la ventana del escritorio.
- `ShellExecute`: ejecuta una operación, como abrir una URL, en el hipervínculo.