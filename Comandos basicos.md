# Ejercicio 1
Para empezar creamos la unidad H

Creamos una carpeta donde queramos y le damos un nombre cualquiera

```cmd
md  ejercicios 
```

```powershell
New-Item 'ejercicios' -ItemType Directory
```

Despues generamos la unidad con 

```cmd
subst H: ejercicios
```

Ahora con el siguiente comando accedermos a la unidad H

```cmd
H:
```

Creamos d1 y nos movemos a la carpeta


```cmd
md d1
cd d1
```

```powershell
New-Item 'd1' -ItemType Directory
Set-Location 'd1'
```


```cmd
copy con fitx1.txt

md d11

cd d11

copy con fitx1.txt
copy con fitx2.txt
copy con fitx3.txt

cd /

md d2
```

```powershell
New-Item 'fitx1.txt' -ItemType File

New-Item 'd11' -ItemType Directory

Set-Location 'd11' 

New-Item 'fitx1.txt' -ItemType File
New-Item 'fitx2.txt' -ItemType File
New-Item 'fitx3.txt' -ItemType File

```

# EJERCICIO 2
```cmd
cd /

md d2

cd d2

copy con ..\d1\d11\doc1.txt

copy con ..\d1\doc1.txt

copy con ..\doc1.txt

md d21

md d22

md \d2\d222

copy con \d22\d222\doc2.txt
```

```powershell

Set-Location / 

New-Item 'd2' -ItemType Directory

Set-Location d2

Out-File -FilePath '..\d1\d11\doc1.txt'
Out-File -FilePath '..\d1\doc1.txt'
Out-File -FilePath '..\doc1.txt'

New-Item 'd21' -ItemType Directory 
New-Item 'd22' -ItemType Directory
New-Item '\d2\d222' -ItemType Directory

New-Item ' \d22\d222\doc2.txt' -ItemType File
```


# EJERCICIO 3 
```cmd
copy \d1\*.*

ren *.txt *.d1

copy \d1\d11\*.*

ren *.txt *.d11
```
```powershell

Set-Location H:\
New-Item -itemType Directory d3
Set-Location d3
Copy-Item ..\d1\*.* *.d1
Copy-Item ..\d1\d11\*.* *.d11
```

# EJERCICIO 4 

Cambian la ruta activa

```cmd
del \d1\*.*

del \d1\d11\*.*

rmdir \d1\d11
```
Sin cambiar la ruta activa

```cmd

cd d1

del *.*

cd d11

del *.*

cd ..\d1

rmdir d11
```




