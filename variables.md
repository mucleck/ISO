# Ejercicio 1 

a. ```dir %tmp% /o:d```

b.```dir *.exe %systemroot%```

c.```cd %systemroot%```

# Ejercicio 2 

a. H:\> md d1 
   ¿? > md d1\d11 
   ¿? > set destino=H:\d1\d11 
   ¿? > copy %systemroot%\system32\notepad.exe destino

   Esta secuencia crearia la carpeta d1 y dentro de esta d11, despues crearia la variable destino que tendria esa ruta y luego ejecutaria el comando copy el cual antes necesita saber que la variable systemroot es igual a una direccion, luego como a destino le faltan los porcentajes lo unico que hara sera cambiarle el nombre de notepad.exe a destino. 

b. H:\> md d1 
   ¿? > md d1\d11 
   ¿? > set destino=H:\d1\d11 
   ¿? > copy %systemroot%\system32\notepad.exe %destino% 

   Este comando es identico pero copiaria notepad.exe en la ruta establecida a la variable destino

c. H:\> md d1 
   ¿? > md d1\d11 
   ¿? > set letra=H: 
   ¿? > set destino=\d1\d11 
   ¿? > cd destino 
   ¿? > copy %systemroot%\system32\notepad.exe %letra% 

   El comando cd destino no hace nada ya que no accede a la variable destino, si quisieras acceder necesitarias usar procentages. El ultimo comando copiaria notepad.exe dentro de H:

d. H:\> md d1 
   ¿? > cd d1 
   ¿? > md d11 
   ¿? > set letra=H: 
   ¿? > set destino=d1\d11 
   ¿? > copy %systemroot%\system32\notepad.exe %letra%%destino%

   Este comando copiaria notepad.exe en H:d1


# Ejercicio 3
Para ayuda con el PROMPT pon HELP PROMPT
a. SET PROMPT=Introduzca orden:

b. SET PROMPT=$V $P$$

C. SET PROMPT= $D $T$G

D. SET PROMPT=$P$G

E. cd