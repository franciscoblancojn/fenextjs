# InputImg

El componente InputImg permite a los usuarios cargar una única imagen y muestra una vista previa de la imagen seleccionada. También incluye la opción de eliminar la imagen cargada.

### Importación

Para importar el componente InputImg, se puede hacer desde fenextjs

```tsx copy
import { InputImg } from "fenextjs";
```

### Parámetros

| Parámetro            | Tipo                           | Requerido | Default                         | Descripcion                                                  |
| -------------------- | ------------------------------ | --------- | ------------------------------- | ------------------------------------------------------------ |
| title                | ReactNode                      | no        | 'Add Image'                     | Título que se muestra en el componente.                      |
| text                 | ReactNode                      | no        | 'Drag Image'                    | Texto que se muestra en el componente para guiar al usuario. |
| icon                 | ReactNode                      | no        | \<SvgImg /\>                    | Ícono que se muestra en el componente.                       |
| onRemove             | () =\> void                    | no        | undefined                       | Función que se ejecuta cuando se elimina la imagen.          |
| className            | string                         | no        | ''                              | Clase CSS para el componente.                                |
| classNameContentIcon | string                         | no        | ''                              | Clase CSS para el contenedor del ícono.                      |
| classNameText        | Omit\<TextProps, 'children'\>  | no        | \{\}                            | Clase CSS para el texto.                                     |
| classNameTitle       | Omit\<TitleProps, 'children'\> | no        | \{\}                            | Clase CSS para el título.                                    |
| classNameProgress    | string                         | no        | ''                              | Clase CSS para la barra de progreso.                         |
| classNameRemove      | string                         | no        | ''                              | Clase CSS para el botón de eliminar.                         |
| classNameImg         | string                         | no        | ''                              | Clase CSS para la imagen mostrada.                           |
| defaultValue         | FileProps                      | no        | \{ fileData: '', text: '' \}    | Valor por defecto que se mostrará en el componente.          |
| parseProgress        | (e: number) =\> string         | no        | Imging . . . $\{e.toFixed(0)\}% | Función que formatea el texto de progreso durante la carga.  |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/input-inputimg--index)

### Usos

- Carga de una imagen simple

```tsx copy
<InputImg
  onChange={(data) => {
    console.log(data);
  }}
/>
```

- Carga de una imagen con título y texto personalizado

```tsx copy
<InputImg
  title="Sube tu Imagen"
  text="Arrastra la imagen aquí"
  onChange={(data) => {
    console.log(data);
  }}
/>
```

- Carga de imagen con función de eliminación

```tsx copy
<InputImg
  onRemove={() => {
    console.log("Imagen eliminada");
  }}
  onChange={(data) => {
    console.log(data);
  }}
/>
```
