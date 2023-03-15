# SSIII
EJERICICIO1
```bash
#!/bin/bash

echo "Ingrese un número entero: "
read num

if ((num > 0))
then
    echo "El número es positivo."
else
    echo "El número no es positivo."
fi
```
EJERCICIO2
```Bash
#!/bin/bash

echo "Introduce un número entero:"
read num

if [ $num -lt 0 ]
then
  echo "El número $num es negativo"
else
  echo "El número $num no es negativo"
fi

```
EJERCICIO3
```Bash
#!/bin/bash

echo "Introduce un número entero:"
read num

if [ $num -eq 0 ]
then
  echo "El número es igual a cero."
else
  echo "El número no es igual a cero."
fi

```
EJERCICIO4
```Bash
#!/bin/bash

echo "Introduce un número entero:"
read num

if [ $num -gt 0 ]
then
  echo "El número es positivo."
elif [ $num -lt 0 ]
then
  echo "El número es negativo."
else
  echo "El número es igual a cero."
fi

```
EJERCICIO5
```Bash
#!/bin/bash

if [ $# -ne 3 ]; then
  echo "Error: Este script necesita exactamente 3 parámetros."
  exit 1
fi
```
EJERCICIO6
```Bash
#!/bin/bash

if [ $# -ne 2 ]; then
  echo "Error: Este script necesita exactamente 2 parámetros."
  exit 1
fi

num1=$1
num2=$2

suma=$((num1 + num2))

echo "La suma de $num1 y $num2 es: $suma"

```
EJERCICIO7
```Bash
#!/bin/bash

if [ $# -ne 3 ]; then
  echo "Error: Este script necesita exactamente 3 parámetros."
  exit 1
fi

if ! [[ "$1" =~ ^[0-9]+$ ]]; then
  echo "Error: El primer parámetro no es un número."
  exit 1
fi

if ! [[ "$2" =~ ^[0-9]+$ ]]; then
  echo "Error: El segundo parámetro no es un número."
  exit 1
fi

case "$3" in
  "+")
    resultado=$(($1 + $2))
    ;;
  "-")
    resultado=$(($1 - $2))
    ;;
  "x")
    resultado=$(($1 * $2))
    ;;
  "/")
    resultado=$(($1 / $2))
    ;;
  *)
    echo "Error: El tercer parámetro debe ser '+', '-', 'x' o '/'."
    exit 1
esac

echo "El resultado de la operación es: $resultado"

```
EJERCICIO8
```Bash
#!/bin/bash

if [ $# -ne 1 ]; then
  echo "Error: Este script necesita exactamente 1 parámetro."
  exit 1
fi

if [ -e "$1" ]; then
  echo "El fichero $1 existe."
else
  echo "El fichero $1 no existe."
fi

```
EJERCICIO9
```Bash
#!/bin/bash

if [ $# -ne 1 ]; then
  echo "Error: Este script necesita exactamente 1 parámetro."
  exit 1
fi

if [ -d "$1" ]; then
  echo "El fichero $1 es un directorio."
elif [ -f "$1" ]; then
  echo "El fichero $1 es un archivo regular."
else
  echo "El fichero $1 no existe o no es un directorio ni un archivo regular."
fi

```
EJERCICIO10
```Bash
#!/bin/bash

if [ $# -ne 1 ]; then
  echo "Error: Este script necesita exactamente 1 parámetro."
  exit 1
fi

if [ ! -e "$1" ]; then
  echo "El fichero $1 no existe."
  exit 1
fi

permisos=$(stat -c '%A' "$1")

echo "El fichero $1 tiene los siguientes permisos:"
echo " - Lectura: $(echo $permisos | cut -c 2)"
echo " - Escritura: $(echo $permisos | cut -c 3)"
echo " - Ejecución: $(echo $permisos | cut -c 4)"

```
EJERCICI011
```Bash
#!/bin/bash
for i in {1..50}
do
    echo "hola"
done

```
