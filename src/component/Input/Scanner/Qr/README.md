# InputScannerQr

El componente InputScannerQr permite escanear códigos QR utilizando la cámara del dispositivo. Incluye opciones para cambiar de cámara, activar el flash y detener el escaneo.

### Importación

Para importar el componente InputScannerQr, se puede hacer desde fenextjs

```tsx copy
import { InputScannerQr } from "fenextjs";
```

### Parámetros

| Parámetro                 | Tipo                 | Requerido | Default            | Descripcion                                                                            |
| ------------------------- | -------------------- | --------- | ------------------ | -------------------------------------------------------------------------------------- |
| className                 | string               | no        | ''                 | Clase CSS para personalizar el contenedor principal del componente.                    |
| onChange                  | (v: string) =\> void | no        | undefined          | Función que se ejecuta al escanear un código QR con éxito, pasando el valor escaneado. |
| buttonScannerContent      | ReactNode            | no        | \<Qr /\>           | Contenido personalizado para el botón que activa el escáner.                           |
| buttonChangeCameraContent | ReactNode            | no        | \<CameraChange /\> | Contenido personalizado para el botón que permite cambiar entre cámaras.               |
| buttonToggleFlashContent  | ReactNode            | no        | \<Bolt /\>         | Contenido personalizado para el botón que activa o desactiva el flash de la cámara.    |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/input-scanner-inputscannerqr--index)

### Usos

- Escáner básico de QR

```tsx copy
<InputScannerQr onChange={(value) => console.log(value)} />
```

- Escáner con contenido personalizado en los botones

```tsx copy
<InputScannerQr buttonScannerContent={<div>Escanear QR</div>} />
```

- Escáner con cambio de cámara y flash activable

```tsx copy
<InputScannerQr
  buttonChangeCameraContent={<div>Cambiar Cámara</div>}
  buttonToggleFlashContent={<div>Flash</div>}
/>
```
