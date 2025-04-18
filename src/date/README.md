# FenextjsDate

Clase para manipular fechas, proporcionando métodos para sumar unidades de tiempo, formatear, validar y comparar fechas.

### Importación

Para importar el componente FenextjsDate, se puede hacer desde fenextjs

```tsx copy
import { FenextjsDate } from "fenextjs";
```

## setOnCallback

Establece el callback que se ejecutará al modificar la fecha.

### Parámetros

| Parámetro | Tipo                  | Requerido | Default | Descripcion                  |
| --------- | --------------------- | --------- | ------- | ---------------------------- |
| callback  | (date: Date) =\> void | sí        |         | Función callback a ejecutar. |

### Usos

- Establecer un callback para actualización de fecha

```tsx copy
const fenextDate = new FenextjsDate();
fenextDate.setOnCallback((date) => console.log("Fecha actualizada:", date));
```

## addTime

Agrega una cantidad de tiempo en milisegundos a la fecha actual.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion                          |
| --------- | ------ | --------- | ------- | ------------------------------------ |
| time      | number | sí        |         | Tiempo en milisegundos para agregar. |

### Usos

- Agregar milisegundos a la fecha actual

```tsx copy
const fenextDate = new FenextjsDate(new Date());
fenextDate.addTime(60000); // Agrega 1 minuto en milisegundos
```

## addMilliseconds

Agrega una cantidad específica de milisegundos a la fecha.

### Parámetros

| Parámetro    | Tipo   | Requerido | Default | Descripcion                           |
| ------------ | ------ | --------- | ------- | ------------------------------------- |
| milliseconds | number | sí        |         | Milisegundos para agregar a la fecha. |

### Usos

- Agregar milisegundos específicos

```tsx copy
const fenextDate = new FenextjsDate(new Date());
fenextDate.addMilliseconds(500); // Agrega 500 milisegundos
```

## addSeconds

Agrega una cantidad de segundos a la fecha actual.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion            |
| --------- | ------ | --------- | ------- | ---------------------- |
| seconds   | number | sí        |         | Segundos para agregar. |

### Usos

- Agregar segundos a la fecha actual

```tsx copy
const fenextDate = new FenextjsDate(new Date());
fenextDate.addSeconds(10); // Agrega 10 segundos
```

## addMinutes

Agrega una cantidad de minutos a la fecha actual.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion           |
| --------- | ------ | --------- | ------- | --------------------- |
| minutes   | number | sí        |         | Minutos para agregar. |

### Usos

- Agregar minutos a la fecha actual

```tsx copy
const fenextDate = new FenextjsDate(new Date());
fenextDate.addMinutes(30); // Agrega 30 minutos
```

## addHours

Agrega una cantidad de horas a la fecha actual.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion         |
| --------- | ------ | --------- | ------- | ------------------- |
| hours     | number | sí        |         | Horas para agregar. |

### Usos

- Agregar horas a la fecha actual

```tsx copy
const fenextDate = new FenextjsDate(new Date());
fenextDate.addHours(5); // Agrega 5 horas
```

## addDate

Agrega una cantidad de días a la fecha actual.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion        |
| --------- | ------ | --------- | ------- | ------------------ |
| date      | number | sí        |         | Días para agregar. |

### Usos

- Agregar días a la fecha actual

```tsx copy
const fenextDate = new FenextjsDate(new Date());
fenextDate.addDate(10); // Agrega 10 días
```

## addMonth

Agrega una cantidad de meses a la fecha actual.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion         |
| --------- | ------ | --------- | ------- | ------------------- |
| month     | number | sí        |         | Meses para agregar. |

### Usos

- Agregar meses a la fecha actual

```tsx copy
const fenextDate = new FenextjsDate(new Date());
fenextDate.addMonth(3); // Agrega 3 meses
```

## addYear

Agrega una cantidad de años a la fecha actual.

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion        |
| --------- | ------ | --------- | ------- | ------------------ |
| year      | number | sí        |         | Años para agregar. |

### Usos

- Agregar años a la fecha actual

```tsx copy
const fenextDate = new FenextjsDate(new Date());
fenextDate.addYear(2); // Agrega 2 años
```

## onFormat

Devuelve la fecha formateada según las opciones dadas.

### Parámetros

