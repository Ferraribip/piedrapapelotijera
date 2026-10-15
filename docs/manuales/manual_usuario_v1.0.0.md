📕 GUÍA DE USUARIO Y OPERACIÓN DEL SISTEMA
Proyecto: Mini Juego "Piedra, Papel o Tijera" con Persistencia (Actividad 7)
Institución: E.E.S.T. N° 1 "Eduardo Ader" — Vicente López
Asignatura: Laboratorio de Programación (LPR) — 5° Año
Autores: Ferrari Ulises, Del Pino Lucas, Mattia Federico y Orué Máximo (Grupo 3)
Versión: v1.0.0 | Fecha: Octubre de 2026

📄 CONTROL DE VERSIONES
| Versión | Fecha | Descripción |
| :--- | :--- | :--- |
| v1.0.0 | 16/10/2026 | Emisión de la guía inicial de usuario para el sistema de juego y persistencia en consola. |

💻 1. REQUISITOS MÍNIMOS DEL SISTEMA
- Sistema Operativo: Windows 10 o Windows 11 (64-bit).
- Consola de Comandos: Windows PowerShell o Símbolo del sistema (CMD).
- Memoria RAM: 512MB libres.
- Almacenamiento: 10MB de espacio disponible en disco.

🚀 2. GUÍA PASO A PASO DE EJECUCIÓN
Paso 1: Apertura de la Terminal
Abra la carpeta del proyecto `piedrapapelotijera`, presione la tecla Shift y haga clic derecho en un área vacía. Seleccione "Abrir la ventana de PowerShell aquí".

Paso 2: Invocación del Ejecutable
En la línea de comandos, ingrese la ruta del binario compilado con soporte C++11 y presione Enter:
.\src\piedrapapelotijera.exe

Paso 3: Interacción con el Menú Principal
Una vez ejecutado, el sistema desplegará el menú interactivo con las siguientes opciones:
1. Jugar Partida (Piedra, Papel o Tijera contra la IA).
2. Ver Historial de Partidas Guardadas en Disco (`.txt`).
3. Salir del Sistema.

Figura 1
Salida en consola del juego y registro en disco
=====================================================
 LPR 2026 - ACTIVIDAD 7: PIEDRA, PAPEL O TIJERA
 Estudiante: Ferrari Ulises (5° 3°)
=====================================================

--- MENÚ PRINCIPAL DE JUEGO Y PERSISTENCIA ---
1. Jugar Partida (Piedra, Papel o Tijera)
2. Ver Historial de Partidas Guardadas en Disco (.txt)
3. Salir del Sistema
Ingrese una opcion (1-3): 1

--- NUEVA PARTIDA #1 ---
Ingrese su Nombre / Nickname: Ulises

Elija su jugada:
1. Piedra
2. Papel
3. Tijera
Opcion (1-3): 1

[JUGADA] Ulises eligio: Piedra
[JUGADA] La IA eligio: Tijera
=> RESULTADO: Victoria!
[DISCO] Partida resguardada con exito en 'historial_partidas.txt'.
Nota. La captura ilustra la ejecución interactiva del minijuego, la evaluación de las reglas frente a la IA y el almacenamiento automático de los datos estructurados en el archivo secundario.

❓ 3. RESOLUCIÓN DE PROBLEMAS FRECUENTES (FAQ)
1. La ventana de la consola se abre y se cierra instantáneamente.
   - Causa: El programa finalizó su ejecución y Windows cerró la ventana emergente.
   - Solución: Ejecute siempre el archivo desde una ventana de PowerShell previamente abierta, en lugar de hacer doble clic directo sobre `piedrapapelotijera.exe`.
2. Windows Defender o SmartScreen bloquea la ejecución.
   - Causa: El archivo ejecutable ha sido compilado localmente y no posee firma digital corporativa.
   - Solución: En la advertencia de SmartScreen, haga clic en "Más información" y luego seleccione el botón "Ejecutar de todas formas".
3. El archivo de historial no se genera o aparece vacío.
   - Causa: No se ha completado al menos una partida seleccionando la opción 1.
   - Solución: Juegue una partida completa; el archivo `historial_partidas.txt` se creará automáticamente en la carpeta `src/`.

📚 4. REFERENCIAS
Microsoft Corporation. (2026). Documentación de Windows PowerShell. https://learn.microsoft.com/powershell/
