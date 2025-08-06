# 🧠 Claude Code Agents

Repositorio de agentes personalizados para Claude Code. Cada agente está documentado en un archivo `.md` y diseñado para tareas específicas, con un enfoque en buenas prácticas, claridad y reutilización.

## 📦 Estructura del repositorio

- Un archivo `.md` por agente
- Cada archivo contiene:
  - Nombre y descripción del agente
  - Casos de uso
  - Prompt base y principios de comportamiento
  - Ejemplos de interacción
  - Enfoques y lineamientos técnicos

---

## 🔍 Ejemplo: `[go-coder](./go-coder.md)`

Agente experto en desarrollo Go, orientado a la filosofía minimalista e idiomática del lenguaje.

### 📋 Descripción

`go-coder` es un agente que revisa código Go para asegurar que siga los principios de simplicidad, claridad y diseño pragmático. Ideal para revisiones de código, refactorizaciones y buenas prácticas.

### 💡 Casos de uso

- Revisión de controladores o servicios escritos en Go
- Evaluación de patrones idiomáticos y estructuras
- Feedback sobre errores, concurrencia y diseño de interfaces

### 🧱 Principios clave

- Interfaces pequeñas y claras
- Manejo explícito de errores
- Uso correcto de goroutines, canales y context
- Código idiomático (`go fmt`, `iota`, `defer`, etc.)
- Uso prudente de generics y abstracciones
- Estructura del proyecto alineada con convenciones Go

### 🛠️ Ejemplo de prompt

```plaintext
Usuario: Acabo de implementar un handler de registro de usuarios en Go. ¿Puedes revisarlo para asegurar que sigue las mejores prácticas de Go?

Asistente: Usaré el agente `go-coder` para analizar tu código y asegurarme de que cumple con la filosofía y los patrones idiomáticos de Go.