| Parámetro | Tipo                      | Requerido | Default | Descripcion                                                     |
| --------- | ------------------------- | --------- | ------- | --------------------------------------------------------------- |
| options   | FenextjsDateFormatOptions | sí        |         | Opciones de formato para la fecha.                              |
| date      | FenextjsDateValue         | no        |         | Fecha para formatear; usa la fecha actual si no se proporciona. |

### Usos

- Formatear la fecha actual

```tsx copy
const fenextDate = new FenextjsDate(new Date());
const formattedDate = fenextDate.onFormat({
  year: "numeric",
  month: "2-digit",
  day: "2-digit",
});
console.log("Fecha formateada:", formattedDate);
```

## onFormatId

Devuelve la fecha formateada usando un formato identificado por un ID.

### Parámetros

| Parámetro | Tipo              | Requerido | Default | Descripcion                                                  |
| --------- | ----------------- | --------- | ------- | ------------------------------------------------------------ |
| id        | string            | sí        |         | ID del formato a usar.                                       |
| date      | FenextjsDateValue | no        |         | Fecha a formatear; usa la fecha actual si no se proporciona. |

### Usos

- Formatear la fecha con un formato identificado

```tsx copy
const fenextDate = new FenextjsDate({
  formats: { short: { year: "numeric", month: "2-digit", day: "2-digit" } },
});
const formattedDate = fenextDate.onFormatId("short");
console.log("Fecha formateada con ID:", formattedDate);
```

## getDateByMonth

Devuelve un arreglo de fechas para un mes y año específicos.

### Importación

Para importar el componente getDateByMonth, se puede hacer desde fenextjs

```tsx copy
import { getDateByMonth } from "fenextjs";
```

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion                                                          |
| --------- | ------ | --------- | ------- | -------------------------------------------------------------------- |
| month     | number | sí        |         | Número del mes (1 para enero, 12 para diciembre).                    |
| year      | number | no        |         | Año para obtener las fechas; usa el año actual si no se proporciona. |

### Usos

- Obtener las fechas de un mes específico

```tsx copy
const fenextDate = new FenextjsDate(new Date());
const dates = fenextDate.getDateByMonth(2); // Obtiene las fechas de febrero del año actual
console.log("Fechas de febrero:", dates);
```

## setDateByMonth

Establece la fecha a un mes y año específicos.

### Importación

Para importar el componente setDateByMonth, se puede hacer desde fenextjs

```tsx copy
import { setDateByMonth } from "fenextjs";
```

### Parámetros

| Parámetro | Tipo   | Requerido | Default | Descripcion                                                           |
| --------- | ------ | --------- | ------- | --------------------------------------------------------------------- |
| month     | number | sí        |         | Número del mes (1 para enero, 12 para diciembre).                     |
| year      | number | no        |         | Año para establecer la fecha; usa el año actual si no se proporciona. |

### Usos

- Establecer la fecha a un mes y año específicos

```tsx copy
const fenextDate = new FenextjsDate(new Date());
fenextDate.setDateByMonth(6, 2023); // Establece la fecha a junio de 2023
console.log("Fecha establecida:", fenextDate);
```

## onGenerateDateByMonth

Genera una lista de fechas para un mes específico.

### Parámetros

| Parámetro | Tipo              | Requerido | Default | Descripcion                                |
| --------- | ----------------- | --------- | ------- | ------------------------------------------ |
| date      | FenextjsDateValue | no        |         | Fecha de referencia para el mes a generar. |

### Usos

- Generar fechas para el mes actual

```tsx copy
const fenextDate = new FenextjsDate(new Date());
const dates = fenextDate.onGenerateDateByMonth();
console.log("Fechas del mes:", dates);
```

## getDateByCalendar

Devuelve un arreglo de fechas que representa un calendario completo del mes actual, con días de la semana.

### Importación

Para importar el componente getDateByCalendar, se puede hacer desde fenextjs

```tsx copy
import { getDateByCalendar } from "fenextjs";
```

### Usos

- Obtener las fechas de un calendario completo para el mes actual

```tsx copy
const fenextDate = new FenextjsDate(new Date());
const calendarDates = fenextDate.getDateByCalendar(); // Obtiene las fechas del calendario completo del mes actual
console.log("Fechas del calendario:", calendarDates);
```

## setDateByCalendar

Establece las fechas del calendario con un arreglo de fechas.

### Importación

Para importar el componente setDateByCalendar, se puede hacer desde fenextjs

```tsx copy
import { setDateByCalendar } from "fenextjs";
```

