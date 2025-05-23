# FenextjsValidator

Clase para validar datos de entrada, proporcionando métodos para verificar requerimientos, longitudes, y tipos específicos de validaciones.

### Importación

Para importar el componente FenextjsValidator, se puede hacer desde fenextjs

```tsx copy
import { FenextjsValidator } from "fenextjs";
```

## isEqual

Método para definir la validación 'isEqual'. Establece la regla de que los datos deben ser iguales al valor especificado.

### Parámetros

| Parámetro | Tipo     | Requerido | Default | Descripcion                                                             |
| --------- | -------- | --------- | ------- | ----------------------------------------------------------------------- |
| d         | T[] \| T | sí        |         | Valor o lista de valores con los que se compararán los datos a validar. |
| msg       | string   | no        |         | Mensaje de error personalizado que se mostrará si la validación falla.  |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación de igualdad

```tsx copy
const validator = FenextjsValidator();
validator.isEqual("value1");
```

- Definir validación con mensaje de error personalizado

```tsx copy
const validator = FenextjsValidator();
validator.isEqual("value1", "Los valores no son iguales");
```

## isRequired

Método para habilitar la validación 'isRequired'. Establece la regla de que los datos deben estar presentes y no ser nulos o indefinidos.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion                                                            |
| --------- | ------ | --------- | ------- | ---------------------------------------------------------------------- |
| msg       | string | no        |         | Mensaje de error personalizado que se mostrará si la validación falla. |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación de requerimiento

```tsx copy
const validator = FenextjsValidator();
validator.isRequired();
```

- Definir validación con mensaje de error personalizado

```tsx copy
const validator = FenextjsValidator();
validator.isRequired("Los datos son obligatorios");
```

## isBoolean

Método para habilitar la validación 'isBoolean'. Establece la regla de que los datos deben ser de tipo booleano.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion                                                            |
| --------- | ------ | --------- | ------- | ---------------------------------------------------------------------- |
| msg       | string | no        |         | Mensaje de error personalizado que se mostrará si la validación falla. |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación de tipo booleano

```tsx copy
const validator = FenextjsValidator();
validator.isBoolean();
```

- Definir validación con mensaje de error personalizado

```tsx copy
const validator = FenextjsValidator();
validator.isBoolean("Debe ser un valor booleano");
```

## isNumber

Método para habilitar la validación 'isNumber'. Establece la regla de que los datos deben ser de tipo número.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion                                                            |
| --------- | ------ | --------- | ------- | ---------------------------------------------------------------------- |
| msg       | string | no        |         | Mensaje de error personalizado que se mostrará si la validación falla. |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación de tipo número

```tsx copy
const validator = FenextjsValidator();
validator.isNumber();
```

- Definir validación con mensaje de error personalizado

```tsx copy
const validator = FenextjsValidator();
validator.isNumber("Debe ser un número");
```

## isString

Método para habilitar la validación 'isString'. Establece la regla de que los datos deben ser de tipo cadena (string).

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion                                                            |
| --------- | ------ | --------- | ------- | ---------------------------------------------------------------------- |
| msg       | string | no        |         | Mensaje de error personalizado que se mostrará si la validación falla. |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación de tipo cadena

```tsx copy
const validator = FenextjsValidator();
validator.isString();
```

- Definir validación con mensaje de error personalizado

```tsx copy
const validator = FenextjsValidator();
validator.isString("Debe ser una cadena");
```

## isLength

Método para habilitar la validación de longitud. Establece la regla de que los datos deben tener una longitud específica.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion                                                              |
| --------- | ------ | --------- | ------- | ------------------------------------------------------------------------ |
| length    | number | sí        |         | La longitud que deben tener los datos para que la validación sea válida. |
| msg       | string | no        |         | Mensaje de error personalizado que se mostrará si la validación falla.   |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación de longitud

```tsx copy
const validator = FenextjsValidator();
validator.isLength(5);
```

- Definir validación con mensaje de error personalizado

```tsx copy
const validator = FenextjsValidator();
validator.isLength(5, "La longitud debe ser 5");
```

## isDate

Método para habilitar la validación 'isDate'. Establece la regla de que los datos deben ser de tipo Date (fecha).

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion                                                            |
| --------- | ------ | --------- | ------- | ---------------------------------------------------------------------- |
| msg       | string | no        |         | Mensaje de error personalizado que se mostrará si la validación falla. |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación de tipo fecha

```tsx copy
const validator = FenextjsValidator();
validator.isDate();
```

