# Actividad 7: Mini Juego "Piedra, Papel o Tijera" con Persistencia de Datos (`struct` + `fstream`)

![C++ Version](https://img.shields.io/badge/C%2B%2B-11-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Build](https://img.shields.io/badge/Build-Passing-brightgreen.svg)

## 📌 Descripción del Proyecto

Este proyecto consiste en el desarrollo de un **Mini Juego de Piedra, Papel o Tijera** interactivo contra la Inteligencia Artificial (IA) de la consola en C++. La particularidad técnica principal radica en la diferenciación práctica entre la **Memoria RAM** (volátil) y el **Almacenamiento Secundario** (no volátil). Cada partida disputada se modela mediante una estructura (`struct Partida`) y se persiste inmediatamente en disco dentro de un archivo de texto plano (`src/historial_partidas.txt`) mediante flujos de archivos (`ofstream` en modo `ios::app`).

Además, permite la lectura y despliegue del historial acumulado (`ifstream`), garantizando la preservación de los datos incluso tras cerrar la ejecución del programa.

---

## 👨‍💻 Información Institucional y del Autor

* **Institución:** E.E.S.T. N.º 1 "Eduardo Ader" - Vicente López
* **Materia:** Laboratorio de Programación (LPR)
* **Curso:** 5° Año 3° División (Grupos A-B)
* **Estudiante:** Ferrari Ulises
* **Profesor:** Mansilla Muñoz York Elías y Ganduglia Yamil
* **Ciclo Lectivo:** 2° Cuatrimestre 2026

---

## 📂 Estructura del Repositorio

```text
piedrapapelotijera/
├── .gitattributes
├── .gitignore
├── LICENSE
├── README.md
├── docs/
│   ├── CHANGELOG.md
│   └── InformeEEST1_LPR2026_ACT07_G03_FerrariUlises_Informe_v1.0.0.pdf
└── src/
    ├── main.cpp
    ├── historial_partidas.txt
    └── capturas/
        ├── jugada_consola.png
        └── archivo_disco.png
```

---

## 🛠️ Requisitos de Compilación y Ejecución

### Prerrequisitos
* Compilador GCC (`g++`) compatible con estándar **C++11** o superior.
* Entorno de terminal (PowerShell en VS Code, Bash, etc.).

### Comandos de Compilación en PowerShell
```powershell
# Compilación limpia asegurando estándar C++11
g++ -std=c++11 src/main.cpp -o src/piedrapapelotijera.exe

# Ejecución del programa
.\src\piedrapapelotijera.exe
```

---

## 🔄 Sincronización Dual-Remote (Git)

El proyecto cuenta con un entorno de repositorio distribuido configurado en dos servicios remotos:

* **GitHub:** `https://github.com/Ferraribip/repasogeneral.git`
* **GitLab:** `https://gitlab.com/Ferraribip/repasogeneral.git`

Para realizar el *push* dual:
```powershell
git push origin main
git push gitlab main
```
