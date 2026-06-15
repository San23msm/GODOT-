# Guía de Uso de Godot con C# y Visual Studio

## Objetivo

Esta guía explica cómo configurar Godot para trabajar con C# (.NET) utilizando Visual Studio como entorno de desarrollo.

---

# Requisitos Previos

Antes de comenzar, es necesario instalar los siguientes componentes:

## 1. Instalar .NET SDK

Godot utiliza .NET para compilar y ejecutar scripts en C#.

Descargar e instalar la versión más reciente del SDK de .NET desde el sitio oficial de Microsoft.

Para verificar la instalación, abrir una terminal y ejecutar:

```bash
dotnet --version
```

Si se muestra un número de versión, la instalación fue exitosa.

---

## 2. Instalar Visual Studio

Durante la instalación de Visual Studio se recomienda seleccionar:

* Desarrollo de escritorio con .NET.
* Herramientas de C#.
* SDK de .NET.

Visual Studio proporcionará:

* Autocompletado de código.
* Depuración (Debugging).
* Administración de proyectos.
* Navegación entre clases y métodos.

---

## 3. Instalar Godot con soporte .NET

Es importante descargar la versión de Godot que incluya soporte para .NET.

Una vez instalada, abrir Godot y crear un nuevo proyecto.

---

# Creación de un Proyecto

## Paso 1: Crear un nuevo proyecto

1. Abrir Godot.
2. Seleccionar "Create Project".
3. Elegir un nombre para el proyecto.
4. Seleccionar la carpeta de almacenamiento.
5. Crear el proyecto.

---

## Paso 2: Verificar soporte de C#

Al crear un script nuevo:

1. Seleccionar un nodo.
2. Presionar "Attach Script".
3. Elegir el lenguaje "C#".

Godot generará automáticamente:

```text
Proyecto
│
├── Proyecto.csproj
├── Main.cs
└── Archivos del proyecto
```

El archivo `.csproj` es administrado por .NET y contiene la configuración del proyecto.

---

# Abrir el Proyecto en Visual Studio

## Paso 1: Configurar el editor externo

Dentro de Godot:

Editor → Editor Settings → Dotnet

Configurar Visual Studio como editor externo.

---

## Paso 2: Abrir el proyecto

Seleccionar cualquier script C# y presionar:

```text
Open in External Editor
```

Visual Studio abrirá automáticamente el proyecto completo.

---

# Estructura Básica de un Script

Ejemplo:

```csharp
using Godot;
using System;

public partial class Player : Node2D
{
    public override void _Ready()
    {
        GD.Print("Hola Mundo");
    }

    public override void _Process(double delta)
    {

    }
}
```

---

# Métodos Principales

## _Ready()

Se ejecuta una sola vez cuando el nodo entra en la escena.

```csharp
public override void _Ready()
{
    GD.Print("Escena cargada");
}
```

---

## _Process()

Se ejecuta cada frame.

```csharp
public override void _Process(double delta)
{
    Position += new Vector2(100,0) * (float)delta;
}
```

---

# Compilar el Proyecto

Godot compila automáticamente cuando se ejecuta el juego.

También puede compilarse manualmente desde:

Build → Build Project

Si existen errores, aparecerán en el panel de salida.

---

# Uso del Debugger

Visual Studio permite:

* Colocar puntos de interrupción (Breakpoints).
* Inspeccionar variables.
* Ejecutar paso a paso.
* Analizar errores en tiempo real.

Para agregar un breakpoint:

1. Hacer clic a la izquierda del número de línea.
2. Ejecutar el proyecto.
3. Cuando la ejecución llegue a esa línea, se detendrá.

---

# Buenas Prácticas

* Utilizar nombres descriptivos para clases y variables.
* Mantener una clase por archivo.
* Organizar scripts en carpetas.
* Evitar duplicación de código.
* Aplicar principios de Programación Orientada a Objetos.
* Documentar sistemas importantes.

---

# Flujo de Trabajo Recomendado

1. Crear escenas en Godot.
2. Crear scripts C# para la lógica.
3. Editar código en Visual Studio.
4. Ejecutar y probar desde Godot.
5. Corregir errores mediante Debug.
6. Guardar cambios en Git.
7. Realizar commits frecuentes.

---

# Conclusión

La integración entre Godot, C# y Visual Studio proporciona un entorno profesional para el desarrollo de videojuegos. Gracias a las herramientas del ecosistema .NET es posible crear proyectos organizados, escalables y mantenibles, aplicando prácticas utilizadas en el desarrollo de software moderno.
