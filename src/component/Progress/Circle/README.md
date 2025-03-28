# ProgressCircle

El componente ProgressCircle muestra un círculo de progreso visual que indica el avance de una tarea o porcentaje completado. Ofrece una opción para mostrar el porcentaje numérico en el centro del círculo.

### Importación

Para importar el componente ProgressCircle, se puede hacer desde fenextjs

```tsx copy
import { ProgressCircle } from "fenextjs";
```

### Parámetros

| Parámetro | Tipo    | Requerido | Default | Descripcion                                                                         |
| --------- | ------- | --------- | ------- | ----------------------------------------------------------------------------------- |
| className | string  | no        | ''      | Clase CSS para personalizar el contenedor del componente ProgressCircle.            |
| p         | number  | sí        | N/A     | Valor de progreso representado en el círculo, como un número entre 0 y 100.         |
| showP     | boolean | no        | true    | Indica si el valor numérico del progreso (`p`) se muestra en el centro del círculo. |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/progress-progresscircle--index)

### Usos

- ProgressCircle básico

```tsx copy
<ProgressCircle p={75} />
```

- ProgressCircle con progreso visible

```tsx copy
<ProgressCircle p={50} showP={true} />
```

- ProgressCircle con clase personalizada

```tsx copy
<ProgressCircle p={90} className="mi-clase" />
```
