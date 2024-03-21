# Documentación del Código

## Clase: Textbox_Properties

```python
class Textbox_Properties:
    def __init__(self, text, color, fontsize):
        self.text = text
        self.color = color
        self.fontsize = fontsize
```

La clase `Textbox_Properties` es responsable de almacenar las propiedades de un cuadro de texto, que incluyen el texto contenido, el color del texto y el tamaño de fuente del texto. Aquí está la documentación detallada de esta clase.

### Método: __init__(self, text, color, fontsize)

El método `__init__` es el constructor de la clase `Textbox_Properties`. Este método se llama cuando se crea una nueva instancia de la clase. Este método acepta tres parámetros: `text`, `color` y `fontsize`.

- `text` (cadena): Es el texto que se mostrará en el cuadro de texto. 
- `color` (cadena): Es el color del texto que se mostrará. 
- `fontsize` (entero): Es el tamaño de fuente del texto que se mostrará. 

### Propiedades:

- `self.text` : Almacena el texto del cuadro de texto.
- `self.color`: Almacena el color del texto.
- `self.fontsize`: Almacena el tamaño de la fuente del texto.

Esta clase es bastante simple, ya que solo incluye un constructor para inicializar sus propiedades. En futuras versiones, podríamos agregar más funcionalidades, como métodos para cambiar el color, el tamaño de la fuente o el texto.