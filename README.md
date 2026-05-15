# Curso de C++

Repositorio con ejemplos prácticos de C++ moderno.

---

## Requisitos

- **Sistema operativo:** Windows
- **Compilador:** MinGW-w64 (GCC) via [WinLibs](https://winlibs.com)
- **Editor recomendado:** Visual Studio Code
- **Estándar de C++:** C++26

---

## Instalación del compilador

1. Ve a [winlibs.com](https://winlibs.com) y descarga la **última versión** bajo el runtime **UCRT**.
2. Descomprime el archivo directamente en la carpeta raíz `C:\`.
3. Presiona la tecla **Windows**, busca _"Editar las variables de entorno del sistema"_ y ábrelo.
4. Haz clic en **Variables de entorno...**.
5. En el área **Variables del sistema**, selecciona `Path` y pulsa **Editar**.
6. Pulsa **Nuevo** y agrega la siguiente ruta:
   ```
   C:\mingw64\bin
   ```
7. Guarda y acepta todas las ventanas.

> **Verificación:** Abre una terminal (`cmd` o PowerShell) y ejecuta `g++ --version`. Debería mostrar la versión instalada.

---

## Configuración de Visual Studio Code

### 1. Configuración del compilador e IntelliSense

1. Abre la **Paleta de comandos** (`Ctrl+Shift+P`).
2. Selecciona: `C/C++: Edit Configurations (UI)`.
3. Ajusta los siguientes campos:

   | Campo                 | Valor                    |
   | --------------------- | ------------------------ |
   | **Compiler path**     | `C:/mingw64/bin/g++.exe` |
   | **IntelliSense mode** | `windows-gcc-x64`        |
   | **C++ standard**      | `c++26`                  |

4. Abre el archivo `HelloWorld/src/main.cpp` y ejecútalo para confirmar que la configuración es correcta.

### 2. Configuración de la tarea de compilación

1. Ve a **Terminal > Configure Default Build Task...**.
2. Selecciona `C/C++: g++.exe build active file`.
3. Esto abrirá o creará el archivo `.vscode/tasks.json`.
4. Dentro de `args`, asegúrate de usar el estándar **C++26**:

   ```json
   "args": [
     "-std=c++26",
     "-fdiagnostics-color=always",
     "-g",
     "-Wall",
     "${fileDirname}\\*.cpp",
     "-o",
     "${fileDirname}\\${fileBasenameNoExtension}.exe"
   ],
   ```

5. Guarda el archivo. Ahora puedes compilar cualquier archivo o proyecto con `Ctrl+Shift+B`.

---

## Temario / Index

- Hello World.
- Variables.
- Basic Math.
  1. Basic math.
  2. F to C.
- Input/Output Basics.
- Arrays and Vectors.
  1. Arrays.
  2. Vectors.
- Decisions.
  1. If - else.
  2. If - else if - else.
  3. Switch.
- Loops.
  1. For.
  2. While.
  3. Do while.
- Strings.
  1. C style strings.
  2. C++ style strings.
  3. Exercise.
- Streams.
  1. Manipulators.
  2. Read files.
  3. Write files.
  4. String streams.
- Functions.
  1. Functions.
  2. Scopes.
  3. Recursivity.
- Pointers.
  1. Pointers.
  2. Pointers and functions.
  3. References.
  4. Exercise 1.
  5. Exercise 2.
- Object Oriented Programming.
  1. Objects.
  2. Public and private.
  3. Standard methods.
  4. Constructors.
  5. Copy constructor.
  6. Shallow and deep copy.
  7. Move constructor.
  8. Constant class.
  9. Static class members.
  10. Exercise.
- Overloading Operators.
  1. Overload constructor.
  2. Overload assignment operator (copy).
  3. Overload assignment operator (move).
  4. Overload operators as member functions.
  5. Overload operators as global functions.
  6. Overload insertion and extraction operators.
- Inheritance.
  1. Basic inheritance.
  2. Protected members.
  3. Constructors and destructors.
  4. Passing arguments to base/derived classes.
  5. Copy and move constructors.
  6. Exercise.
- Polymorphism.
  1. Static binding.
  2. Virtual functions.
  3. Override specifier.
  4. Base class reference.
  5. Abstract classes.
  6. Interfaces.
  7. Exercise.
- Smart Pointers.
  1. Unique pointers.
  2. Shared pointers.
  3. Weak pointers.
  4. Custom deleters.
- Exception Handling.
  1. Exception handling.
  2. Multiple exceptions.
  3. Stack unwinding.
  4. User defined exceptions.
  5. Class level exceptions.
  6. Std exception.
- Standard Template Library.
  1. Macros.
  2. Functions templates.
  3. Class templates.
  4. Class template array.
  5. Iterators.
  6. Algorithms.
  7. Arrays.
  8. Vectors.
  9. Deque.
  10. List.
  11. Sets.
  12. Map.
  13. Stack.
  14. Queue.
  15. Priority Queue.
- Lambda Expressions.
  1. Function objects.
  2. Stateless lambda.
  3. Stateful lambda.
  4. STL lambdas.
- Enumerations.
  1. Unscoped.
  2. Scoped.
