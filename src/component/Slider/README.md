# Slider

El componente Slider permite crear un carrusel de elementos con opciones de personalización de cantidad de ítems visibles, tiempo de animación y bucle automático. Incluye controles de navegación y estilos personalizados.

### Importación

Para importar el componente Slider, se puede hacer desde fenextjs

```tsx copy
import { Slider } from "fenextjs";
```

### Parámetros

| Parámetro          | Tipo        | Requerido | Default | Descripcion                                                                          |
| ------------------ | ----------- | --------- | ------- | ------------------------------------------------------------------------------------ |
| className          | string      | no        | ''      | Clase CSS para personalizar el contenedor principal del componente Slider.           |
| classNameContent   | string      | no        | ''      | Clase CSS para personalizar el contenedor de contenido del slider.                   |
| classNameItem      | string      | no        | ''      | Clase CSS para personalizar cada ítem dentro del slider.                             |
| classNameDogs      | string      | no        | ''      | Clase CSS para personalizar el contenedor de elementos de slider.                    |
| classNameDog       | string      | no        | ''      | Clase CSS para personalizar un elemento individual dentro del contenedor de slider.  |
| classNameArrows    | string      | no        | ''      | Clase CSS para personalizar las flechas de navegación del slider.                    |
| classNameArrowPre  | string      | no        | ''      | Clase CSS para personalizar la flecha de navegación anterior.                        |
| classNameArrowNext | string      | no        | ''      | Clase CSS para personalizar la flecha de navegación siguiente.                       |
| items              | ReactNode[] | no        | []      | Arreglo de elementos que se mostrarán dentro del slider.                             |
| nItemsDesktop      | number      | no        | 3       | Número de elementos visibles en pantallas de escritorio.                             |
| nItemsTable        | number      | no        | 2       | Número de elementos visibles en pantallas de tabletas.                               |
| nItemsPhone        | number      | no        | 1       | Número de elementos visibles en pantallas de teléfonos.                              |
| timeDelay          | number      | no        | 4000    | Tiempo de espera en milisegundos antes de avanzar automáticamente al siguiente ítem. |
| timeAnimation      | number      | no        | 500     | Duración de la animación en milisegundos para mover el slider.                       |
| loop               | boolean     | no        | true    | Determina si el slider se reproduce en bucle o se detiene al final.                  |
| separationItems    | number      | no        | 16      | Espacio de separación en píxeles entre cada ítem del slider.                         |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/slider-slider--index)

### Usos

- Uso básico del Slider

```tsx copy
<Slider items={[<Item1 />, <Item2 />, <Item3 />]} />
```

- Slider con 4 ítems en escritorio y 2 en tablet

```tsx copy
<Slider nItemsDesktop={4} nItemsTable={2} />
```

- Slider con animación de 1 segundo y sin bucle

```tsx copy
<Slider timeAnimation={1000} loop={false} />
```

- Slider con espacio de separación de 32px entre ítems

```tsx copy
<Slider separationItems={32} />
```
