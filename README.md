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
