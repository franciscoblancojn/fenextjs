# ContentLoading

El componente ContentLoading es una envoltura que muestra un contenido cargando o el contenido completo, dependiendo de si el estado de carga está activado o no. Es útil para manejar la visualización condicional de contenido mientras se espera una carga.

### Importación

Para importar el componente ContentLoading, se puede hacer desde fenextjs

```tsx copy
import { ContentLoading } from "fenextjs";
```

### Parámetros

| Parámetro       | Tipo      | Requerido | Default             | Descripcion                                                                      |
| --------------- | --------- | --------- | ------------------- | -------------------------------------------------------------------------------- |
| children        | ReactNode | no        | undefined           | El contenido que se mostrará cuando no esté en estado de carga.                  |
| componentLoader | ReactNode | no        | \<LoaderSpinner /\> | Componente que se muestra mientras el contenido está en estado de carga.         |
| loader          | boolean   | no        | false               | Indica si el componente está en estado de carga, mostrando el componente loader. |
| isPage          | boolean   | no        | false               | Determina si el componente debe comportarse como una página en carga.            |
| className       | string    | no        | ''                  | Clase CSS para personalizar el contenedor del componente.                        |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/contentloading-contentloading--index)

### Usos

- Básico

```tsx copy
<ContentLoading>
  <div>Contenido cargado</div>
</ContentLoading>
```

- ContentLoading con loader activado

```tsx copy
<ContentLoading loader={true}>
  <div>Contenido cargado</div>
</ContentLoading>
```

- ContentLoading como página

```tsx copy
<ContentLoading isPage={true}>
  <div>Contenido cargado</div>
</ContentLoading>
```
