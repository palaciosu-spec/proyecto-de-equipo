# proyecto-de-equipo
# registro.py

alumnos = []

def registrar_alumno():
    print("=== Registro de Alumno ===")
    
    nombre = input("Ingresa tu nombre: ")
    edad = input("Ingresa tu edad: ")
    grupo = input("Ingresa tu grupo: ")

    alumno = {
        "nombre": nombre,
        "edad": edad,
        "grupo": grupo
    }

    alumnos.append(alumno)
    print("✅ Alumno registrado correctamente\n")
    
# mostrar.py

def mostrar_alumnos(alumnos):
    print(“=== Lista de Alumnos ===“)
    
    if len(alumnos) == 0:
        print(“No hay alumnos registrados”)
    
    for a in alumnos:
        print(f”Nombre: {a[‘nombre’]} | Edad: {a[‘edad’]} | Grupo: {a[‘grupo’]}”)
        
# main.py

from registro import registrar_alumno
from mostrar import mostrar_alumnos

alumnos = []

while True:
    print(“\n1. Registrar alumno”)
    print(“2. Mostrar alumnos”)
    print(“3. Salir”)

    opcion = input(“Elige una opción: “)

    if opcion == “1”:
        registrar_alumno(alumnos)
    elif opcion == “2”:
        mostrar_alumnos(alumnos)
    elif opcion == “3”:
        break
    else:
        print(“❌ Opción inválida”)
