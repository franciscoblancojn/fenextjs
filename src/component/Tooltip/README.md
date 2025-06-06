# Tooltip

El componente Tooltip muestra información adicional en un cuadro emergente cuando el usuario se desplaza sobre un elemento o interactúa con él. La posición del tooltip puede ajustarse en los ejes X e Y.

### Importación

Para importar el componente Tooltip, se puede hacer desde fenextjs

```tsx copy
import { Tooltip } from "fenextjs";
```

### Parámetros

| Parámetro | Tipo                          | Requerido | Default   | Descripcion                                                            |
| --------- | ----------------------------- | --------- | --------- | ---------------------------------------------------------------------- |
| className | string                        | no        | ''        | Clase CSS para personalizar el contenedor del tooltip.                 |
| children  | ReactNode                     | no        | undefined | Contenido o elemento que activará la visualización del tooltip.        |
| tooltip   | ReactNode                     | no        | undefined | Contenido del tooltip que se mostrará al usuario.                      |
| positionX | 'center' \| 'right' \| 'left' | no        | 'center'  | Posición horizontal del tooltip en relación con el elemento activador. |
| positionY | 'center' \| 'top' \| 'bottom' | no        | 'top'     | Posición vertical del tooltip en relación con el elemento activador.   |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/tooltip-tooltip--index)

### Usos

- Tooltip básico

```tsx copy
<Tooltip tooltip="Texto de ayuda">Hover aquí</Tooltip>
```

- Tooltip con posición ajustada

```tsx copy
<Tooltip tooltip="Texto de ayuda" positionX="right" positionY="bottom">
  Hover aquí
</Tooltip>
```

- Tooltip con clase personalizada

```tsx copy
<Tooltip tooltip="Texto de ayuda" className="custom-tooltip">
  Hover aquí
</Tooltip>
```
