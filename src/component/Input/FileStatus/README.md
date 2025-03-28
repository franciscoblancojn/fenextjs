# InputFileStatus

El componente InputFileStatus combina la funcionalidad de carga de archivos con un estado visual, mostrando diferentes iconos y mensajes según el estado del archivo (Aprobado, Rechazado, Pendiente).

### Importación

Para importar el componente InputFileStatus, se puede hacer desde fenextjs

```tsx copy
import { InputFileStatus } from "fenextjs";
```

### Parámetros

| Parámetro       | Tipo                                       | Requerido | Default                                     | Descripcion                                                                              |
| --------------- | ------------------------------------------ | --------- | ------------------------------------------- | ---------------------------------------------------------------------------------------- |
| title           | ReactNode                                  | no        | 'Drag and drop here'                        | Título del componente que se muestra cuando no hay archivos cargados.                    |
| text            | ReactNode                                  | no        | 'Drag and drop your file or template here.' | Texto que se muestra para guiar al usuario sobre la acción que debe realizar.            |
| icon            | ReactNode                                  | no        | \<Upload2 /\>                               | Ícono que se muestra en el componente.                                                   |
| btn             | ReactNode                                  | no        | 'Choose File'                               | Texto o contenido del botón de carga.                                                    |
| iconLoader      | ReactNode                                  | no        | \<LoaderSpinner /\>                         | Ícono que se muestra mientras se está cargando el archivo.                               |
| className       | string                                     | no        | ''                                          | Clase CSS para el componente.                                                            |
| onUploadFile    | (data: FileProps) =\> Promise\<FileProps\> | sí        | undefined                                   | Función que se ejecuta para manejar la carga del archivo.                                |
| contentByStatus | InputFileStatusContentByStatus             | no        | \{\}                                        | Contenido específico para cada estado del archivo, que incluye título, ícono y etiqueta. |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/input-inputfilestatus--index)

### Usos

- Carga de archivo con estado de éxito

```tsx copy
<InputFileStatus
  onUploadFile={async (file) => {
    /* Lógica de carga */
    return file;
  }}
/>
```

- Carga de archivo con gestión de errores

```tsx copy
<InputFileStatus
  onUploadFile={async (file) => {
    throw new Error("Error de carga");
  }}
/>
```

- Componente de carga con botón personalizado

```tsx copy
<InputFileStatus
  btn={<Button>Subir Archivo</Button>}
  onUploadFile={async (file) => {
    /* Lógica de carga */
    return file;
  }}
/>
```
