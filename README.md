# Snippets para PHP

## Índice de contenidos

- [Crear objeto](#crear-objeto)
- [Explode](#Explode)
- [Quitar tildes a una cadena](#quitar-tildes-a-una-cadena)
- [Eliminar etiquetas HTML de un string](#eliminar-etiquetas-html-de-un-string)
- [Buscar texto](#buscar-texto)

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

## Quitar tildes a una cadena

```
private function quitar_tildes($cadena) {
        
        $no_permitidas= array ("á","é","í","ó","ú","Á","É","Í","Ó","Ú","ñ","À","Ã","Ì","Ò","Ù","Ã™","Ã ","Ã¨","Ã¬","Ã²","Ã¹","ç","Ç","Ã¢","ê","Ã®","Ã´","Ã»","Ã‚","ÃŠ","ÃŽ","Ã”","Ã›","ü","Ã¶","Ã–","Ã¯","Ã¤","«","Ò","Ã","Ã„","Ã‹");
        $permitidas= array ("a","e","i","o","u","A","E","I","O","U","n","N","A","E","I","O","U","a","e","i","o","u","c","C","a","e","i","o","u","A","E","I","O","U","u","o","O","i","a","e","U","I","A","E");
        $texto = str_replace($no_permitidas, $permitidas ,$cadena);
        
        return $texto;
        
    }

$nuevaCadena = quitar_tildes($cadena);
```

## Eliminar etiquetas HTML de un string

```
$cadena="<p>El veloz <b>murciélago</b></p>";
echo stript_tags($cadena);
```

## Buscar texto

```
$textoABuscar = 'veloz';
$cadena = "El veloz murciélago hindú";
$estaContenido = strpos($cadena, $textoABuscar);

if ($estaContenido !== false) {
   echo "La cadena contiene el texto a buscar";
}
```

