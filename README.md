Seccion de quests por entregar

nombre = input("Ingresa tu nombre: ")
edad = int(input("Ingresa tu edad: "))

if edad >= 0 and edad <= 5:
    print(f"{nombre} perteneces a la primera infancia.")

elif edad >= 6 and edad <= 12:
    print(f"{nombre} perteneces a la niñez.")

elif edad >= 13 and edad <= 14:
    print(f"{nombre} perteneces a la preadolescencia.")

elif edad >= 15 and edad <= 19:
    print(f"{nombre} perteneces a la adolescencia tardía.")

elif edad >= 20 and edad <= 26:
    print(f"{nombre} perteneces a los adultos jóvenes.")

elif edad >= 27 and edad <= 59:
    print(f"{nombre} perteneces a la adultez general.")

elif edad >= 60:
    print(f"{nombre} eres un adulto mayor.")

else:
    print("Edad no válida.")
     

c=0
for tabla in range(4,41,4):
  c=c+1
  print(f"4x{c}={tabla}")
     
4x1=4
4x2=8
4x3=12
4x4=16
4x5=20
4x6=24
4x7=28
4x8=32
4x9=36
4x10=40

n=int(input("cual numero?"))
for i in range(1,11):
  print(f"{n}x{i}={n*i}")
     
cual numero?9
9x1=9
9x2=18
9x3=27
9x4=36
9x5=45
9x6=54
9x7=63
9x8=72
9x9=81
9x10=90

n=int(input("ingrese un numero:"))
for i in range(1,n+1):
  if i==1:
    print("1", end = " ")
else:
      if i%2==0:
        print(f"-1/{i}", end = " ")
      else:
          print(f"+1/{i}", end = " ")
     
ingrese un numero:9
1 +1/9 

total_personas = 28
suma_experiencia = 0

for i in range(total_personas):
    while True:
        try:
            exp = float(input(f"Ingrese la experiencia de la persona {i + 1}: "))
            if exp < 0:
                print("La experiencia no puede ser negativa. Intente de nuevo.")
                continue
            break
        except ValueError:
            print("Entrada inválida. Ingrese un número.")

    suma_experiencia += exp

# Cálculo del promedio
promedio = suma_experiencia / total_personas

# Clasificación del nivel
if promedio < 1:
    nivel = "Salón mayormente sin experiencia"
elif promedio <= 3:
    nivel = "Salón con experiencia básica"
elif promedio <= 6:
    nivel = "Salón con experiencia intermedia"
else:
    nivel = "Salón con experiencia avanzada"

# Resultados
print(f"\nEl promedio de experiencia del salón es: {promedio:.2f}")
print(f"Nivel general: {nivel}")
     
Ingrese la experiencia de la persona 1: 34
Ingrese la experiencia de la persona 2: 67
Ingrese la experiencia de la persona 3: 356
Ingrese la experiencia de la persona 4: 525
Ingrese la experiencia de la persona 5: 7
Ingrese la experiencia de la persona 6: 6867
Ingrese la experiencia de la persona 7: 34
Ingrese la experiencia de la persona 8: 75
Ingrese la experiencia de la persona 9: 374
Ingrese la experiencia de la persona 10: 2983
Ingrese la experiencia de la persona 11: 27894
Ingrese la experiencia de la persona 12: 28
Ingrese la experiencia de la persona 13: 938
Ingrese la experiencia de la persona 14: 82494
Ingrese la experiencia de la persona 15: 3829
Ingrese la experiencia de la persona 16: 21
Ingrese la experiencia de la persona 17: 839
Ingrese la experiencia de la persona 18: 283928
Ingrese la experiencia de la persona 19: 829
Ingrese la experiencia de la persona 20: 84938
Ingrese la experiencia de la persona 21: 18
Ingrese la experiencia de la persona 22: 83018
Ingrese la experiencia de la persona 23: 8293
Ingrese la experiencia de la persona 24: 7426
Ingrese la experiencia de la persona 25: 719
Ingrese la experiencia de la persona 26: 279472
Ingrese la experiencia de la persona 27: 8129
Ingrese la experiencia de la persona 28: 7849

El promedio de experiencia del salón es: 31856.57
Nivel general: Salón con experiencia avanzada

import random

total_objetos = 50
objetos = ["Sirven"] * total_objetos

# Marcar algunos como dañados
for _ in range(5):
    pos = random.randint(0, total_objetos - 1)
    objetos[pos] = "dañado"

# Mostrar los defectuosos
print("Objetos defectuosos:")
for i, estado in enumerate(objetos):
    if estado == "dañado":
        print(f"Defectuoso el {i}")
     
Objetos defectuosos:
Defectuoso el 2
Defectuoso el 3
Defectuoso el 8
Defectuoso el 43
Defectuoso el 49
crear una lista con los numeros pares presentes hasta el 20

pares=[i
   for i in range(21)
   if i % 2==0]
print(pares)
     
[0, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20]

recursos=[10,20,15,30,25]
dobles=[j*2 for j in recursos]
print(dobles)
     
[20, 40, 30, 60, 50]

lis=[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20]
nx=[l**3 for l in lis]
print(nx)
     
[1, 8, 27, 64, 125, 216, 343, 512, 729, 1000, 1331, 1728, 2197, 2744, 3375, 4096, 4913, 5832, 6859, 8000]

personajes=["alcaldesa","constructor","paladin","bardo"]
mayus=[nombre.upper()for nombre in personajes]
print(mayus)
     
['ALCALDESA', 'CONSTRUCTOR', 'PALADIN', 'BARDO']

objetos=["ESPADA","PICO","MARTILLO","MAPA","CHEMCOIN"]
cantidad_letras=[]
for objeto in objetos:
  cantidad_letras.append(len(objeto))
  print(cantidad_letras)
     
[6]
[6, 4]
[6, 4, 8]
[6, 4, 8, 4]
[6, 4, 8, 4, 8]

divisibles=[n for n in range(1,101)if n %6 ==0]
print(divisibles)
     
[6, 12, 18, 24, 30, 36, 42, 48, 54, 60, 66, 72, 78, 84, 90, 96]
