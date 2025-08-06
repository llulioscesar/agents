# 🧠 Claude Code Agents

Este repositorio contiene agentes personalizados para Claude Code, definidos en archivos `.md`. Cada agente está diseñado para tareas específicas, siguiendo principios como claridad, simplicidad y buenas prácticas técnicas.

## 📁 Estructura del repositorio

- Un archivo `.md` por agente
- Cada archivo contiene:
  - Nombre y descripción del agente
  - Casos de uso típicos
  - Prompt base y filosofía de diseño
  - Ejemplos de interacción o uso avanzado

---

## 🧪 Ejemplo de agente: `go-coder`

Agente experto en desarrollo con Go, centrado en la filosofía minimalista del lenguaje.

### 📋 Descripción

`go-coder` analiza, revisa y ayuda a desarrollar código Go siguiendo principios como simplicidad, legibilidad, composición y diseño idiomático. Es útil para refactorización, revisión de PRs y diseño de estructuras claras.

### 💡 Casos de uso

- Revisar servicios, controladores o paquetes escritos en Go
- Refactorizar para hacer el código más idiomático
- Obtener recomendaciones sobre interfaces, errores y concurrencia
- Evaluar el uso correcto de `context`, `defer`, `iota`, `generics`, etc.

---

## 🧠 Prompt avanzado (coordinador con `go-coder`)

```plaintext
Actúa como coordinador experto en desarrollo Go siguiendo la filosofía minimalista de Go.
Tienes acceso a varios agentes auxiliares (Haiku con el agente `go-coder`) para realizar
trabajo paralelo optimizando tokens.

Objetivo principal:
1. Agregar funcionalidades para que el customer actualice nombre, correo y teléfono:
   - Para correo y teléfono, primero validar los nuevos valores con OTP.
   - Hasta que el OTP no sea confirmado, no actualizar el dato.
2. Agregar funcionalidades post-autenticación:
   - Enviar nombre y correo en caso de que falten.
3. Implementar aceptación de términos y condiciones.
4. Todo el código debe quedar en modo flat dentro de `internal/customer/`.

Instrucciones clave:
- Divide la implementación en tareas pequeñas y paralelizables.
- Genera **paquetes de tareas** que puedan ser enviados a agentes secundarios Haiku
  con el agente `go-coder` para ejecución.
- Cada paquete debe contener:
  1. Descripción clara de la subtarea
  2. Archivos de destino
  3. Pasos de implementación en Go idiomático
  4. Generación de tests unitarios para cada feature
- Optimiza el uso de tokens asignando:
  - Haiku para generación de código y tests
  - Sonnet/Opus para planificación y consolidación
- Al finalizar, genera un plan maestro y los paquetes de tareas listos para enviar.

Tu salida inicial debe ser:
1. Plan maestro con la división de tareas
2. Paquetes de tareas para cada agente
3. Instrucciones para consolidar resultados finales
