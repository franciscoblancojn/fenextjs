# InputGallery

El componente InputGallery permite a los usuarios cargar y gestionar múltiples imágenes a través de una interfaz de galería. Incluye opciones para añadir y eliminar imágenes.

### Importación

Para importar el componente InputGallery, se puede hacer desde fenextjs

```tsx copy
import { InputGallery } from "fenextjs";
```

### Parámetros

| Parámetro              | Tipo                          | Requerido | Default           | Descripcion                                                                              |
| ---------------------- | ----------------------------- | --------- | ----------------- | ---------------------------------------------------------------------------------------- |
| defaultValue           | FileProps[]                   | no        | []                | Valor por defecto que se muestra en la galería. Se espera un array de objetos FileProps. |
| value                  | FileProps[]                   | no        | undefined         | Valor controlado para la galería, que reemplaza el defaultValue si se proporciona.       |
| textBtn                | string                        | no        | 'Add More Images' | Texto que se muestra en el botón para añadir más imágenes.                               |
| className              | string                        | no        | ''                | Clase CSS para el componente.                                                            |
| classNameContentButton | string                        | no        | ''                | Clase CSS para el contenedor del botón.                                                  |
| classNameButton        | ButtonClassProps              | no        | \{\}              | Clase CSS específica para el botón.                                                      |
| onChange               | (items: FileProps[]) =\> void | no        | undefined         | Función que se ejecuta cuando la lista de imágenes cambia.                               |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/input-inputgallery--index)

### Usos

- Galería de imágenes básica

```tsx copy
<InputGallery
  onChange={(items) => {
    console.log(items);
  }}
/>
```

- Galería de imágenes con valores predefinidos

```tsx copy
<InputGallery
  defaultValue={[{ fileData: "url1", text: "Image 1" }]}
  onChange={(items) => {
    console.log(items);
  }}
/>
```

- Galería con botón personalizado

```tsx copy
<InputGallery
  textBtn="Upload New Image"
  onChange={(items) => {
    console.log(items);
  }}
/>
```
