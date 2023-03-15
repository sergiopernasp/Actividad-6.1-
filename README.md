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

# Ejercicio14
```sh
#!/bin/bash

n=$1

for i in $(seq 0 $n);
do
    echo $i
done
```

# Ejercicio15
```sh
#!/bin/bash

if [[ $# -ne 1 ]]
then
	echo "Debe de introducir un número por parámetro"
	exit
fi

#Comenzamos la suma desde 1
total=1

#Bucle para sumar hasta el número introducido
for((i=2; i<=$1; i++))
do
  total=$((total + i))
done
  
echo "El resultado de la suma es $total"
```

# Ejercicio16
```sh
#!/bin/bash

var1=$1
var2=$2

temp=$var1
var1=$var2
var2=$temp

echo "El valor del primer parámetro es: $var1"
echo "El valor del segundo parámetro es: $var2"
```

# Ejercicio17
```sh
#!/bin/bash

echo "Escribe una palabra (q para salir):"
read palabra

while [ "$palabra" != "q" ]
do
    echo "Escrito: $palabra"
    echo "Escribe otra palabra (q para salir):"
    read palabra
done
echo "Adios!"
```

# Ejercicio18
```sh
#!/bin/bash

while True:
palabra = input("Introduce una palabra: ")
if palabra == "q":
    break
else:
    with open("fichero.txt", "a") as fichero:
        fichero.write(palabra + "\n")
```

# Ejercicio19
```sh
#!/bin/bash

# Script para leer palabras y guardarlas en un fichero de forma ordenada

echo "Introduce palabras (para salir escribe q):"

# Bucle infinito
while true; do
    read palabra
    if [ "$palabra" = "q" ]; then
        break
    else
        # Añadimos la palabra al final del fichero, ordenada alfabeticamente
        echo "$palabra" >> fichero.txt
        sort -o fichero.txt fichero.txt
    fi
done

echo "Fin del programa."
```

# Ejercicio20
```sh
#!/bin/bash

# Solicitar al usuario un número
echo "Por favor, introduce un número: "
read num

# Comprueba si el número está en el archivo números.txt
if grep -q $num números.txt; then
  echo "El número $num se encuentra en el archivo números.txt"
else
  echo "El número $num no se encuentra en el archivo números.txt"
fi
```
