# ScheduleWeekly

El componente ScheduleWeekly permite a los usuarios gestionar horarios semanales seleccionando intervalos de tiempo específicos para cada día de la semana. Utiliza ScheduleDay y CollapseMultiple para representar los horarios diarios en un formato de colapso.

### Importación

Para importar el componente ScheduleWeekly, se puede hacer desde fenextjs

```tsx copy
import { ScheduleWeekly } from "fenextjs";
```

### Parámetros

| Parámetro             | Tipo                                   | Requerido | Default                                                 | Descripcion                                                                                                   |
| --------------------- | -------------------------------------- | --------- | ------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| className             | string                                 | no        | ''                                                      | Clase CSS para personalizar el contenedor del componente ScheduleWeekly.                                      |
| title                 | ReactNode                              | no        | 'Schedule Weekly'                                       | Título del componente ScheduleWeekly.                                                                         |
| defaultValue          | ScheduleWeeklyValueType                | no        | \{\}                                                    | Valor inicial del horario semanal, estructurado por días de la semana.                                        |
| value                 | ScheduleWeeklyValueType                | no        | undefined                                               | Valor actual del horario semanal, usado para el control del componente desde el exterior.                     |
| onChange              | (v: ScheduleWeeklyValueType) =\> void  | no        | N/A                                                     | Función callback para manejar cambios en el valor del horario semanal.                                        |
| CollapseMultipleProps | Omit\<CollapseMultipleProps, 'items'\> | no        | \{ name: 'schedule', type: 'radio', defaultActive: 0 \} | Props para personalizar el comportamiento del componente CollapseMultiple que envuelve cada día de la semana. |
| onParseHeaderDay      | (v: DaysEnum) =\> ReactNode            | no        | undefined                                               | Función para personalizar el encabezado de cada día de la semana en el colapso.                               |

### Storybook

Para ver el storybook del componente lo puede hacer con este [link](https://fenextjs-component-storybook.vercel.app/?path=/story/schedule-scheduleweekly--index)

### Usos

- Uso básico del ScheduleWeekly

```tsx copy
<ScheduleWeekly onChange={(value) => console.log(value)} />
```

- ScheduleWeekly con título personalizado

```tsx copy
<ScheduleWeekly title="Horario Semanal" />
```

- ScheduleWeekly con CollapseMultipleProps personalizados

```tsx copy
<ScheduleWeekly
  CollapseMultipleProps={{ type: "checkbox", defaultActive: [0, 1] }}
/>
```
