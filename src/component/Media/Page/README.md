# MediaPage

El componente MediaPage proporciona una interfaz para subir, mostrar y seleccionar imágenes, con funcionalidades adicionales como eliminación, aceptación y un header personalizable. Permite manejar tanto una imagen única como múltiples imágenes.

### Importación

Para importar el componente MediaPage, se puede hacer desde fenextjs

```tsx copy
import { MediaPage } from "fenextjs";
```

### Parámetros

| Parámetro   | Tipo                                                         | Requerido | Default   | Descripcion                                                                         |
| ----------- | ------------------------------------------------------------ | --------- | --------- | ----------------------------------------------------------------------------------- |
| className   | string                                                       | no        | ''        | Clase CSS para personalizar el contenedor del componente MediaPage.                 |
| multiple    | boolean                                                      | no        | false     | Determina si se pueden seleccionar o subir múltiples imágenes a la vez.             |
| onChange    | (data: ImgDataProps[] \| ImgDataProps \| undefined) =\> void | no        | undefined | Función que se ejecuta cuando hay cambios en las imágenes seleccionadas o cargadas. |
| onUploadImg | (data: ImgDataProps) =\> void                                | no        | undefined | Función que se ejecuta cuando se sube una imagen.                                   |
| onDeleteImg | (data: ImgDataProps) =\> void                                | no        | undefined | Función que se ejecuta cuando se elimina una imagen.                                |
| onAcepte    | (data: ImgDataProps[] \| ImgDataProps) =\> void              | no        | undefined | Función que se ejecuta cuando se acepta la selección de imágenes.                   |
| HeaderPage  | ReactNode                                                    | no        |

\<Title tag="h3"\>Media\</Title\>
\<Text\>Upload or Select Imagen.\</Text\> | Contenido del encabezado de la página de medios, se puede personalizar. |
| defaultValue | ImgDataProps[] \| ImgDataProps | no | undefined | Valor por defecto del componente, que puede ser una o varias imágenes. |
| images | ImgDataProps[] | no | [] | Imágenes a mostrar en el componente MediaPage. |
| loaderImages | boolean | no | false | Muestra un cargador mientras las imágenes están siendo cargadas. |
| disabledSelectImg | boolean | no | false | Deshabilita la opción de seleccionar imágenes. |
| InputUploadProps | Omit\<InputUploadProps, 'onChange' \| 'defaultValue' \| 'onChangeProgress' \| 'onUploadFile' \| 'clearAfterUpload'\> | no | \{
accept: ["png", "jpg", "jpeg", "webp"],
title: "Upload Imagen",
text: "Click for select or upload Imagen.",
\} | Propiedades para personalizar el componente InputUpload utilizado dentro de MediaPage. |
| ButtonAcceptProps | Omit\<ButtonProps, 'onClick'\> | no | \{ children: 'Acepte' \} | Propiedades del botón de aceptación. |
| ButtonCancelProps | Omit\<ButtonProps, 'onClick'\> | no | \{ children: 'Cancel' \} | Propiedades del botón de cancelación. |
| isPage | boolean | no | true | Determina si el componente se comporta como una página completa de medios o como un componente en línea. |
| extraContentImgs | ReactNode | no | undefined | Contenido adicional que se puede agregar junto a las imágenes en MediaPage. |
| onRenderImg | (data: ImgDataProps) =\> ReactNode | no | undefined | Función que permite renderizar imágenes personalizadas dentro de la galería. |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/media-page--index)

### Usos

- MediaPage básico

```tsx copy
<MediaPage />
```

- MediaPage con imágenes predeterminadas

```tsx copy
<MediaPage defaultValue={defaultImages} />
```

- MediaPage con múltiples imágenes

```tsx copy
<MediaPage multiple={true} />
```
