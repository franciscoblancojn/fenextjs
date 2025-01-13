# Notification

El componente Notification permite mostrar mensajes de notificación personalizados, con distintos tipos de resultados y estilos para cada tipo.

### Importación

Para importar el componente Notification, se puede hacer desde fenextjs

```tsx copy
import { Notification } from "fenextjs";
```

### Parámetros

| Parámetro | Tipo                                                          | Requerido | Default                       | Descripcion                                                            |
| --------- | ------------------------------------------------------------- | --------- | ----------------------------- | ---------------------------------------------------------------------- |
| className | string                                                        | no        | ''                            | Clase CSS para el contenedor del componente.                           |
| type      | RequestResultTypeProps \| keyof typeof RequestResultTypeProps | no        | RequestResultTypeProps.NORMAL | Tipo de notificación, que define el estilo y el propósito del mensaje. |
| children  | ReactNode                                                     | no        | undefined                     | Contenido o mensaje que se mostrará dentro de la notificación.         |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/notification-notification--index)

### Usos

- Notificación básica

```tsx copy
<Notification>Mensaje de notificación</Notification>
```

- Notificación de éxito

```tsx copy
<Notification type="SUCCESS">Operación éxitosa</Notification>
```

- Notificación de error

```tsx copy
<Notification type="ERROR">Error en la operación</Notification>
```