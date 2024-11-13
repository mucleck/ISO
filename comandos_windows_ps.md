# POWERSHELL
## EJERCICIO 1

```ps
New-Item -Name "ARCH1.txt" -ItemType File
New-Item -ItemType Directory -Name "d2"
Set-Location d2
New-Item -ItemType Directory -Name "d21"
Set-Location ..
New-Item -ItemType Directory -Name "d3"
Set-Location ..
New-Item -ItemType Directory -Name "d1"
Set-Location d1
New-Item -ItemType Directory -Name "d11"
Set-Location d11
New-Item -Name "ARCH2.txt" -ItemType File

New-Item -ItemType Directory -Path "..\..\d2\d21\d211"
New-Item -ItemType Directory -Path "..\..\d2\d22"
New-Item -Name "ARCH3.txt" -Path "..\..\d2\d22" -ItemType File
New-Item -Name "ARCH6.txt" -Path "..\..\d2\d21\d211" -ItemType File
New-Item -Name "ARCH8.txt" -Path "..\..\d3" -ItemType File

New-Item -Name "ARCH5.txt" -Path "..\..\d2\d22" -ItemType File
New-Item -ItemType Directory -Path "..\..\d4"
New-Item -Name "ARCH9.txt" -Path "..\..\d4" -ItemType File
New-Item -ItemType Directory -Path "..\d12"

Set-Location /
Set-Location d3
Copy-Item "..\d2\d22\ARCH3.txt" -Destination "..\d1\d12\"
Copy-Item "ARCH8.txt" -Destination "..\d1\d12\"
Rename-Item "..\d1\d12\ARCH8.txt" "ARCH4.txt"

New-Item -ItemType Directory -Path "..\..\d3\d31"
```


## EJERICIO 2

```ps
Set-Location 'H:\d1\d12' | Rename-Item -NewName { $_.Name -replace '.txt', '.DAT' }
```
## EJERCICIO 3

```ps
Get-Content "..\arch3.txt"
Remove-Item -Recurse "d12"    
Copy-Item "..\d2\d22\arch3.txt" -Destination "h:\d3\fich3.dat"   
Copy-Item "arch5.txt" -Destination "\d4"     
Copy-Item "arch5.txt" -Destination "d4" 

```
## EJERCICIO 4

```ps
a.
Get-ChildItem "\d1\d12" | Sort-Object CreationTime

b.
Get-ChildItem "\d1\d12" | Sort-Object CreationTime -Descending

c.
Get-ChildItem -Path "ARCH3.*" -Recurse

```

## EJERCICIO 5

No existe el + en powershell

## EJERICIO 6 
```ps
a.
Copy-Item "H:\d4\ARCH9.txt" -Destination "H:\d2\d21\d211\"

b.
Copy-Item "..\d4\ARCH9.txt" -Destination "d21\d211\"

c.
Copy-Item "ARCH9.TXT" -Destination "..\d2\d21\d211"

d.
Copy-Item "..\..\d4\ARCH9.txt" -Destination "..\d21\d211"

e.
Copy-Item "..\..\..\d4\ARCH9.txt" -Destination "."

f.
Copy-Item "d4\ARCH9.txt" -Destination "d2\d21\d211"
```

## Ejercicio 7 
```ps
1.
Copy-Item "ARCH1.txt" -Destination "d0"

2.
Copy-Item "d1\d11\ARCH2.txt" -Destination "d0\d1\d11"

3.
Copy-Item "d1\d12\ARCH4.txt" -Destination "d0\d1\d12"

4.
Copy-Item "d1\d12\ARCH3.txt" -Destination "d0\d1\d12"

5.
Copy-Item "d2\d21\d211\ARCH6.txt" -Destination "d0\d2\d21\d211"

6.
Copy-Item "d2\d22\ARCH3.txt" -Destination "d0\d2\d22"

7.
Copy-Item "d3\ARCH8.txt" -Destination "d0\d3"

8.
Copy-Item "d4\ARCH9.txt" -Destination "d0\d4"
```

## EJERICIO 8

```ps
a.
Set-Location "d0\d2"
Set-Location "d22"
Remove-Item "ARCH3.txt"
Set-Location ..
Remove-Item "d22"

Set-Location "21"
Remove-Item "ARCH5.txt"
Set-Location "d211"
Remove-Item "ARCH6.txt"
Set-Location ..
Remove-Item "d211"
Set-Location ..
Remove-Item "21"

Set-Location ..
Remove-Item "d2"
```
```ps
b.
Remove-Item "d2\d22\ARCH3.txt"
Remove-Item "d2\d22"

Remove-Item "d2\d21\ARCH5.txt"
Remove-Item "d2\d21\d211\ARCH6.txt"
Remove-Item "d2\d21\d211"
Remove-Item "d2\d21"
Remove-Item "d2"
```
```ps
c. 
Remove-Item "..\..\d2\d22\ARCH3.txt"
Remove-Item "..\..\d2\d22"

Remove-Item "..\..\d2\d21\ARCH5.txt"
Remove-Item "..\..\d2\d21\d211\ARCH6.txt"
Remove-Item "..\..\d2\d21\d211"
Remove-Item "..\..\d2\d21"
Remove-Item "..\..\d2"
```


## EJERCICIO 9 
```ps
a. Get-ChildItem "c???*.dat"
b. Get-ChildItem "?o*.txt"
```
