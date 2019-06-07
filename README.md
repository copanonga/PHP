# Snippets para PHP

## Índice de contenidos

- [Crear objeto](#crear-objeto)
- [Explode](#Explode)

## Crear objeto

```

$objetoCreado = new stdClass();
$objetoCreado->id = $valor->id;
$objetoCreado->nombre = $valor->nombre;

```

## Explode

```
Datos de entrada en cadena de texto: 12|23|34|

$datos = substr($datos, 0, -1);
$datosObtenidos = explode("|", $datos);

Array obtenido: 12,23,34

```
