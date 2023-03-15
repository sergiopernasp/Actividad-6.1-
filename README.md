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

# Ejercicio7
```sh
#!/bin/bash
if [ -f $1 ]; then 
  echo "El fichero $1 existe"
else
  echo "El fichero $1 no existe"
fi
```