- Definir validación con mensaje de error personalizado

```tsx copy
const validator = FenextjsValidator();
validator.isDate("Debe ser una fecha válida");
```

## isObject

Método para habilitar la validación 'isObject'. Establece la regla de que los datos deben ser de tipo objeto.

### Parámetros

| Parámetro | Tipo                                                        | Requerido | Default | Descripcion                                                            |
| --------- | ----------------------------------------------------------- | --------- | ------- | ---------------------------------------------------------------------- |
| obj       | \{ [id in keyof T]?: FenextjsValidatorClass \} \| undefined | sí        |         | Objeto con las reglas de validación para cada propiedad del objeto.    |
| msg       | string                                                      | no        |         | Mensaje de error personalizado que se mostrará si la validación falla. |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación de tipo objeto

```tsx copy
const validator = FenextjsValidator();
validator.isObject({
  propertyName: FenextjsValidator().isString(),
});
```

- Definir validación con reglas de propiedades y mensaje de error personalizado

```tsx copy
const validator = FenextjsValidator();
validator.isObject(
  {
    propertyName: FenextjsValidator().isString("Debe ser una cadena"),
  },
  "El objeto no es válido",
);
```

## isArray

Método para habilitar la validación 'isArray'. Establece la regla de que los datos deben ser un array.

### Parámetros

| Parámetro | Tipo                                | Requerido | Default | Descripcion                                                                                           |
| --------- | ----------------------------------- | --------- | ------- | ----------------------------------------------------------------------------------------------------- |
| item      | FenextjsValidatorClass \| undefined | no        |         | Instancia de FenextjsValidatorClass que define las reglas de validación para cada elemento del array. |
| msg       | string                              | no        |         | Mensaje de error personalizado que se mostrará si la validación falla.                                |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación de tipo array

```tsx copy
const validator = FenextjsValidator();
validator.isArray();
```

- Definir validación de array con reglas para sus elementos

```tsx copy
const validator = FenextjsValidator();
validator.isArray(FenextjsValidator().isString());
```

- Definir validación con mensaje de error personalizado

```tsx copy
const validator = FenextjsValidator();
validator.isArray(
  FenextjsValidator().isString("Cada elemento debe ser una cadena"),
);
```

## isMin

Método para habilitar la validación 'isMin'. Establece la regla de que los datos deben ser mayores que un valor específico.

### Parámetros

| Parámetro | Tipo           | Requerido | Default | Descripcion                                                                 |
| --------- | -------------- | --------- | ------- | --------------------------------------------------------------------------- |
| min       | number \| Date | sí        |         | Valor mínimo que los datos deben superar para que la validación sea válida. |
| msg       | string         | no        |         | Mensaje de error personalizado que se mostrará si la validación falla.      |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación de valor mínimo

```tsx copy
const validator = FenextjsValidator();
validator.isMin(10);
```

- Definir validación con mensaje de error personalizado

```tsx copy
const validator = FenextjsValidator();
validator.isMin(10, "El valor debe ser mayor que 10");
```

- Definir validación con valor mínimo de fecha

```tsx copy
const validator = FenextjsValidator();
validator.isMin(new Date("2024-01-01"));
```

## isMinOrEqual

Método para habilitar la validación 'isMinOrEqual'. Establece la regla de que los datos deben ser mayores o iguales que un valor específico.

### Parámetros

| Parámetro | Tipo           | Requerido | Default | Descripcion                                                                           |
| --------- | -------------- | --------- | ------- | ------------------------------------------------------------------------------------- |
| min       | number \| Date | sí        |         | Valor mínimo que los datos deben superar o igualar para que la validación sea válida. |
| msg       | string         | no        |         | Mensaje de error personalizado que se mostrará si la validación falla.                |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación de valor mínimo o igual

```tsx copy
const validator = FenextjsValidator();
validator.isMinOrEqual(10);
```

- Definir validación con mensaje de error personalizado

```tsx copy
const validator = FenextjsValidator();
validator.isMinOrEqual(10, "El valor debe ser mayor o igual a 10");
```

- Definir validación con valor mínimo o igual de fecha

```tsx copy
const validator = FenextjsValidator();
validator.isMinOrEqual(new Date("2024-01-01"));
```

## isMax

Método para habilitar la validación 'isMax'. Establece la regla de que los datos deben ser menores que un valor específico.

### Parámetros

