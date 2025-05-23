# PrintPage

El componente PrintPage permite renderizar contenido listo para impresión y proporciona un hook `usePrintData` para gestionar la carga y obtención de datos necesarios para la impresión.

### Importación

Para importar el componente PrintPage, se puede hacer desde fenextjs

```tsx copy
import { PrintPage } from "fenextjs";
```

### Parámetros

| Parámetro   | Tipo                                               | Requerido | Default   | Descripcion                                                                                                                               |
| ----------- | -------------------------------------------------- | --------- | --------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| className   | string                                             | no        | ''        | Clase CSS para personalizar el contenedor del componente PrintPage.                                                                       |
| onComponent | (data: PrintPageComponentProps\<T\>) =\> ReactNode | sí        | N/A       | Función que retorna el contenido a renderizar dentro del componente de impresión, aceptando datos de tipo `PrintPageComponentProps\<T\>`. |
| data        | T \| undefined                                     | no        | undefined | Datos utilizados dentro del componente para la impresión, gestionados a través del hook `usePrintData`.                                   |
| load        | boolean                                            | no        | false     | Indica si el componente está en estado de carga, mostrando un indicador de carga si es `true`.                                            |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/print-page--index)

### Usos

- PrintPage básico

```tsx copy
<PrintPage
  onComponent={({ data, load }) => (
    <div>
      {load
        ? "Cargando..."
        : data
          ? "Contenido listo para imprimir"
          : "Sin datos"}
    </div>
  )}
/>
```

- PrintPage con clase personalizada

```tsx copy
<PrintPage
  className="mi-clase"
  onComponent={({ data, load }) => (
    <div>
      {load ? "Cargando..." : data ? "Datos cargados" : "Sin datos disponibles"}
    </div>
  )}
/>
```
