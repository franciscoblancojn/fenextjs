# Chat

El componente Chat es un contenedor completo que incluye elementos como el usuario del chat, los mensajes, un formulario para enviar mensajes y un botón de cargar más mensajes. Se puede configurar para mostrar un loader mientras se cargan los datos, así como manejar diferentes estados como chat vacío y auto-scroll cuando hay nuevos mensajes.

### Importación

Para importar el componente Chat, se puede hacer desde fenextjs

```tsx copy
import { Chat } from "fenextjs";
```

### Parámetros

| Parámetro                 | Tipo                             | Requerido | Default                                                  | Descripcion                                                                                     |
| ------------------------- | -------------------------------- | --------- | -------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| loader                    | boolean                          | no        | false                                                    | Si el chat está en estado de carga, deshabilitando otras acciones mientras se cargan los datos. |
| useAccountOwner           | boolean                          | no        | false                                                    | Si se debe mostrar al dueño de la cuenta en el chat.                                            |
| onScrollIfNewMessage      | boolean                          | no        | true                                                     | Si se debe hacer scroll automáticamente cuando hay un nuevo mensaje.                            |
| onActionAfterNewMessage   | () =\> void                      | no        |                                                          | Función que se ejecuta después de recibir un nuevo mensaje.                                     |
| empty                     | ReactNode                        | no        | \<Text\>There is not messages yet\</Text\>\<Telegram /\> | Contenido que se mostrará si no hay mensajes en el chat.                                        |
| customBack                | ReactNode                        | no        | undefined                                                | Componente Back personalizado ejectuar la accion de atras.                                      |
| chatUser                  | ChatUserProps \| ChatUserProps[] | sí        |                                                          | Información del usuario o usuarios del chat.                                                    |
| loaderChatUser            | boolean                          | no        | false                                                    | Si el usuario del chat está en estado de carga.                                                 |
| chatMessage               | ChatMessageProps[]               | sí        |                                                          | Lista de mensajes del chat.                                                                     |
| loaderChatMessage         | boolean                          | no        | false                                                    | Si los mensajes del chat están en estado de carga.                                              |
| chatFormSendMessage       | ChatFormSendMessageProps         | sí        |                                                          | Propiedades del formulario para enviar un mensaje en el chat.                                   |
| loaderChatFormSendMessage | boolean                          | no        | false                                                    | Si el formulario de enviar mensaje está en estado de carga.                                     |
| useBtnLoadMoreMssages     | boolean                          | no        | false                                                    | Si se debe mostrar el botón para cargar más mensajes.                                           |
| btnLoadMoreMessages       | ButtonProps                      | no        | \{ children: "Load more messages" \}                     | Propiedades para el botón de cargar más mensajes.                                               |
| fullPage                  | boolean                          | no        | true                                                     | Si el chat debe mostrarse en modo de página completa.                                           |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/chat-chat--index)

### Usos

- Chat básico con mensajes

```tsx copy
<Chat
  chatUser={[{ id: 1, name: "User1" }]}
  chatMessage={[
    { id: 1, message: "Hello!" },
    { id: 2, message: "How are you?" },
  ]}
  chatFormSendMessage={{ onSubmit: (msg) => console.log(msg) }}
/>
```

- Chat vacío

```tsx copy
<Chat
  chatUser={[{ id: 1, name: "User1" }]}
  chatMessage={[]}
  chatFormSendMessage={{ onSubmit: () => {} }}
/>
```

- Chat con botón de cargar más mensajes

```tsx copy
<Chat
  chatUser={[{ id: 1, name: "User1" }]}
  chatMessage={[
    { id: 1, message: "Hello!" },
    { id: 2, message: "How are you?" },
  ]}
  chatFormSendMessage={{ onSubmit: (msg) => console.log(msg) }}
  useBtnLoadMoreMssages={true}
/>
```