| Parámetro | Tipo           | Requerido | Default | Descripcion                                                                            |
| --------- | -------------- | --------- | ------- | -------------------------------------------------------------------------------------- |
| max       | number \| Date | sí        |         | Valor máximo que los datos deben ser menores que él para que la validación sea válida. |
| msg       | string         | no        |         | Mensaje de error personalizado que se mostrará si la validación falla.                 |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación de valor máximo

```tsx copy
const validator = FenextjsValidator();
validator.isMax(100);
```

- Definir validación con mensaje de error personalizado

```tsx copy
const validator = FenextjsValidator();
validator.isMax(100, "El valor debe ser menor que 100");
```

- Definir validación con valor máximo de fecha

```tsx copy
const validator = FenextjsValidator();
validator.isMax(new Date("2024-01-01"));
```

## isMaxOrEqual

Método para habilitar la validación 'isMaxOrEqual'. Establece la regla de que los datos deben ser menores o iguales que un valor específico.

### Parámetros

| Parámetro | Tipo           | Requerido | Default | Descripcion                                                                                      |
| --------- | -------------- | --------- | ------- | ------------------------------------------------------------------------------------------------ |
| max       | number \| Date | sí        |         | Valor máximo que los datos deben ser menores o iguales que él para que la validación sea válida. |
| msg       | string         | no        |         | Mensaje de error personalizado que se mostrará si la validación falla.                           |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación de valor máximo o igual

```tsx copy
const validator = FenextjsValidator();
validator.isMaxOrEqual(100);
```

- Definir validación con mensaje de error personalizado

```tsx copy
const validator = FenextjsValidator();
validator.isMaxOrEqual(100, "El valor debe ser menor o igual que 100");
```

- Definir validación con valor máximo o igual de fecha

```tsx copy
const validator = FenextjsValidator();
validator.isMaxOrEqual(new Date("2024-01-01"));
```

## isCompareRef

Método para habilitar la comparación de valores de referencia. Establece la regla de que los datos deben ser iguales a otro valor de referencia almacenado en la instancia.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion                                                                                    |
| --------- | ------ | --------- | ------- | ---------------------------------------------------------------------------------------------- |
| refKey    | string | sí        |         | La clave que identifica el valor de referencia almacenado en la instancia para la comparación. |
| msg       | string | no        |         | Mensaje de error personalizado que se mostrará si la validación falla.                         |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación de comparación con valor de referencia

```tsx copy
const validator = FenextjsValidator();
validator.isCompareRef("myRefKey");
```

- Definir validación con mensaje de error personalizado

```tsx copy
const validator = FenextjsValidator();
validator.isCompareRef("myRefKey", "Los valores no coinciden");
```

## isWhen

Método para habilitar la validación 'isWhen'. Establece la regla de comparación cuando se cumpla una condición específica.

### Parámetros

| Parámetro | Tipo                              | Requerido | Default | Descripcion                                                                                                                                                                                                                                       |
| --------- | --------------------------------- | --------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| data      | FenextjsValidatorClassIsWhenProps | sí        |         | Objeto que contiene las reglas de validación a aplicar cuando la condición especificada sea verdadera. La estructura de 'FenextjsValidatorClassIsWhenProps' incluye los campos 'key', 'is', 'then', 'otherwise', y opcionalmente 'dataIsCurrent'. |

### Condiciones en 'isWhen'

El método 'isWhen' permite aplicar validaciones condicionales basadas en los valores de las propiedades. A continuación se describen las posibles condiciones y el comportamiento de cada una:

| Condición     | Descripción                                                                                                                                                                 |
| ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| key           | El campo 'key' es el nombre de la propiedad a evaluar. Se usará para determinar si la validación debe aplicarse a esa propiedad.                                            |
| is            | La propiedad 'is' contiene una instancia de 'FenextjsValidatorClass' que define las reglas de validación para aplicar cuando se cumpla la condición.                        |
| then          | La propiedad 'then' contiene una instancia de 'FenextjsValidatorClass' que define las reglas de validación a aplicar si la condición es verdadera.                          |
| otherwise     | La propiedad 'otherwise' contiene una instancia de 'FenextjsValidatorClass' que define las reglas de validación a aplicar si la condición es falsa. Este campo es opcional. |
| dataIsCurrent | La propiedad 'dataIsCurrent' es un valor booleano opcional que indica si se debe comparar la propiedad con los datos actuales. Si no se establece, se asumirá como 'false'. |

### Returns

| Parametro | Tipo                   | Descripcion                                                                   |
| --------- | ---------------------- | ----------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia de la clase para permitir el encadenamiento de métodos. |

