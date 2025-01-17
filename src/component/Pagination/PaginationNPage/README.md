# PaginationNPage

Componente de selección de elementos por página para la paginación, permitiendo seleccionar el número de elementos a mostrar en cada página.

### Importación

Para importar el componente PaginationNPage, se puede hacer desde fenextjs

```tsx copy
import { PaginationNPage } from "fenextjs";
```

### Parámetros

| Parámetro     | Tipo                                              | Requerido | Default                                                                                                                                          | Descripcion                                                                                   |
| ------------- | ------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------- |
| className     | string                                            | no        | ''                                                                                                                                               | Clase CSS para el contenedor principal del componente de paginación.                          |
| defaultValue  | string \| number                                  | no        |                                                                                                                                                  | Valor por defecto de la opción seleccionada en el menú desplegable.                           |
| listNpage     | Array\<\{ id: string \| number; text: string \}\> | no        | [\{ id: "10", text: "10" \}, \{ id: "20", text: "20" \}, \{ id: "50", text: "50" \}, \{ id: "100", text: "100" \}, \{ id: "all", text: "All" \}] | Lista de opciones para el número de elementos por página que se puede seleccionar.            |
| onChangeNPage | (value: string \| number) =\> void                | no        |                                                                                                                                                  | Función de callback que se llama cuando cambia la opción seleccionada en el menú desplegable. |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/pagination-paginationnpage--index)

### Usos

- Componente de selección de número de elementos por página con valor por defecto de 20

```tsx copy
<PaginationNPage defaultValue="20" />
```

- Componente de selección de número de elementos por página con clases personalizadas

```tsx copy
<PaginationNPage className="custom-pagination-class" />
```

- Componente con callback en cambio de selección

```tsx copy
<PaginationNPage
  onChangeNPage={(value) => console.log("Elementos por página:", value)}
/>
```
