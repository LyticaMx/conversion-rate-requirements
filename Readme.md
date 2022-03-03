# Requerimientos para mostrar tasa de conversión.

Vico es un sistema de detección de tráfico para retail.

Para mostrar la tasa de conversión por tienda, es decir la cantidad ventas comparada con el tráfico en la tienda se necesitan los siguientes datos:

## Datos requeridos

### 1. CSV de tiendas:

Archivo CSV que contiene los nombres de las tiendas y sus identificadores.

*Se envía una única vez.*

```csv
store,store_id
CDMX Aeropuerto,MX-46756
Guadalajara Central,MX-49210
Monterrey Aeropuerto,MX-38685
Oaxaca Galerías,MX-69593
```

| columna | descripción |
| --- | --- |
| store | Dirección de la tienda (para poder registrarla en nuestro sistema)  |
| store_id | Identificador único para cada tienda (no debe contener espacios) |

[Ejemplo CSV de tiendas](../blob/main/stores.csv)

### 2. CSV de transacciones: Archivo CSV que contiene las transacciones de las tiendas.

*Se envía frecuentemente cada que se desean visualizar datos de conversión*

```csv
store_id,ticket_number,timestamp,ammount
MX-38685,527688681-4,2022-02-19T20:37:30Z,2730.06
MX-49210,475347897-1,2022-01-07T13:03:44Z,999.24
MX-26793,660342013-9,2022-01-02T07:34:18Z,2004.71
MX-49210,688738924-X,2022-02-02T10:06:49Z,1852.54
```

[Ejemplo CSV de transacciones](../blob/main/transactions.csv)

| columna | descripción |
| --- | --- |
| store_id | Identificador único para cada tienda (no debe contener espacios) |
| ticket_number | Número de ticket, debe ser único por cada venta |
| timestamp | Fecha y hora de la venta en formato ISO |
| ammount | Monto de la venta, puede ser decimal |

