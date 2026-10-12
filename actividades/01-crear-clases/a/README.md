# Experiencia 01: Crear clases

## Descripción
Sistema de matrícula sencillo por consola. Registra los datos de un estudiante
(nombre, edad y grado) y, mediante un menú, permite imprimirlos, matricularlo y
registrar el pago de su pensión.

## Funcionamiento
La clase `Estudiante` (`estudiante.py`) guarda los atributos `nombre`, `edad` y
`grado`, y tiene los métodos `ingresarDatos()`, `imprimirDatos()`,
`matricular()` y `pagarPension()`.

`menu.py` pide los datos del estudiante, crea la instancia y entra en un bucle
que muestra el menú y ejecuta el método correspondiente a la opción elegida,
hasta que se selecciona **Salir**. `test.py` crea objetos directamente y
ejecuta los métodos sin pasar por el menú.

Los métodos `matricular()` y `pagarPension()` solo muestran un mensaje en
pantalla; no guardan ningún estado.

## Conceptos aplicados
POO (clases, objetos y métodos) · importación de módulos · entrada y salida por
consola · bucle con menú

## Ejecución
```
cd 01-crear-clases
python menu.py
python test.py
```

## Resultado
```
Ingrese el nombre del estudiante: Juan
Ingrese la edad del estudiante: 16
Ingrese el grado del estudiante: 5
--- MENU ---
1. Ingresar datos
2. Imprimir datos
3. Matricular
4. Pagar pension
5. Salir
Seleccione una opcion: 3
Juan ha sido matriculado en el grado 5
--- MENU ---
...
Seleccione una opcion: 5
Saliendo del programa...
```

## Limitaciones y mejoras
- Los datos solo existen en memoria y se pierden al cerrar el programa.
  Mejora: guardarlos en un archivo `.json` o en una base de datos.
- No valida la entrada: si la edad no es un número, el programa se detiene con
  un error. Mejora: validar con `try/except`.
- Maneja un solo estudiante a la vez.