### Usos

- Definir validación 'isWhen' con una condición

```tsx copy
const validator = FenextjsValidator();
validator.isWhen({
  key: "age",
  is: validator.isNumber(),
  then: validator.isMin(18),
});
```

- Definir validación 'isWhen' con condiciones múltiples y alternativa

```tsx copy
const validator = FenextjsValidator();
validator.isWhen({
  key: "age",
  is: validator.isNumber(),
  then: validator.isMin(18),
  otherwise: validator.isMax(65),
});
validator.isWhen({
  key: "name",
  is: validator.isString(),
  then: validator.isLength(3),
});
```

## isRegex

Método para habilitar la validación 'isRegex'. Establece la regla de que los datos deben coincidir con una expresión regular especificada.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion                                                                                |
| --------- | ------ | --------- | ------- | ------------------------------------------------------------------------------------------ |
| data      | RegExp | sí        |         | Expresión regular con la que los datos deben coincidir para que la validación sea éxitosa. |
| msg       | string | no        |         | Mensaje de error personalizado que se muestra si la validación falla.                      |

### Returns

| Parametro | Tipo                   | Descripcion                                                                                                   |
| --------- | ---------------------- | ------------------------------------------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia actual de la clase FenextjsValidatorClass, lo que permite el encadenamiento de métodos. |

### Usos

- Habilitar validación 'isRegex'

```tsx copy
const validator = FenextjsValidator();
validator.isRegex(
  /^[a-zA-Z0-9]+$/,
  "El valor debe contener solo caracteres alfanuméricos",
);
```

## isEmail

Método para habilitar la validación 'isEmail'. Establece la regla de que los datos deben ser un correo electrónico válido.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion                                                           |
| --------- | ------ | --------- | ------- | --------------------------------------------------------------------- |
| msg       | string | no        |         | Mensaje de error personalizado que se muestra si la validación falla. |

### Returns

| Parametro | Tipo                   | Descripcion                                                                                                   |
| --------- | ---------------------- | ------------------------------------------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia actual de la clase FenextjsValidatorClass, lo que permite el encadenamiento de métodos. |

### Usos

- Habilitar validación 'isEmail'

```tsx copy
const validator = FenextjsValidator();
validator.isEmail("Por favor, ingresa un correo electrónico válido");
```

## isCustom

Método para habilitar la validación 'onCustom'. Establece la regla de que los datos deben cumplir con una validación personalizada definida por una función.

### Parámetros

| Parámetro | Tipo                                                                 | Requerido | Default | Descripcion                                                                                                           |
| --------- | -------------------------------------------------------------------- | --------- | ------- | --------------------------------------------------------------------------------------------------------------------- |
| data      | (data: T, parent?: FenextjsValidatorClass) =\> true \| ErrorFenextjs | sí        |         | Función que define la validación personalizada. Si la validación falla, debe retornar un error de tipo ErrorFenextjs. |
| msg       | string                                                               | no        |         | Mensaje de error personalizado que se muestra si la validación falla.                                                 |

### Returns

| Parametro | Tipo                   | Descripcion                                                                                                   |
| --------- | ---------------------- | ------------------------------------------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia actual de la clase FenextjsValidatorClass, lo que permite el encadenamiento de métodos. |

### Usos

- Habilitar validación 'isCustom'

```tsx copy
const validator = FenextjsValidator();
validator.isCustom((data) => {
  if (data.length < 5) return new ErrorFenextjs("El valor es demasiado corto");
  return true;
}, "Error en validación personalizada");
```

## isOr

Método para definir la validación 'isOr'. Establece la regla de que los datos deben cumplir al menos una validación de las proporcionadas.

### Parámetros

| Parámetro | Tipo                     | Requerido | Default | Descripcion                                                                                              |
| --------- | ------------------------ | --------- | ------- | -------------------------------------------------------------------------------------------------------- |
| d         | FenextjsValidatorClass[] | sí        |         | Lista de instancias de FenextjsValidatorClass que representan las validaciones a comparar con los datos. |
| msg       | string                   | no        |         | Mensaje de error personalizado que se muestra si la validación falla.                                    |

### Returns

| Parametro | Tipo                   | Descripcion                                                                                                   |
| --------- | ---------------------- | ------------------------------------------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia actual de la clase FenextjsValidatorClass, lo que permite el encadenamiento de métodos. |

### Usos

- Habilitar validación 'isOr'

