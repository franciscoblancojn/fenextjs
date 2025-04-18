# Share

El componente Share permite a los usuarios compartir contenido a través de diversas plataformas como WhatsApp, Facebook, Twitter, correo electrónico o copiar el enlace. Incluye personalización de botones y títulos.

### Importación

Para importar el componente Share, se puede hacer desde fenextjs

```tsx copy
import { Share } from "fenextjs";
```

### Parámetros

| Parámetro     | Tipo            | Requerido | Default                                        | Descripcion                                                                                  |
| ------------- | --------------- | --------- | ---------------------------------------------- | -------------------------------------------------------------------------------------------- |
| className     | string          | no        | ''                                             | Clase CSS para personalizar el contenedor del componente Share.                              |
| ButtonProps   | ButtonProps     | no        | \{ children: 'Share' \}                        | Props del componente Button para personalizar el botón de compartir.                         |
| TitleProps    | TitleProps      | no        | \{ children: 'Share', tag: 'h2' \}             | Props del componente Title para personalizar el título de la ventana de compartir.           |
| share         | string          | no        | ''                                             | Texto que se comparte en las redes sociales o se copia en el portapapeles.                   |
| shareList     | ShareListType[] | no        | ['whatsapp', 'facebook', 'x', 'email', 'copy'] | Lista de plataformas de redes sociales o acciones de compartir disponibles en el componente. |
| showShareCopy | boolean         | no        | false                                          | Indica si se debe mostrar el botón de copia para compartir el texto.                         |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/share-share--index)

### Usos

- Uso básico del Share

```tsx copy
<Share share="http://example.com" />
```

- Share con título personalizado

```tsx copy
<Share TitleProps={{ children: "Compartir en redes" }} />
```

- Share con opciones específicas de redes sociales

```tsx copy
<Share shareList={["whatsapp", "twitter"]} />
```

- Share con botón de copia de enlace visible

```tsx copy
<Share showShareCopy={true} />
```
