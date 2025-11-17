# 🎯 Bloque 1: Metodologías Ágiles

**Objetivo:** Aprender a trabajar con Scrum y GitHub Flow en proyectos reales

---

## 📑 Índice de Contenidos

1. [Introducción a las Metodologías Ágiles](#1-introducción-a-las-metodologías-ágiles)
2. [Scrum Framework](#2-scrum-framework)
   - [Roles de Scrum](#-roles-de-scrum)
   - [Eventos de Scrum](#-eventos-de-scrum)
   - [Artefactos de Scrum](#-artefactos-de-scrum)
3. [GitHub Flow](#3-github-flow)
   - [Ramas (Branches)](#-1-ramas-branches)
   - [Pull Requests](#-2-pull-requests-pr)
   - [Code Review](#-3-code-review)
   - [Integración Continua](#-4-integración-continua-ci)
4. [Herramientas de Gestión](#4-herramientas-de-gestión)
   - [GitHub Issues](#-github-issues)
   - [GitHub Projects](#-github-projects)
   - [Milestones](#-milestones)
5. [Ejercicios Prácticos](#5-ejercicios-prácticos)

---

## 1. Introducción a las Metodologías Ágiles

Las metodologías ágiles surgieron como respuesta a las limitaciones de los enfoques tradicionales de desarrollo de software (modelo cascada). Se basan en el **Manifiesto Ágil** (2001), que prioriza:

### Los 4 Valores del Manifiesto Ágil

> ✨ **Individuos e interacciones** sobre procesos y herramientas  
> ✨ **Software funcionando** sobre documentación extensiva  
> ✨ **Colaboración con el cliente** sobre negociación contractual  
> ✨ **Respuesta ante el cambio** sobre seguir un plan

### ¿Por qué metodologías ágiles?

- ✅ **Entregas frecuentes:** Valor al cliente desde las primeras semanas
- ✅ **Adaptabilidad:** Respuesta rápida a cambios en requisitos
- ✅ **Colaboración:** Equipos autoorganizados y multifuncionales
- ✅ **Mejora continua:** Retrospectivas y aprendizaje constante
- ✅ **Transparencia:** Visibilidad del progreso en todo momento

### Comparación: Cascada vs Ágil

| Aspecto | 🔻 Cascada | 🔄 Ágil |
|---------|------------|---------|
| **Proceso** | Requisitos → Diseño → Desarrollo → Pruebas → Despliegue | Ciclos iterativos cortos |
| **Duración de ciclos** | Meses o años | 1-4 semanas (sprints) |
| **Entrega** | Una única entrega final | Entregas incrementales frecuentes |
| **Cambios** | Costosos y difíciles | Bienvenidos y esperados |
| **Feedback** | Tardío (al final) | Continuo (en cada sprint) |
| **Riesgo** | Alto (problemas al final) | Bajo (detección temprana) |

---

## 2. Scrum Framework

Scrum es el framework ágil más utilizado en desarrollo de software. Se basa en ciclos iterativos llamados **Sprints**, donde equipos multifuncionales entregan incrementos de producto potencialmente desplegables.

### 🔄 El Ciclo de Scrum

```
Product Backlog → Sprint Planning → Sprint (1-4 semanas) → Daily Scrums
                                           ↓
                      Sprint Retrospective ← Sprint Review ← Incremento
                              ↓
                      (Volver a empezar)
```

---

## 🎭 Roles de Scrum

### 1. Product Owner (PO)

**Responsabilidades:**
- ✅ Maximizar el valor del producto
- ✅ Gestionar y priorizar el Product Backlog
- ✅ Definir claramente los items del Backlog
- ✅ Asegurar que el equipo comprende los items
- ✅ Aceptar o rechazar el trabajo completado

---

### 2. Scrum Master (SM)

**Responsabilidades:**
- ✅ Facilitar todos los eventos de Scrum
- ✅ Eliminar impedimentos del equipo
- ✅ Proteger al equipo de interrupciones externas
- ✅ Promover y apoyar Scrum
- ✅ Ayudar al equipo a mejorar continuamente

---

### 3. Development Team (Equipo de Desarrollo)

**Responsabilidades:**
- ✅ Desarrollar el incremento de producto
- ✅ Autoorganizarse para alcanzar el Sprint Goal
- ✅ Estimar el esfuerzo de las tareas
- ✅ Garantizar la calidad del producto
- ✅ Ser multifuncionales (frontend, backend, testing, etc.)

---

## 📅 Eventos de Scrum

### 1. Sprint Planning (Planificación del Sprint)

**⏱️ Duración:** 2-4 horas para sprint de 2 semanas  
**🎯 Objetivo:** Definir qué se va a hacer y cómo

**Preguntas clave:**
1. **¿Qué puede entregarse en este Sprint?** → Sprint Goal
2. **¿Cómo se realizará el trabajo?** → Sprint Backlog

**Resultado:**
- Sprint Goal definido
- Sprint Backlog con tareas asignadas
- Compromiso del equipo

---

### 2. Daily Scrum (Reunión Diaria)

**⏱️ Duración:** 15 minutos máximo (¡timeboxed!)  
**🎯 Objetivo:** Sincronizar actividades y planificar las próximas 24 horas

**Las 3 preguntas:**

1. ¿Qué hice **ayer** para ayudar al equipo a cumplir el Sprint Goal?
2. ¿Qué haré **hoy** para ayudar al equipo a cumplir el Sprint Goal?
3. ¿Veo algún **impedimento** que evite que el equipo cumpla el Sprint Goal?

**💡 Tips:**
- Misma hora y lugar todos los días
- No es una reunión de reporte al Scrum Master
- Enfocada en la colaboración del equipo

---

### 3. Sprint Review (Revisión del Sprint)

**⏱️ Duración:** 1-2 horas para sprint de 2 semanas  
**🎯 Objetivo:** Inspeccionar el incremento y adaptar el Product Backlog

**Actividades:**
1. El equipo demuestra el trabajo completado
2. Se obtiene feedback del Product Owner
3. Se revisa el Product Backlog según sea necesario
4. Se discute qué hacer a continuación
5. Se actualiza la proyección de fechas

**Es una demo del programa, no una presentación de PowerPoint! 🎬**

---

### 4. Sprint Retrospective (Retrospectiva del Sprint)

**⏱️ Duración:** 1-1.5 horas para sprint de 2 semanas  
**🎯 Objetivo:** Mejorar continuamente el proceso y el equipo

**Formato típico - "Estrella de mar" ⭐**

| Categoría | Descripción | Ejemplo |
|-----------|-------------|---------|
| ⭐ **Empezar a hacer** | Prácticas nuevas a adoptar | Pair programming en tareas complejas |
| 📈 **Hacer más** | Lo que funciona bien | Code reviews más detallados |
| ➡️ **Seguir haciendo** | Lo que funciona correctamente | Daily Scrums a las 9:00 |
| 📉 **Hacer menos** | No aporta suficiente valor | Reuniones largas sin agenda |
| 🛑 **Dejar de hacer** | Nos está perjudicando | Commits directos a main |

**Resultado:**
- Lista de acciones de mejora concretas (1-3 máximo)
- Asignación de responsables
- Plan para implementarlas en el próximo sprint

---

## 📦 Artefactos de Scrum

### 1. Product Backlog

Lista ordenada y dinámica de todo lo que se necesita en el producto. El Product Owner es responsable de su contenido, disponibilidad y ordenamiento.

**Características de buenos items (INVEST):**
- **I**ndependiente: Puede desarrollarse por separado
- **N**egociable: Flexible en su implementación
- **V**aliosa: Aporta valor al usuario
- **E**stimable: Se puede estimar su esfuerzo
- **S**mall (Pequeña): Completable en un sprint
- **T**esteable: Se puede verificar su cumplimiento

---

### 2. Sprint Backlog

Conjunto de items del Product Backlog seleccionados para el Sprint, más el plan para entregarlos.

**Incluye:**
- 🎯 Sprint Goal
- 📋 Items seleccionados del Product Backlog
- ✅ Tareas necesarias para completar cada item
- 👤 Asignaciones del equipo

**Visibilidad:**
Actualizado diariamente durante el Daily Scrum

---

### 3. Increment (Incremento)

La suma de todos los items del Product Backlog completados durante el Sprint, más los incrementos de sprints anteriores.

**Debe cumplir la Definition of Done (DoD):**

#### 📋 Ejemplo de Definition of Done

- [x] Código escrito siguiendo las guías de estilo
- [x] Code review completado y aprobado
- [x] Tests unitarios escritos y pasando (>80% cobertura)
- [x] Tests de integración pasando
- [x] Documentación actualizada
- [x] Sin errores de linter/análisis estático
- [x] Desplegado en entorno de pruebas
- [x] Aprobado por el Product Owner

---

## 3. GitHub Flow

GitHub Flow es un flujo de trabajo ligero y basado en ramas que soporta equipos y proyectos con despliegues regulares. Es perfecto para combinar con Scrum.

### 🔄 El Flujo de GitHub Flow

```
1. Crear rama desde develop
        ↓
2. Añadir commits
        ↓
3. Abrir Pull Request
        ↓
4. Discutir y revisar código
        ↓
5. Merge a main
        ↓
6. Deploy inmediato
```

---

## 🌿 1. Ramas (Branches)

Cada nueva funcionalidad, corrección de bug o experimento se desarrolla en su propia rama.

### Nomenclatura recomendada

```bash
feature/nombre-funcionalidad    # Nueva funcionalidad
fix/nombre-bug                  # Corrección de errores
hotfix/nombre-urgente          # Corrección urgente en producción
docs/actualizar-readme         # Cambios en documentación
refactor/mejorar-componente    # Refactorización
test/añadir-tests-login        # Añadir tests
```

### Comandos básicos

```bash
# Crear y cambiar a una nueva rama
git checkout -b feature/login-usuario

# Ver todas las ramas
git branch -a

# Cambiar de rama
git checkout main

# Actualizar tu rama con los últimos cambios de main
git checkout feature/login-usuario
git merge main

# Eliminar rama local
git branch -d feature/login-usuario

# Eliminar rama remota
git push origin --delete feature/login-usuario
```

### 💡 Buenas prácticas

- ✅ Una rama por funcionalidad/fix
- ✅ Nombres descriptivos y concisos
- ✅ Mantener ramas actualizadas con develop
- ✅ Ramas de corta duración (1-3 días máximo)
- ✅ Eliminar ramas después del merge

---

## 📤 2. Pull Requests (PR)

Un Pull Request es una solicitud para fusionar cambios de una rama a otra (normalmente a `main`). Es el corazón de la colaboración en GitHub.

### Anatomía de un buen Pull Request

#### ✍️ Título
Claro y descriptivo siguiendo Conventional Commits:

```
feat: Implementar autenticación de usuarios con JWT
fix: Corregir error en validación de email
docs: Actualizar guía de instalación
refactor: Simplificar lógica de cálculo de precios
```

#### 📝 Descripción

**Template recomendado:**

```markdown
## Descripción
Implementación del sistema de login con autenticación JWT.

## Tipo de cambio
- [x] Nueva funcionalidad (feature)
- [ ] Corrección de bug (fix)
- [ ] Refactorización (refactor)
- [ ] Documentación (docs)

## ¿Qué hace este PR?
- Añade endpoint `/api/auth/login`
- Implementa middleware de autenticación
- Genera y valida tokens JWT
- Añade tests de autenticación

## ¿Cómo se ha probado?
- [x] Tests unitarios
- [x] Tests de integración
- [x] Pruebas manuales en Postman

## Screenshots (si aplica)
![Login form](url-de-imagen)

## Checklist
- [x] Mi código sigue las guías de estilo del proyecto
- [x] He realizado una auto-revisión de mi código
- [x] He comentado áreas complejas del código
- [x] He actualizado la documentación
- [x] Mis cambios no generan nuevos warnings
- [x] He añadido tests que prueban mi funcionalidad
- [x] Tests nuevos y existentes pasan localmente

## Relacionado con
Closes #123
Related to #124
```

---

## 👀 3. Code Review

La revisión de código es fundamental para mantener la calidad y compartir conocimiento en el equipo.

### ¿Qué buscar al revisar código?

| Aspecto | Preguntas a hacer |
|---------|-------------------|
| **✅ Funcionalidad** | ¿El código hace lo que debe? ¿Cumple los requisitos? |
| **📖 Legibilidad** | ¿Es fácil de entender? ¿Los nombres son descriptivos? |
| **🔧 Mantenibilidad** | ¿Será fácil de modificar? ¿Sigue principios SOLID? |
| **⚡ Performance** | ¿Hay problemas de rendimiento obvios? |
| **🔒 Seguridad** | ¿Hay vulnerabilidades evidentes? ¿Valida inputs? |
| **🧪 Tests** | ¿Hay cobertura de tests adecuada? ¿Tests útiles? |
| **🎨 Estilo** | ¿Sigue las convenciones del proyecto? |
| **📚 Documentación** | ¿Está bien documentado lo necesario? |

### 💡 Consejos para hacer buenos code reviews

**Como revisor:**
- 🤝 Sé amable y constructivo
- 💬 Haz preguntas en lugar de dar órdenes
  - ❌ "Cambia esto"
  - ✅ "¿Has considerado usar X en lugar de Y?"
- 👏 Celebra el buen código
- 📚 Comparte conocimiento y recursos
- 🎯 Enfócate en lo importante (no bikeshedding)
- ⚡ Responde rápidamente (máximo 24h)
- 🔍 Prueba el código si es posible

**Como autor:**
- 📏 Mantén los PRs pequeños (<400 líneas)
- 📝 Proporciona contexto suficiente
- 💬 Responde a todos los comentarios
- 🙏 Agradece el feedback
- 🔄 Implementa cambios sugeridos rápidamente
- ❓ Pregunta si no entiendes algo

### Ejemplo de comentarios constructivos

```markdown
❌ Mal: "Esto está mal"
✅ Bien: "Este approach podría causar problemas de memoria con arrays grandes. 
         ¿Qué te parece usar un Map en su lugar? Aquí un ejemplo: [link]"

❌ Mal: "No me gusta este nombre"
✅ Bien: "El nombre `data` es muy genérico. ¿Podríamos llamarlo `userProfiles` 
         para que sea más descriptivo?"

👏 Genial: "¡Excelente uso de destructuring aquí! Hace el código mucho más legible."
```

---

### 📊 GitHub Projects

GitHub Projects es una herramienta integrada para gestionar el trabajo usando tableros Kanban o vistas de tabla.

#### Configuración recomendada para Scrum

**Tablero Kanban del Sprint:**

| 📋 To Do | 🔄 In Progress | 👀 In Review | ✅ Done |
|----------|----------------|--------------|---------|
| Sprint Backlog pendiente | En desarrollo activo | PR abierto | Completado y mergeado |

**Campos personalizados útiles:**

- **Sprint:** Sprint 1, Sprint 2, etc.
- **Story Points:** 1, 2, 3, 5, 8, 13
- **Prioridad:** Alta, Media, Baja
- **Tipo:** Feature, Bug, Docs, Refactor
- **Asignado a:** Miembro del equipo

#### Automatizaciones útiles

- 🔄 Mover issue a "In Progress" cuando se crea una rama
- 📝 Mover issue a "In Review" cuando se abre un PR
- ✅ Mover issue a "Done" cuando se cierra el PR
- 🎯 Asignar automáticamente a milestone actual
- 🏷️ Añadir label según tipo de issue

---

## 5. Ejercicios Prácticos

### 📝 Ejercicio 1: Configurar el repositorio del proyecto

**🎯 Objetivo:** Preparar el entorno de trabajo con GitHub  
**⏱️ Duración:** 30 minutos

**Tareas:**

1. Crear un repositorio en GitHub para el proyecto del equipo
2. Añadir todos los miembros del equipo como colaboradores
3. Configurar protección de la rama `main`:
   - Settings → Branches → Add rule
   - Branch name pattern: `main`
   - ✅ Require a pull request before merging
   - ✅ Require approvals (1 mínimo)
   - ✅ Require conversation resolution before merging
   - ✅ Require status checks to pass
4. Crear las labels recomendadas
5. Configurar un GitHub Project con vista Kanban

---

### 📝 Ejercicio 2: Simulación de Sprint Planning

**🎯 Objetivo:** Practicar la planificación de un sprint  
**⏱️ Duración:** 1-2 horas

**Escenario:**  
Vais a desarrollar una aplicación de gestión de tareas (ToDo App)

**Tareas:**

1. **Definir el Sprint Goal:**  
   *Ejemplo: "Implementar CRUD básico de tareas"*

2. **Crear 5-8 User Stories como GitHub Issues:**
   ```
   - Como usuario quiero registrarme en la app
   - Como usuario quiero crear una nueva tarea
   - Como usuario quiero ver mi lista de tareas
   - Como usuario quiero marcar tarea como completada
   - Como usuario quiero eliminar una tarea
   ```

3. **Para cada issue:**
   - Usar el template de User Story
   - Añadir labels apropiadas
   - Estimar story points (fibonacci: 1, 2, 3, 5, 8)
   - Definir criterios de aceptación
   - Añadir al Milestone del Sprint 1

4. **Asignar issues a los miembros del equipo**

5. **Documentar decisiones:**
   - Crear un issue de "Sprint Planning - Sprint 1"
   - Documentar Sprint Goal, velocity esperada, acuerdos

---

### 📝 Ejercicio 3: GitHub Flow en práctica

**🎯 Objetivo:** Dominar el flujo de trabajo con ramas y PRs  
**⏱️ Duración:** 2-3 horas

**Pasos:**

1. **Cada miembro toma una issue del Sprint Backlog**
   - Asignarse la issue
   - Moverla a "In Progress" en el Project

2. **Crear una rama feature:**
   ```bash
   git checkout -b feature/crear-tarea
   ```

3. **Desarrollar la funcionalidad:**
   - Realizar commits descriptivos
   - Usar Conventional Commits:
     ```
     feat: añadir formulario de nueva tarea
     feat: implementar POST /api/tasks
     test: añadir tests para creación de tareas
     docs: actualizar API docs con endpoint de tareas
     ```

4. **Abrir un Pull Request:**
   - Usar el template
   - Referenciar la issue: `Closes #5`
   - Añadir screenshots si hay cambios visuales

5. **Code Review:**
   - Otro compañero revisa el código
   - Deja al menos 2 comentarios constructivos
   - Aprueba si todo está correcto

6. **Merge del PR:**
   - Verificar que el CI pasa
   - Hacer squash merge
   - Eliminar la rama

7. **Verificar:**
   - La issue se cerró automáticamente
   - Se movió a "Done" en el Project

---

### 📝 Ejercicio 4: Daily Scrum

**🎯 Objetivo:** Establecer el hábito de sincronización diaria  
**⏱️ Duración:** 15 minutos diarios durante una semana

**Formato:**

Cada día a la misma hora (ej: 9:00), reunión de 15 min máximo:

1. **Cada miembro responde:**
   - ¿Qué hice ayer?
   - ¿Qué haré hoy?
   - ¿Algún impedimento?

2. **El Scrum Master:**
   - Facilita la reunión (timekeeper)
   - Actualiza el tablero Kanban si es necesario
   - Anota impedimentos para resolverlos después

3. **Documentación:**
   - Crear un documento compartido
   - Anotar impedimentos identificados
   - Tracking de resolución de impedimentos

**Al final de la semana:**
- Reflexionar: ¿Fue útil?
- ¿Qué mejoraría la daily?
- Ajustar formato si es necesario

---

### 📝 Ejercicio 5: Sprint Review y Retrospective

**🎯 Objetivo:** Cerrar el sprint con aprendizajes  
**⏱️ Duración:** 2-3 horas

#### Parte 1: Sprint Review (1-1.5h)

1. **Preparar demo:**
   - Cada miembro prepara su parte
   - Probar en entorno de staging
   - Preparar datos de prueba

2. **Realizar la demo:**
   - Mostrar funcionalidades completadas
   - Demostrar en vivo (no slides)
   - Invitar al Product Owner (profesor)

3. **Recoger feedback:**
   - Anotar comentarios del PO
   - Discutir próximos pasos
   - Actualizar Product Backlog según feedback

4. **Métricas del sprint:**
   - Story points completados vs planificados
   - Velocity del equipo
   - Issues cerradas

#### Parte 2: Sprint Retrospective (1h)

1. **Formato "Estrella de mar":**

   Crear un documento con 5 columnas:
   
   | ⭐ Empezar | 📈 Más | ➡️ Seguir | 📉 Menos | 🛑 Dejar |
   |-----------|--------|----------|---------|---------|
   | | | | | |

2. **Cada miembro añade post-its/comentarios**
   (5-10 minutos en silencio)

3. **Agrupar y discutir**
   (20 minutos)

4. **Votar prioridades**
   (5 minutos)

5. **Definir 1-3 acciones concretas:**
   ```markdown
   ## Acciones de Mejora - Sprint 2
   
   1. **Hacer más pair programming en tareas complejas**
      - Responsable: Todo el equipo
      - Cómo medirlo: Al menos 50% de tareas grandes en pair
   
   2. **Mejorar descripciones de PRs**
      - Responsable: Scrum Master revisa
      - Cómo medirlo: Todos los PRs usan el template completo
   
   3. **Reducir scope de PRs**
      - Responsable: Todo el equipo
      - Cómo medirlo: Máximo 300 líneas por PR
   ```

6. **Documentar:**
   - Crear issue "Retrospectiva Sprint 1"
   - Listar acciones de mejora
   - Asignar al Milestone del Sprint 2

---

## 📚 Recursos Adicionales

### Documentación Oficial
- [Scrum Guide (PDF español)](https://scrumguides.org/docs/scrumguide/v2020/2020-Scrum-Guide-Spanish-European.pdf)
- [GitHub Flow](https://docs.github.com/es/get-started/quickstart/github-flow)
- [GitHub Actions Documentation](https://docs.github.com/es/actions)

### Artículos y Guías
- [Atlassian: Scrum](https://www.atlassian.com/es/agile/scrum)
- [Atlassian: Git Flow vs GitHub Flow](https://www.atlassian.com/git/tutorials/comparing-workflows)
- [Conventional Commits](https://www.conventionalcommits.org/es/)

### Herramientas
- [GitHub Projects](https://github.com/features/project-management)
- [GitHub Issues](https://github.com/features/issues)
- [Scrum.org Resources](https://www.scrum.org/resources)

---

[⬅️ Volver al inicio](README.md) | [➡️ Siguiente: Bloque 2 - Ingeniería de Requisitos](bloque2.md)