```tsx copy
const validator = FenextjsValidator();
const validator1 = FenextjsValidator().isRequired();
const validator2 = FenextjsValidator().isEmail();
validator.isOr(
  [validator1, validator2],
  "Debe ser un valor requerido o un email válido",
);
```

## isEnum

Método para habilitar la validación 'isEnum'. Establece la regla de que los datos deben coincidir con uno de los valores especificados en un objeto enumerado.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion                                                                                                      |
| --------- | ------ | --------- | ------- | ---------------------------------------------------------------------------------------------------------------- |
| data      | object | sí        |         | Objeto que define los valores permitidos para la validación. Los datos deben coincidir con uno de estos valores. |
| msg       | string | no        |         | Mensaje de error personalizado que se muestra si la validación falla.                                            |

### Returns

| Parametro | Tipo                   | Descripcion                                                                                                   |
| --------- | ---------------------- | ------------------------------------------------------------------------------------------------------------- |
| this      | FenextjsValidatorClass | Devuelve la instancia actual de la clase FenextjsValidatorClass, lo que permite el encadenamiento de métodos. |

### Usos

- Habilitar validación 'isEnum'

```tsx copy
const validator = FenextjsValidator();
enum enumValues {
  "VALUE_1" = "VALUE_1",
  "VALUE_2" = "VALUE_2",
}
validator.isEnum(enumValues, "El valor debe estar en el enum especificado");
```

## onValidate

Método para validar los datos proporcionados según las reglas establecidas. Ejecuta todas las reglas de validación habilitadas previamente para los datos.

### Parámetros

| Parámetro | Tipo | Requerido | Default | Descripcion                                                                                                     |
| --------- | ---- | --------- | ------- | --------------------------------------------------------------------------------------------------------------- |
| d         | T    | sí        |         | Datos que se deben validar, los cuales serán evaluados contra las reglas de validación previamente habilitadas. |

### Returns

| Parametro     | Tipo          | Descripcion                                                                                     |
| ------------- | ------------- | ----------------------------------------------------------------------------------------------- |
| true          | boolean       | Devuelve 'true' si los datos cumplen con todas las reglas de validación habilitadas.            |
| ErrorFenextjs | ErrorFenextjs | Si alguna regla de validación falla, retorna el error que indica qué regla de validación falló. |

### Usos

- Validación de datos con las reglas habilitadas

```tsx copy
const validator = FenextjsValidator();
const data = { name: "Juan", age: 30 };
const result = validator.onValidate(data);
if (result === true) {
  console.log("Datos válidos");
} else {
  console.log("Error de validación:", result);
}
```

## getObjectValidator

Método para obtener la validación 'isObject'. Devuelve el objeto con las reglas de validación definidas para las propiedades del objeto.

### Returns

| Parametro   | Tipo                                                        | Descripcion                                                                                                                   |
| ----------- | ----------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| objectValue | \{ [id in keyof T]?: FenextjsValidatorClass \} \| undefined | Devuelve el objeto con las reglas de validación para cada propiedad si 'isObject' está habilitado, o undefined si no lo está. |

### Usos

- Obtener las reglas de validación del objeto

```tsx copy
const validator = FenextjsValidator();
const objectValidator = validator.getObjectValidator();
console.log(objectValidator);
```

## getArrayValue

Método público para obtener el valor de validación de array. Devuelve las reglas de validación definidas para los elementos del array.

### Returns

| Parametro  | Tipo                                           | Descripcion                                                                              |
| ---------- | ---------------------------------------------- | ---------------------------------------------------------------------------------------- |
| arrayValue | FenextjsValidatorClassIsWhenProps \| undefined | Devuelve el valor de validación del array si está habilitada, o undefined si no lo está. |

### Usos

- Obtener el valor de validación de array

```tsx copy
const validator = FenextjsValidator();
const arrayValidator = validator.getArrayValue();
console.log(arrayValidator);
```

## getWhenValue

Método público para obtener el valor de validación de 'when'. Devuelve las condiciones definidas para la validación 'isWhen'.

### Returns

| Parametro      | Tipo                                             | Descripcion                                                                                                                           |
| -------------- | ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------- |
| this.whenValue | FenextjsValidatorClassIsWhenProps[] \| undefined | Devuelve el valor de 'when' como un array de objetos de tipo 'FenextjsValidatorClassIsWhenProps', o 'undefined' si no se ha definido. |

### Usos

- Obtener valor de validación 'when'

```tsx copy
const whenValue = validator.getWhenValue();
```
