# Documentación del Código

```vba
Attribute VB_Name = "ModLanguage"
Option Explicit
```

## Módulo: ModLanguage
El módulo ModLanguage contiene funciones para aplicaciones multilingües.

**Fecha de Creación:** 04-10-2021

**Fecha de Modificación:** 25-10-2021

**Autor:** Sibra-Soft - Alex van den Berg

---

### Función Pública: SetLanguage(Frm As Form)

Esta función establece el idioma para un formulario específico. Recorre todos los controles del formulario e invoca la función `GetLanguage` para obtener la traducción correspondiente.

**Parámetros:**
- `Frm`: El formulario para el cual se debe establecer el idioma.

**Flujo de la función:**
1. Si el formulario tiene un `Tag`, se obtiene la traducción correspondiente y se establece como título del formulario.
2. Recorre todos los controles del formulario.
3. Para cada control, si tiene un `Tag`, se obtiene la traducción correspondiente y se establece como título del control.
4. Si el control tiene un `HelpContextID`, también se obtiene la traducción correspondiente y se establece como título del control.
5. Al final, imprime en la consola de depuración el total de controles encontrados y cuántos de ellos fueron traducidos.

---

### Función Pública: GetLanguage(TextID As Integer) As String

Esta función se utiliza para obtener la traducción correspondiente para un texto específico.

**Parámetros:**
- `TextID`: El ID de texto para el cual se debe obtener la traducción.

**Flujo de la función:**
1. Llama a la función `Extensions.INIRead` para obtener la traducción del archivo INI.
2. Reemplaza todos los "\n" en la traducción obtenida con un salto de línea.
3. Devuelve la traducción.

**Nota:** El archivo INI se encuentra en el directorio "languages" del directorio de la aplicación, y su nombre es el valor de la variable `LanguageFile` con la extensión ".lng".

---