### Parámetros

| Parámetro     | Tipo   | Requerido | Default | Descripcion                                                                     |
| ------------- | ------ | --------- | ------- | ------------------------------------------------------------------------------- |
| calendarDates | Date[] | sí        |         | Un arreglo de objetos `Date` que representa las fechas del calendario completo. |

### Usos

- Establecer un calendario con un arreglo de fechas

```tsx copy
const fenextDate = new FenextjsDate(new Date());
const calendarDates = [new Date(2023, 5, 1), new Date(2023, 5, 2)]; // Un ejemplo de fechas del calendario
fenextDate.setDateByCalendar(calendarDates); // Establece las fechas del calendario
console.log("Fechas del calendario establecidas:", fenextDate);
```

## onGenerateDateByCalendar

Genera una lista de fechas para el mes y año específicos, con una vista tipo calendario.

### Parámetros

| Parámetro | Tipo              | Requerido | Default | Descripcion                                     |
| --------- | ----------------- | --------- | ------- | ----------------------------------------------- |
| date      | FenextjsDateValue | no        |         | Fecha de referencia para generar el calendario. |

### Usos

- Generar fechas para el calendario de un mes

```tsx copy
const fenextDate = new FenextjsDate(new Date());
const calendarDates = fenextDate.onGenerateDateByCalendar();
console.log("Fechas del calendario:", calendarDates);
```

## onValidateMinMax

Valida si la fecha proporcionada está dentro del rango especificado por las fechas mínima y máxima.

### Parámetros

| Parámetro | Tipo | Requerido | Default | Descripcion                                                                                                  |
| --------- | ---- | --------- | ------- | ------------------------------------------------------------------------------------------------------------ |
| min       | Date | no        |         | Fecha mínima que la fecha proporcionada debe cumplir. Si no se proporciona, no se valida el límite inferior. |
| max       | Date | no        |         | Fecha máxima que la fecha proporcionada debe cumplir. Si no se proporciona, no se valida el límite superior. |
| date      | Date | no        |         | Fecha que se va a validar. Si no se proporciona, se usa la fecha actual de la instancia.                     |

### Usos

- Validar si una fecha está dentro de un rango específico

```tsx copy
const fenextDate = new FenextjsDate(new Date());
const isValid = fenextDate.onValidateMinMax({
  min: new Date(2023, 0, 1),
  max: new Date(2023, 11, 31),
}); // Retorna true si la fecha está dentro del rango, false en caso contrario
console.log(isValid);
```

## onCompareDate

Compara la fecha actual con otra fecha proporcionada, utilizando los criterios de comparación especificados.

### Parámetros

| Parámetro   | Tipo                                            | Requerido | Default | Descripcion                                                                                                           |
| ----------- | ----------------------------------------------- | --------- | ------- | --------------------------------------------------------------------------------------------------------------------- |
| dateCompare | Date                                            | sí        |         | La fecha con la que se va a comparar la fecha actual.                                                                 |
| compare     | \{ [id in FenextjsDateCompareType]?: boolean \} | sí        |         | Un objeto que contiene los criterios de comparación. Puede incluir propiedades como 'FullYear', 'Month', 'Date', etc. |

### Usos

- Comparar dos fechas con diferentes criterios

```tsx copy
const fenextDate = new FenextjsDate(new Date());
const compareResult = fenextDate.onCompareDate({
  dateCompare: new Date(2023, 0, 1),
  compare: { FullYear: true, Month: true, Date: true },
}); // Compara el año, mes y día de las dos fechas
console.log(compareResult);
```

## onGetDifDate

Obtiene la difereciona entre 2 fechas, si no se proporciona date se usa el valor actual de la clase.

### Parámetros

| Parámetro   | Tipo | Requerido | Default | Descripcion                                                                 |
| ----------- | ---- | --------- | ------- | --------------------------------------------------------------------------- |
| dateCompare | Date | sí        |         | La fecha con la que se va obtener la diferencia con date o la fecha actual. |
| date        | Date | sí        |         | La fecha con la que se va obtener la diferencia con dateCompare.            |

### Usos

- Obtiene la difereciona entre 2 fechas

```tsx copy
const fenextDate = new FenextjsDate(new Date());
const difResult = fenextDate.onGetDifDate({
  dateCompare: new Date(2023, 1, 1),
  date: new Date(2024, 1, 1),
});
console.log(difResult);
```
