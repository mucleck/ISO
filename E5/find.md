1. 
a   sort ro.dat /+28 > ro1.dat

b. find ro.dat "AÑOS APTO" > APTOS.DAT 

find ro.dat "AÑOS NO APTO" > NOAPTOS.DAT 

c. find "LICENCIADO" APTOS.DAT > LINCAPT.DAT

d. find "AÑOS APTO" ro.dat | find "LICENCIADO"

e. sort ro.dat /+41

f. 
    find "DIPLOMADO" < ro.dat > TU.DAT
    sort TU.DAT 
    find "LICENCIADO" < ro.dat >> TU.DAT
   
