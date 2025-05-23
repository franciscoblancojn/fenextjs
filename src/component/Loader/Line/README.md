# LoaderLine

El componente LoaderLine se utiliza para mostrar un indicador de carga en forma de línea. Se puede personalizar tanto su altura como su estilo utilizando una clase CSS específica.

### Importación

Para importar el componente LoaderLine, se puede hacer desde fenextjs

```tsx copy
import { LoaderLine } from "fenextjs";
```

### Parámetros

| Parámetro           | Tipo   | Requerido | Default | Descripcion                                                               |
| ------------------- | ------ | --------- | ------- | ------------------------------------------------------------------------- |
| classNameLoaderLine | string | no        | ''      | Clase CSS para personalizar el estilo de la línea del indicador de carga. |
| height              | number | no        | 20      | Altura de la línea del indicador de carga, en píxeles.                    |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/loader-line--index)

### Usos

- LoaderLine básico

```tsx copy
<LoaderLine />
```

- LoaderLine con altura personalizada

```tsx copy
<LoaderLine height={30} />
```

- LoaderLine con clase personalizada

```tsx copy
<LoaderLine classNameLoaderLine="custom-loader-line" />
```
