
# CMD

## EJERCICIO 1

```cmd
copy con ARCH1.txt
md d2
cd d2
md d21
cd ..
md d3
cd ..
md d1
cd d1
md d11
cd d11
copy con ARCH2.txt

md ..\..\d2\d21\d211
md ..\..\d2\d22
copy con ..\..\d2\d22\ARCH3.txt
copy con ..\..\d2\d21\d211\ARCH6.txt
copy con ..\..\d3\ARCH8.txt

copy con ..\..\d2\d22\ARCH5.txt
md ..\..\d4
copy con ..\..\d4\ARCH9.txt
md ..\d12

cd /
cd d3
copy ..\d2\d22\ARCH3.txt ..\d1\d12\
copy ARCH8.txt ..\d1\d12\
ren ..\d1\d12\ARCH8.txt ARCH4.txt

md ..\..\d3\d31
```

## EJERCICIO 2

```cmd
ren H:\d1\d12\*.* *.DAT

```

## EJERCICIO 3

a.- `H:\D1\D12> type ..\arch3.txt`

    Daría un error ya que primero haría que la ruta activa pasara a ser d1 y luego buscaría en este el archivo arch3.txt y este no se encuentra ahí, sino en d12.

    El comando correcto sería:
    ```cmd
    type arch3.txt
    ```

b.- `H:\D1> rd d12`

    No ejecutaría la acción ya que el directorio no está vacío. Para poder ejecutarlo habría que añadir el argumento `/s`.

c.- `H:\D1> copy ..\d2\d22\arch3.txt h:\d3\fich3.dat`

    Es correcto y copiaría el arch3.txt en d3 a la vez que le cambiaría el nombre y la extensión.

d.- `H:\D2\D21> copy arch5.txt \d4`

    Sería incorrecto ya que intentaría acceder a un directorio llamado d4 en la carpeta actual, la cual no tiene ese directorio. Si se refiere al d4 correcto entonces tendría que ser `..\..\d4`.

e.- `H:\D2\D21> copy arch5.txt d4`

    Haría una copia del arch5 y lo llamaría d4.

## EJERCICIO 4

a. 
```cmd
dir \d1\d12\ /T:C /O:D
```

b. 
```cmd
dir \d1\d12\ /T:C /O:-D
```

c.
```cmd
dir ARCH3.* /s /b
```

## EJERCICIO 5

Se usa para concatenar el contenido de dos o más archivos. Por ejemplo, si tenemos en `ARCH3.dat` una frase que dice "Hola Mundo" y en otro archivo llamado `ARCH4.dat` tenemos escrito "Bienvenidos a Este Mundo", el comando:

```cmd
copy ARCH3.dat + ARCH4.dat .
```

nos copiará el archivo ARCH3.dat y su resultado será:

```
Hola mundo
Bienvenidos a Este Mundo
```

Para concatenar archivos de `d12` en uno solo:

Ruta absoluta:
```cmd
copy H:\d1\d12\ARCH3.txt + H:\d1\d12\ARCH4.txt H:\d4
```

Ruta relativa:
```cmd
copy ..\d1\d12\ARCH3.txt + ..\d1\d12\ARCH4.txt .
```

## EJERCICIO 6

a. 
```cmd
copy H:\d4\ARCH9.txt H:\d2\d21\d211\
```

b. 
```cmd
copy ..\d4\ARCH9.txt d21\d211\
```

c.
```cmd
copy ARCH9.TXT ..\d2\d21\d211
```

d.
```cmd
copy ..\..\d4\ARCH9.txt ..\d21\d211
```

e.
```cmd
copy ..\..\..\d4\ARCH9.txt .
```

f.
```cmd
copy d4\ARCH9.txt d2\d21\d211
```

## EJERCICIO 7

Suponiendo que nos encontremos en H: todo el rato:

1.
```cmd
copy ARCH1.txt d0
```

2.
```cmd
copy d1\d11\ARCH2.txt d0\d1\d11
```

3.
```cmd
copy d1\d12\ARCH4.txt d0\d1\d12
```

4.
```cmd
copy d1\d12\ARCH3.txt d0\d1\d12
```

5.
```cmd
copy d2\d21\d211\ARCH6.txt d0\d2\d21\d211
```

6.
```cmd
copy d2\d22\ARCH3.txt d0\d2\d22
```

7.
```cmd
copy d3\ARCH8.txt d0\d3
```

8.
```cmd
copy d4\ARCH9.txt d0\d4
```

## EJERCICIO 8

a.
```cmd
cd d0\d2
cd d22
del ARCH3.txt
cd ..
del d22

cd 21
del ARCH5.txt
cd d211
del ARCH6.txt
cd ..
rd d211
cd ..
rd 21

cd ..
rd d2
```

b. Desde d0
```cmd
del d2\d22\ARCH3.txt
rd d2\d22

del d2\d21\ARCH5.txt
del d2\d21\d211\ARCH6.txt
rd d2\d21\d211
rd d2\d21
rd d2
```

c. Desde d0/d3/d31
```cmd
del ..\..\d2\d22\ARCH3.txt
rd ..\..\d2\d22

del ..\..\d2\d21\ARCH5.txt
del ..\..\d2\d21\d211\ARCH6.txt
rd ..\..\d2\d21\d211
rd ..\..\d2\d21
rd ..\..\d2
```

## EJERICIO 9

a. 
```cmd
dir c???.dat
```

b. 
```cmd
dir ?o*.txt
```

c. Buscar archivos que tengan los últimos caracteres "at" y que delante de esto haya un carácter que puede ser cualquiera, y delante de este también puede haber un número cualquiera de caracteres.

d. Buscará un archivo que tenga la segunda y tercera letra "a" y "s" respectivamente, y además que solo pueda haber un carácter delante de estas y otro después, además de un punto seguido de tres caracteres más.

## EJERICIO 10 

El 7 se puede hacer muy facil con el xcopy y las opciones de /s /e 

```cmd
xcopy ARCH1.txt d0

md d0\d1

md d0\d2

md d0\d3

md d0\d4

xcopy d1 d0 /s /e 

xcopy d2 d0 /s /e 

xcopy d3 d0 /s /e

xcopy d4 d0 /s /e 
```