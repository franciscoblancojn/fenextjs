# Button

El componente Button es un botón interactivo que puede ser configurado para mostrar íconos, estar en estado de carga (loader), deshabilitarse y adaptarse a diferentes tamaños. Permite a los usuarios interactuar con la aplicación ejecutando acciones al hacer clic.

### Importación

Para importar el componente Button, se puede hacer desde fenextjs

```tsx copy
import { Button } from "fenextjs";
```

### Parámetros

| Parámetro                     | Tipo                                                               | Requerido | Default   | Descripcion                                                                                                         |
| ----------------------------- | ------------------------------------------------------------------ | --------- | --------- | ------------------------------------------------------------------------------------------------------------------- |
| loader                        | boolean                                                            | no        | false     | Si el botón está en estado de carga, mostrando un indicador de carga (spinner) y deshabilitado para otras acciones. |
| invert                        | boolean                                                            | no        | false     | Si el botón invierte sus colores de background y hover.                                                             |
| disabled                      | boolean                                                            | no        | false     | Si el botón está deshabilitado, impidiendo cualquier interacción.                                                   |
| onClick                       | function                                                           | no        |           | Función que se ejecuta cuando se hace click en el botón (solo si no está deshabilitado o en estado de carga).       |
| onClickDisabled               | function                                                           | no        |           | Función que se ejecuta cuando se hace click en el botón estando deshabilitado.                                      |
| icon                          | ReactNode                                                          | no        | undefined | El ícono que se mostrará dentro del botón.                                                                          |
| iconLoader                    | ReactNode                                                          | no        | undefined | El ícono que se mostrará dentro del botón cuando esta en estado de carga.                                           |
| isBtn                         | boolean                                                            | no        | true      | Si se renderiza el componente como un botón (`\<button\>`) o como un `\<div\>`.                                     |
| size                          | "extra-small" \| "small" \| "normal" \| "strong" \| "extra-strong" | no        | "normal"  | El tamaño del botón.                                                                                                |
| full                          | boolean                                                            | no        | false     | Si el botón debe ocupar todo el ancho disponible.                                                                   |
| className                     | string                                                             | no        | ""        | Clase personalizada para el componente Button.                                                                      |
| classNameDisabled             | string                                                             | no        | ""        | Clase personalizada para el componente Button cuando esta deshabilitado.                                            |
| classNameLoader               | string                                                             | no        | ""        | Clase personalizada para el componente Button cuando esta en estado de carga.                                       |
| classNameContentLoaderElement | string                                                             | no        | ""        | Clase personalizada para contenedor del componente Loader dentro del botón cuando está en estado de carga.          |
| classNameLoaderElement        | string                                                             | no        | ""        | Clase personalizada para el componente Loader dentro del botón cuando está en estado de carga.                      |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/component-button--index)

### Usos

- Botón básico

```tsx copy
<Button>Click me</Button>
```

- Botón con ícono

```tsx copy
<Button icon={<img src="/icon.svg" alt="Icon" />}>Click me</Button>
```

- Botón en estado de carga

```tsx copy
<Button loader={true}>Loading...</Button>
```

- Botón deshabilitado

```tsx copy
<Button disabled={true}>Disabled</Button>
```

- Botón con tamaño personalizado

```tsx copy
<Button size="strong">Strong Button</Button>
```

- Botón con ancho completo

```tsx copy
<Button full={true}>Full Width Button</Button>
```
