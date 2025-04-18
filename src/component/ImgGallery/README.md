# ImgGallery

El componente ImgGallery muestra una galería de imágenes con la opción de cargar más imágenes y visualizar cada imagen en un modal con un deslizador.

### Importación

Para importar el componente ImgGallery, se puede hacer desde fenextjs

```tsx copy
import { ImgGallery } from "fenextjs";
```

### Parámetros

| Parámetro           | Tipo                           | Requerido | Default                              | Descripcion                                                                                      |
| ------------------- | ------------------------------ | --------- | ------------------------------------ | ------------------------------------------------------------------------------------------------ |
| imgs                | ImgProps[]                     | sí        |                                      | Lista de imágenes a mostrar en la galería.                                                       |
| buttonShowMoreImg   | Omit\<ButtonProps, 'onClick'\> | no        | \{ children: 'Show more pictures' \} | Propiedades del botón para mostrar más imágenes.                                                 |
| buttonHiddenMoreImg | Omit\<ButtonProps, 'onClick'\> | no        | \{ children: 'Hidden pictures' \}    | Propiedades del botón para ocultar imágenes adicionales.                                         |
| loader              | boolean                        | no        | false                                | Indica si el componente está en estado de carga, mostrando un cargador en lugar de las imágenes. |
| nLoader             | number                         | no        | 5                                    | Número de elementos que mostrarán el loader mientras se cargan las imágenes.                     |
| className           | string                         | no        | ''                                   | Clase CSS para personalizar el contenedor de la galería.                                         |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/img-imggallery--index)

### Usos

- Galería básica

```tsx copy
<ImgGallery imgs={imageList} />
```

- Galería con botón personalizado

```tsx copy
<ImgGallery
  imgs={imageList}
  buttonShowMoreImg={{ children: "Ver más imágenes" }}
/>
```

- Galería en estado de carga

```tsx copy
<ImgGallery loader={true} nLoader={3} />
```
