# SwichViewSelect

El componente SwichViewSelect permite al usuario alternar entre diferentes vistas de selección mediante opciones visuales, representadas por íconos específicos para cada vista de selección.

### Importación

Para importar el componente SwichViewSelect, se puede hacer desde fenextjs

```tsx copy
import { SwichViewSelect } from "fenextjs";
```

### Parámetros

| Parámetro    | Tipo                                                                                                   | Requerido | Default                           | Descripcion                                            |
| ------------ | ------------------------------------------------------------------------------------------------------ | --------- | --------------------------------- | ------------------------------------------------------ |
| className    | string                                                                                                 | no        | ""                                | Clase CSS para el contenedor del componente.           |
| defaultValue | "fenext-swich-view-select-box" \| "fenext-swich-view-select-list" \| "fenext-swich-view-select-normal" | no        | "fenext-swich-view-select-normal" | Valor predeterminado de la vista de selección inicial. |
| onChange     | (e?: SwichViewSelectType) =\> void                                                                     | no        | undefined                         | Función que se ejecuta al seleccionar una nueva vista. |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/swichview-select--index)

### Usos

- Ejemplo básico

```tsx copy
<SwichViewSelect />
```

- Con valor predeterminado y función de cambio

```tsx copy
<SwichViewSelect
  defaultValue="fenext-swich-view-select-box"
  onChange={(e) => console.log("Vista seleccionada:", e)}
/>
```

- Aplicando una clase personalizada

```tsx copy
<SwichViewSelect className="custom-class" />
```
