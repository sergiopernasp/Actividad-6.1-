# Actividad-6.1

# Ejercicio1
```sh
#!bin/bash

# Pedir el número entero
numero = int(input("Introduce un número entero: "))

# Comprobar si es positivo
if numero > 0:
    print("El número es positivo")
else:
    print("El número no es positivo")
```

# Ejercicio2
```sh
#!bin/bash

# Pedir el número entero
numero = int(input("Introduce un número entero: "))

# Comprobar si es positivo
if numero < 0:
    print("El número es negativo")
else:
    print("El número no es positivo")
```

# Ejercicio3
```sh
#!bin/bash

# Recibir un número entero por teclado y decir si es igual a cero
read -p "Ingrese un número entero: " num

if [ $num -eq 0 ]; then
  echo "El número es igual a cero"
else
  echo "El número no es igual a cero"
fi
```

# Ejercicio4
```sh
#!/bin/bash

echo "Ingrese un numero entero:"
read num

if [ $num -eq 0 ]; then
    echo "El numero es cero"
elif [ $num -gt 0 ]; then
    echo "El numero es positivo"
else
    echo "El numero es negativo"
fi
```
# Ejercicio5
```sh
#!/bin/bash

if [ $# -ne 3 ]; then
  echo "Error: Incorrect number of parameters."
fi
```
# Ejercicio6
```sh
#!/bin/bash

if [ $# -ne 2 ]; then
    echo "Error: Se deben recibir dos números por parámetros"
    exit 1
fi

echo $(($1 + $2))
```


# Ejercicio7
```sh
#!/bin/bash

if [ $# -ne 3 ]; then 
  echo "Error. El script requiere 3 parámetros."
  exit
fi

num1=$1
num2=$2
oper=$3

if [ "$oper" != "+" ] && [ "$oper" != "-" ] && [ "$oper" != "x" ] && [ "$oper" != "/" ]; then
  echo "Operador no válido. Las opciones válidas son +, -, x y /."
  exit
fi

if [ "$oper" = "+" ]; then
  result=$(($num1 + $num2))
elif [ "$oper" = "-" ]; then
  result=$(($num1 - $num2))
elif [ "$oper" = "x" ]; then
  result=$(($num1 * $num2))
else
  result=$(($num1 / $num2))
fi

echo "El resultado de la operación es $result"
```

# Ejercicio8
```sh
#!/bin/bash
if [ -f $1 ]; then 
  echo "El fichero $1 existe"
else
  echo "El fichero $1 no existe"
fi
```

# Ejercicio9
```sh
#!/bin/bash

if [ -d "$1" ]; then
  echo "$1 es un directorio"
elif [ -f "$1" ]; then
  echo "$1 es un fichero"
else
  echo "$1 no es ni un directorio ni un fichero"
fi
```

# Ejercicio10
```sh
#!/bin/bash

`ls -l $1`
```
# Ejercicio11
```sh
#!/bin/bash

`for i in {1..50}; do echo "Hola"; done`
```

# Ejercicio12
```sh
#!/bin/bash

for i in {1..10}; do
    read -p "Ingrese una palabra: " palabra
    
    echo "La palabra ingresada es: $palabra"
done
```

# Ejercicio13
```sh
#!/bin/bash
if [ $# -eq 0 ]
then
  echo "No se ha indicado ningún parámetro"
else
  for (( i = 0 ; i < $1 ; i++ ))
    do
      echo "hola"
    done
fi
```
