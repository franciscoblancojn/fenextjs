# InputSelectNumber

El componente `InputSelectNumber` permite la selección de un valor numérico de una lista de números dentro de un rango definido. Ofrece funcionalidades adicionales como la personalización del texto a mostrar para cada número.

### Importación

Para importar el componente InputSelectNumber, se puede hacer desde fenextjs

```tsx copy
import { InputSelectNumber } from "fenextjs";
```

### Parámetros

| Parámetro    | Tipo                   | Requerido | Default | Descripcion                                                                                                          |
| ------------ | ---------------------- | --------- | ------- | -------------------------------------------------------------------------------------------------------------------- |
| onChange     | (n?: number) =\> void  | no        |         | Función que se ejecuta cuando el valor seleccionado cambia.                                                          |
| defaultValue | number                 | no        |         | Valor numérico por defecto seleccionado.                                                                             |
| min          | number                 | no        |         | El valor mínimo permitido en el rango de selección.                                                                  |
| max          | number                 | no        |         | El valor máximo permitido en el rango de selección.                                                                  |
| parseText    | (e: number) =\> string | no        |         | Función utilizada para convertir el número seleccionado en una cadena de texto personalizada a mostrar en el select. |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/input-inputselectnumber--index)

### Usos

- Uso básico de InputSelectNumber

```tsx copy
<InputSelectNumber
  min={1}
  max={10}
  defaultValue={5}
  onChange={(n) => console.log("Valor seleccionado:", n)}
/>
```

- InputSelectNumber con formato personalizado

```tsx copy
<InputSelectNumber
  min={1}
  max={20}
  parseText={(n) => `Número: ${n}`}
  onChange={(n) => console.log("Número seleccionado:", n)}
/>
```
