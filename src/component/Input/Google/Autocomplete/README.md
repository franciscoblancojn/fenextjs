# InputGoogleAutocomplete

El componente InputGoogleAutocomplete permite la entrada de direcciones utilizando la funcionalidad de autocompletado de Google, con validaciones y manejo de errores.

### Importación

Para importar el componente InputGoogleAutocomplete, se puede hacer desde fenextjs

```tsx copy
import { InputGoogleAutocomplete } from "fenextjs";
```

### Parámetros

| Parámetro              | Tipo                                           | Requerido | Default                | Descripcion                                                                |
| ---------------------- | ---------------------------------------------- | --------- | ---------------------- | -------------------------------------------------------------------------- |
| defaultValueJsonString | string                                         | no        | undefined              | Valor predeterminado en formato JSON string para la dirección.             |
| valueJsonString        | string                                         | no        | undefined              | Valor actual en formato JSON string para la dirección.                     |
| onChangeJsonString     | (value: string) =\> void                       | no        | undefined              | Función que se ejecuta cuando el valor en formato JSON string cambia.      |
| defaultValue           | AddressGoogle \| undefined                     | no        | undefined              | El valor predeterminado del input.                                         |
| value                  | AddressGoogle \| undefined                     | no        | undefined              | El valor actual del input.                                                 |
| onChange               | (value: AddressGoogle \| undefined) =\> void   | no        | undefined              | Función que se ejecuta cuando cambia el valor de la dirección.             |
| parseJson_to_String    | (value: AddressGoogle \| undefined) =\> string | no        | parseAddress_to_String | Función que convierte el objeto de dirección a string.                     |
| parseString_to_Json    | (value: string) =\> AddressGoogle \| undefined | no        | parseString_to_Address | Función que convierte un string a un objeto de dirección.                  |
| className              | string                                         | no        | ''                     | Clase CSS para personalizar el contenedor del input.                       |
| validator              | FenextjsValidatorClass\<AddressGoogle\>        | no        | undefined              | Instancia de FenextjsValidator para validaciones personalizadas del input. |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/input-google-autocomplete--index)

### Usos

- InputGoogleAutocomplete básico

```tsx copy
<InputGoogleAutocomplete />
```

- InputGoogleAutocomplete con validación

```tsx copy
<InputGoogleAutocomplete validator={customValidator} />
```

- InputGoogleAutocomplete con valor predeterminado

```tsx copy
<InputGoogleAutocomplete defaultValueJsonString='{"formatted_address": "1600 Amphitheatre Parkway, Mountain View, CA"}' />
```

- InputGoogleAutocomplete con función personalizada

```tsx copy
<InputGoogleAutocomplete onChangeJsonString={(value) => console.log(value)} />
```
