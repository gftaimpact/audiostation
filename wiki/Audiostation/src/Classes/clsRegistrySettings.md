# Documentación del Código Fuente

Esta clase se llama `RegistrySettings`. Su objetivo principal es interactuar con el registro del sistema operativo para leer y escribir configuraciones. 

## Constantes

- `REG_SZ`: Este es el tipo de valor para una cadena de texto en el registro.
- `HKEY_CURRENT_USER`: Esta es una constante que se refiere a la sección de usuario actual del registro.
- `BASE_KEY`: Esta es la llave base en el registro donde se almacenarán las configuraciones.
- `ERROR_NONE`, `ERROR_KEY_DOES_NOT_EXIST`: Estos son códigos de error específicos relacionados con las operaciones del registro.
- `READ_CONTROL`, `STANDARD_RIGHTS_READ`, `KEY_QUERY_VALUE`, `KEY_SET_VALUE`, `KEY_CREATE_SUB_KEY`, `KEY_ENUMERATE_SUB_KEYS`, `KEY_NOTIFY`, `KEY_CREATE_LINK`, `SYNCHRONIZE`: Estas son constantes utilizadas para definir los derechos de acceso al registro.

## Funciones Privadas (Windows API)

- Las funciones `RegCloseKey`, `RegCreateKeyEx`, `RegOpenKeyEx`, `RegQueryValueExString`, `RegQueryValueExNULL`, `RegSetValueExString` son funciones de la API de Windows para interactuar con el registro.

## Subrutina `WriteSetting`

Esta subrutina recibe cuatro argumentos: `sCompanyName`, `sAppName`, `sKey` y `sSetting`. El propósito de esta subrutina es escribir una configuración en el registro.

Primero, valida los argumentos de entrada para asegurar que no estén vacíos. Luego, intenta crear o abrir la clave en el registro y establece el valor de la clave. Si alguna de estas operaciones falla, se genera un error.

## Función `ReadSetting`

Esta función recibe cuatro argumentos: `sCompanyName`, `sAppName`, `sKey` y `sDefault`. El propósito de esta función es leer una configuración del registro.

Al igual que `WriteSetting`, esta función valida sus argumentos de entrada. Luego, intenta abrir la clave en el registro y leer su valor. Si la clave no existe o si ocurre algún otro error, devuelve el valor predeterminado proporcionado. Si el valor de la clave se almacena como una cadena en el registro, devuelve ese valor.