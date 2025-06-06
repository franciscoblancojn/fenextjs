# User

El componente User muestra información de un usuario, incluyendo su imagen, nombre, y correo electrónico. También incluye una opción de cargador para mostrar un indicador de carga cuando la información del usuario no está disponible.

### Importación

Para importar el componente User, se puede hacer desde fenextjs

```tsx copy
import { User } from "fenextjs";
```

### Parámetros

| Parámetro        | Tipo                 | Requerido | Default   | Descripcion                                                                                   |
| ---------------- | -------------------- | --------- | --------- | --------------------------------------------------------------------------------------------- |
| user             | Partial\<UserProps\> | no        | undefined | Objeto con la información del usuario, como nombre, imagen, y correo electrónico.             |
| loader           | boolean              | no        | false     | Indica si se debe mostrar el cargador en lugar de la información del usuario.                 |
| className        | string               | no        | ''        | Clase CSS para personalizar el contenedor principal del componente.                           |
| classNamePicture | string               | no        | ''        | Clase CSS para personalizar el contenedor de la imagen del usuario.                           |
| classNameImg     | string               | no        | ''        | Clase CSS para la imagen del usuario.                                                         |
| classNameName    | string               | no        | ''        | Clase CSS para el nombre del usuario.                                                         |
| classNameLetter  | string               | no        | ''        | Clase CSS para la inicial del nombre del usuario cuando no se tiene imagen.                   |
| classNameEmail   | string               | no        | ''        | Clase CSS para el correo electrónico del usuario.                                             |
| classNameLoader  | LoaderUserClassProps | no        | \{\}      | Clase CSS para el componente de cargador cuando se muestra en lugar de los datos del usuario. |

### UserProps

Fenextjs posee su interface estandar para:

| Propiedad  | Tipo            | Descripción                    |
| ---------- | --------------- | ------------------------------ |
| status     | UserStatusProps | Estatus del usuario.           |
| id         | string          | Id del usuario.                |
| token      | string          | token del usuario.             |
| name       | string          | Nombre del usuario.            |
| img        | ImgDataProps    | Avatar del usuario.            |
| role       | UserRoleProps   | Rol del usuario.               |
| phone      | PhoneProps      | Telefono del usuario.          |
| email      | string          | Correo del usuario.            |
| dateCreate | Date            | Fecha de creacion del usuario. |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/user-user--index)

### Usos

- User básico

```tsx copy
<User
  user={{
    name: "John Doe",
    email: "john@example.com",
  }}
/>
```

- User con imagen de perfil

```tsx copy
<User
  user={{
    name: "Jane Doe",
    email: "jane@example.com",
    image: "/path/to/image.jpg",
  }}
/>
```

- User con cargador

```tsx copy
<User loader={true} />
```

- User con clases personalizadas

```tsx copy
<User
  user={{ name: "John Doe" }}
  className="custom-container"
  classNameName="custom-name"
/>
```
