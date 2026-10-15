📘 MANUAL TÉCNICO DEL PROGRAMADOR Y ARQUITECTURA DE CÓDIGO
Proyecto: Mini Juego "Piedra, Papel o Tijera" con Persistencia (Actividad 7)
Institución: E.E.S.T. N° 1 "Eduardo Ader" — Vicente López
Asignatura: Laboratorio de Programación (LPR) — 5° Año
Docente: Mansilla Muñoz York Elías
Autor / Grupo: Ferrari Ulises, Del Pino Lucas, Mattia Federico y Orué Máximo (Grupo 3)
Fecha: 16 de octubre de 2026 | Versión: v1.0.0

📄 CONTROL DE VERSIONES Y CHANGELOG
| Versión | Fecha | Autor | Descripción de Cambios |
| :--- | :--- | :--- | :--- |
| v1.0.0 | 16/10/2026 | Grupo 3 | Versión inicial del sistema modular en C++ con struct, fstream y soporte Dual-Remote. |

🏗️ 1. ARQUITECTURA DEL SISTEMA Y ENTORNO DE DESARROLLO
Requisitos del Entorno
- Compilador: `g++` (MinGW-w64 GCC v8.1.0 o superior). Estándar C++11 habilitado.
- IDE recomendado: Visual Studio Code con extensión C/C++ Extension Pack.
- Shell: Windows PowerShell 5.1 o PowerShell Core 7+.

Estructura de Directorios del Repositorio
piedrapapelotijera/
├── .gitattributes                  <-- Normalización de finales de línea
├── .gitignore                      <-- Exclusiones de Git (.exe, .vscode/)
├── LICENSE                         <-- Licencia MIT de uso escolar
├── README.md                       <-- Portada técnica del proyecto
├── docs/                           <-- Documentación y manuales técnicos
│   ├── InformeEEST1_LPR2026_ACT07_G03_Informe_v1.0.0.pdf
│   ├── CHANGELOG.md                <-- Bitácora de versionado SemVer
│   └── manuales/
│       ├── manual_programador_v1.0.0.pdf
│       ├── manual_programador_v1.0.0.md
│       ├── manual_usuario_v1.0.0.pdf
│       └── manual_usuario_v1.0.0.md
├── src/                            <-- Código fuente compilable
│   ├── main.cpp                    <-- Código fuente C++ unificado
│   ├── historial_partidas.txt      <-- Archivo de persistencia acumulativa
│   └── piedrapapelotijera.exe      <-- Ejecutable local (ignorado por Git)
└── capturas/                       <-- Evidencias de ejecución (.png)
    ├── jugada_consola.png          <-- Captura del menú y partida jugada
    └── archivo_disco.png           <-- Captura del archivo .txt abierto

🧩 2. DOCUMENTACIÓN DE MÓDULOS Y FUNCIONES (src/main.cpp)
Módulo 1: struct Partida
- Propósito: Agrupar variables heterogéneas (`idPartida`, `jugador`, `eleccionJugador`, `eleccionIA`, `resultado`) en una sola entidad lógica para simplificar el flujo de datos.

Módulo 2: void jugarPartida(int& contadorID)
- Propósito: Gestionar la interacción con el usuario, limpiar el búfer de entrada mediante `cin.ignore()` antes de capturar el nombre con `getline()`, calcular aleatoriamente la jugada de la IA mediante `rand()`, evaluar las reglas del juego y disparar el guardado automático en disco.

Módulo 3: void guardarEnDisco(const Partida& p)
- Propósito: Abrir el flujo de salida mediante `ofstream` utilizando el modo append (`ios::app`), lo que garantiza que las partidas nuevas se añadan al final del archivo `historial_partidas.txt` sin sobrescribir los registros previos acumulados.

Módulo 4: void leerHistorialDisco()
- Propósito: Recuperar de forma secuencial y estructurada todo el contenido almacenado en el disco utilizando `ifstream` y el delimitador de comas (formato CSV) mediante la función `getline()`.

⚙️ 3. INSTRUCCIONES DE COMPILACIÓN Y DEPURACIÓN
Compilación desde PowerShell
Ubicándose en la raíz del proyecto, ejecute:
# Compilación del fuente habilitando C++11 hacia la carpeta src
g++ -std=c++11 src/main.cpp -o src/piedrapapelotijera.exe
# Ejecución del binario resultante
.\src\piedrapapelotijera.exe

Diagnóstico de Errores Frecuentes
- Error: `'g++' no se reconoce como un comando interno...`
  - Causa: Las variables de entorno de Windows (`PATH`) no incluyen el directorio bin de MinGW.
  - Solución: Agregar `C:\mingw64\bin` al PATH del sistema y reiniciar la terminal.
- Error: `fatal error: iostream: No such file or directory`
  - Causa: Instalación incompleta o corrupta de MinGW-w64.
  - Solución: Reinstalar el compilador o utilizar un entorno en línea compatible con C++11.

📚 4. REFERENCIAS
Kernighan, B. W., & Ritchie, D. M. (1988). El lenguaje de programación C (2.ª ed.). Prentice Hall.
Stroustrup, B. (2013). The C++ programming language (4th ed.). Addison-Wesley.
Microsoft Learn. (2026). Flujos de archivos en C++ (`fstream`, `ofstream`, `ifstream`). https://learn.microsoft.com/
