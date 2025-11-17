# 📗 Bloque 2: Ingeniería de Requisitos

**Objetivo:** Dominar el arte de capturar, analizar y documentar las necesidades del cliente

---

## 📑 Índice de Contenidos

1. [Introducción a la Ingeniería de Requisitos](#1-introducción-a-la-ingeniería-de-requisitos)
2. [Levantamiento de Requisitos](#2-levantamiento-de-requisitos)
   - [Técnicas de Elicitación](#-técnicas-de-elicitación)
   - [Entrevistas Efectivas](#-entrevistas-efectivas)
   - [Análisis de Partes Interesadas](#-análisis-de-partes-interesadas)
3. [Documentación Técnica](#3-documentación-técnica)
   - [Diagramas UML Esenciales](#-diagramas-uml-esenciales)
   - [Arquitectura de Solución](#-arquitectura-de-solución)
4. [Priorización y Estimación](#4-priorización-y-estimación)
5. [Ejercicios Prácticos](#5-ejercicios-prácticos)

---

## 1. Introducción a la Ingeniería de Requisitos

La ingeniería de requisitos es el proceso de **descubrir, documentar y mantener** los requisitos de un sistema software. Es la base para construir el producto correcto.

### ¿Por qué es importante?

> 💡 **El 70% de los proyectos software fallan por problemas en los requisitos**

Problemas comunes:
- ❌ Requisitos ambiguos o incompletos
- ❌ No entender las necesidades reales del usuario
- ❌ Cambios constantes sin gestión
- ❌ Falta de comunicación con partes interesadas
- ❌ Requisitos no verificables

Beneficios de hacerlo bien:
- ✅ Menos cambios costosos durante el desarrollo
- ✅ Mayor satisfacción del cliente
- ✅ Mejor estimación de tiempos y costos
- ✅ Equipo alineado con los objetivos
- ✅ Producto que realmente resuelve el problema

### Tipos de Requisitos

| Tipo | Descripción | Ejemplo |
|------|-------------|---------|
| **Funcionales** | Qué debe hacer el sistema | "El sistema debe permitir login con email y contraseña" |
| **No funcionales** | Cómo debe comportarse | "El login debe responder en <2 segundos" |
| **De negocio** | Objetivos de la organización | "Aumentar conversión de registro en 20%" |
| **De usuario** | Necesidades del usuario final | "Como usuario quiero recuperar mi contraseña" |
| **Del sistema** | Requisitos técnicos detallados | "Usar JWT para autenticación con expiración de 24h" |

---

## 2. Levantamiento de Requisitos

El levantamiento (o elicitación) de requisitos es el proceso de **descubrir** qué necesita realmente el cliente y los usuarios.

---

## 🎯 Técnicas de Elicitación

### 1. Entrevistas

**Cuándo usar:** Con partes interesadas clave, expertos del dominio

**Tipos:**
- **Estructuradas:** Preguntas predefinidas, formato formal
- **Semi-estructuradas:** Guión flexible, permite exploración
- **No estructuradas:** Conversación abierta, exploratoria

**Ventajas:**
- ✅ Información detallada y profunda
- ✅ Construye relación con las partes interesadas
- ✅ Permite aclarar dudas inmediatamente

**Desventajas:**
- ❌ Consume mucho tiempo
- ❌ Puede haber sesgos del entrevistador
- ❌ Solo captura la visión de pocos

---

### 2. Cuestionarios y Encuestas

**Cuándo usar:** Con muchos usuarios, datos cuantitativos

**Tipos de preguntas:**
- **Cerradas:** Sí/No, múltiple opción
- **Escala Likert:** Del 1 al 5
- **Abiertas:** Respuesta libre

**Ventajas:**
- ✅ Rápido de distribuir
- ✅ Muchas respuestas
- ✅ Datos cuantificables

**Desventajas:**
- ❌ Respuestas superficiales
- ❌ Baja tasa de respuesta
- ❌ No permite profundizar

---

### 3. Observación

**Cuándo usar:** Para entender el flujo de trabajo actual

**Tipos:**
- **Directa:** Observar al usuario trabajando
- **Etnográfica:** Inmersión en el entorno
- **Análisis de tareas:** Documentar paso a paso

**Ventajas:**
- ✅ Captura comportamiento real (no declarado)
- ✅ Identifica ineficiencias actuales
- ✅ Descubre necesidades no verbalizadas

---

### 4. Workshops y Brainstorming

**Cuándo usar:** Para generar ideas, alinear visiones

**Formato:**
- Reunir partes interesadas clave (5-10 personas)
- Facilitador neutral
- Técnicas: Post-its, votación, agrupación

**Ventajas:**
- ✅ Colaboración y creatividad
- ✅ Alineación de equipo
- ✅ Muchas ideas en poco tiempo

---

### 5. Análisis de Documentación

**Qué analizar:**
- Documentación existente del sistema actual
- Procesos de negocio
- Reportes y métricas
- Competencia

**Ventajas:**
- ✅ No requiere disponibilidad de personas
- ✅ Información ya validada
- ✅ Contexto histórico

---

### 6. Prototipos

**Tipos:**
- **Baja fidelidad:** Wireframes, sketches
- **Alta fidelidad:** Mockups interactivos
- **MVP:** Producto mínimo funcional

**Ventajas:**
- ✅ Feedback visual y concreto
- ✅ Valida ideas rápidamente
- ✅ Reduce malentendidos

---

## 🎤 Entrevistas Efectivas

### Preparación

**Antes de la entrevista:**

1. **Investigar:**
   - Perfil del entrevistado
   - Dominio del negocio
   - Sistema actual (si existe)

2. **Preparar preguntas:**
   - Empezar general → específico
   - Preguntas abiertas
   - Escenarios concretos

3. **Logística:**
   - Agendar con tiempo suficiente (1-2h)
   - Lugar cómodo y sin interrupciones
   - Herramientas: grabadora, notas

### Guía de Preguntas

#### 🔵 Contexto y Objetivos

```
- ¿Cuál es el objetivo principal del proyecto?
- ¿Qué problema estamos intentando resolver?
- ¿Quiénes son los usuarios finales?
- ¿Cuál es el contexto de uso?
- ¿Qué pasa actualmente sin este sistema?
```

#### 🟢 Funcionalidades

```
- ¿Qué tareas realizan los usuarios?
- ¿Cuál es el flujo de trabajo típico?
- ¿Qué información necesitan los usuarios?
- ¿Qué decisiones deben tomar?
- ¿Qué acciones deben poder ejecutar?
```

#### 🟡 Restricciones y No Funcionales

```
- ¿Cuántos usuarios concurrentes esperamos?
- ¿Hay requisitos de rendimiento?
- ¿Existen regulaciones o normativas?
- ¿Hay sistemas con los que debemos integrarnos?
- ¿Cuál es el presupuesto y timeline?
```

#### 🔴 Prioridades

```
- ¿Qué es imprescindible para la primera versión?
- ¿Qué sería nice-to-have?
- ¿Qué podemos dejar para después?
- ¿Cuál es el criterio de éxito?
```

### Durante la Entrevista

**✅ HACER:**
- Escuchar activamente (80% escuchar, 20% hablar)
- Hacer preguntas de seguimiento
- Parafrasear para confirmar entendimiento
- Tomar notas de palabras clave
- Pedir ejemplos concretos
- Ser neutral y objetivo

**❌ NO HACER:**
- Interrumpir
- Proponer soluciones prematuramente
- Juzgar o criticar
- Usar jerga técnica
- Asumir que entiendes
- Hacer preguntas guiadas

### Técnicas Efectivas

**Técnica de los 5 Por Qués:**
```
Usuario: "Necesito un botón de exportar"
    ↓
¿Por qué? → "Para compartir datos con mi equipo"
    ↓
¿Por qué? → "Porque necesitan los datos para sus reportes"
    ↓
¿Por qué? → "Porque toman decisiones basadas en estos datos"
    ↓
¿Por qué? → "Porque necesitamos optimizar el proceso"
    ↓
¿Por qué? → "Porque perdemos mucho tiempo en coordinación"

💡 Necesidad real: Sistema colaborativo en tiempo real
```

**Preguntas STAR (Situación, Tarea, Acción, Resultado):**
```
- Situación: "Cuéntame de la última vez que..."
- Tarea: "¿Qué intentabas lograr?"
- Acción: "¿Qué hiciste específicamente?"
- Resultado: "¿Qué pasó?"
```

### Después de la Entrevista

1. **Documentar inmediatamente** (en las primeras 24h)
2. **Organizar notas** en categorías
3. **Identificar patrones** entre entrevistas
4. **Validar entendimiento** con el entrevistado
5. **Compartir con el equipo**

---

## 👥 Análisis de Partes Interesadas

Las partes interesadas son todas las personas que tienen interés o son afectadas por el proyecto.

### Identificar Partes Interesadas

**Tipos comunes:**
- 🎯 **Usuario final:** Quien usa el sistema
- 👔 **Cliente/Sponsor:** Quien paga
- 🏢 **Product Owner:** Define el producto
- 👨‍💼 **Gerentes:** Aprueban decisiones
- 🔧 **Equipo técnico:** Desarrolla
- 📊 **Analistas:** Usan datos del sistema
- 🔐 **Compliance:** Requisitos legales

### Matriz de Poder/Interés

```
        Alta Influencia
              |
    Gestionar | Mantener
    de Cerca  | Satisfechos
    ----------|------------
    Mantener  | Mantener
    Informados| Monitoreados
              |
        Baja Influencia
         
         Alto Interés → Bajo Interés
```

### Template de Parte Interesada

```markdown
## Parte Interesada: María García

**Rol:** Gerente de Ventas
**Interés:** Alto - Usuario principal
**Influencia:** Alta - Aprueba presupuesto
**Expectativas:**
- Sistema rápido y fácil de usar
- Reportes de ventas en tiempo real
- Acceso móvil

**Cómo involucrar:**
- Entrevista semanal
- Demo cada sprint
- Feedback en User Stories

**Riesgos:**
- Poco tiempo disponible
- Resistencia al cambio
```

---

## 3. Documentación Técnica

Aunque Agile valora "software funcionando sobre documentación extensiva", cierta documentación es esencial.

---

## 📊 Diagramas UML Esenciales

### 1. Diagrama de Casos de Uso

**Cuándo:** Visión general de funcionalidades y actores

```
        ┌────────────────────────────────┐
        │     Sistema E-commerce         │
        │                                │
        │   ┌──────────────────┐        │
        │   │ Buscar Productos │◄───────┼─────● Cliente
        │   └──────────────────┘        │
        │   ┌──────────────────┐        │
        │   │  Añadir Carrito  │◄───────┼─────●
        │   └──────────────────┘        │
        │   ┌──────────────────┐        │
        │   │ Realizar Compra  │◄───────┼─────●
        │   └──────────────────┘        │
        │   ┌──────────────────┐        │
        │   │ Gestionar Pedidos│◄───────┼─────● Admin
        │   └──────────────────┘        │
        │   ┌──────────────────┐        │
        │   │Gestionar Productos│◄──────┼─────●
        │   └──────────────────┘        │
        └────────────────────────────────┘
```

---

### 2. Diagrama de Clases

**Cuándo:** Diseño de la estructura de datos y relaciones

```
┌─────────────────────┐
│       User          │
├─────────────────────┤
│ - id: UUID          │
│ - email: string     │
│ - password: string  │
│ - createdAt: Date   │
├─────────────────────┤
│ + register()        │
│ + login()           │
│ + updateProfile()   │
└──────────┬──────────┘
           │ 1
           │
           │ 0..*
┌──────────▼──────────┐
│       Order         │
├─────────────────────┤
│ - id: UUID          │
│ - userId: UUID      │
│ - total: number     │
│ - status: OrderStatus│
│ - createdAt: Date   │
├─────────────────────┤
│ + create()          │
│ + addItem()         │
│ + calculateTotal()  │
│ + updateStatus()    │
└──────────┬──────────┘
           │ 1
           │
           │ 1..*
┌──────────▼──────────┐
│     OrderItem       │
├─────────────────────┤
│ - id: UUID          │
│ - orderId: UUID     │
│ - productId: UUID   │
│ - quantity: number  │
│ - price: number     │
└─────────────────────┘
```

---

### 3. Diagrama de Secuencia

**Cuándo:** Flujos complejos con múltiples componentes

```
Cliente    Frontend    API Gateway    Auth Service    Database
  │           │             │               │             │
  │─login()──>│             │               │             │
  │           │─POST────────>│               │             │
  │           │ /auth/login │               │             │
  │           │             │─validate()───>│             │
  │           │             │               │─query()────>│
  │           │             │               │             │
  │           │             │               │<──user─────│
  │           │             │<──JWT token──│             │
  │           │<─200 OK─────│               │             │
  │<──token───│             │               │             │
  │           │             │               │             │
  │─getData()->│             │               │             │
  │           │─GET─────────>│               │             │
  │           │ /api/data   │               │             │
  │           │ Header:JWT  │               │             │
  │           │             │─verify JWT───>│             │
  │           │             │<──valid──────│             │
  │           │             │               │             │
  │           │             │─────query()───────────────>│
  │           │             │<─────data()────────────────│
  │           │<─200 OK─────│               │             │
  │<──data────│             │               │             │
```

---

### 4. Diagrama de Estados

**Cuándo:** Entidades con ciclo de vida complejo

```
             ┌────────────┐
      ┌──────│   Draft    │
      │      └──────┬─────┘
      │             │ submit()
      │      ┌──────▼─────┐
      │      │  Pending   │
      │      │  Review    │
      │      └──┬────┬────┘
      │         │    │
      │ reject()│    │approve()
      │         │    │
      │   ┌─────▼──┐ │  ┌─────────┐
      └───│Rejected│ └──│Approved │
          └────────┘    └────┬────┘
                             │ publish()
                        ┌────▼────┐
                        │Published│
                        └────┬────┘
                             │ archive()
                        ┌────▼────┐
                        │Archived │
                        └─────────┘
```

---

## 🏗️ Arquitectura de Solución

### Diagrama de Arquitectura

```
┌─────────────────────────────────────────────────────┐
│                    Frontend                         │
│          React + TypeScript + Tailwind              │
└────────────────────┬────────────────────────────────┘
                     │ HTTPS/REST
                     │
┌────────────────────▼────────────────────────────────┐
│                  API Gateway                        │
│              (Rate Limiting, CORS)                  │
└───────┬──────────────────────────────┬──────────────┘
        │                              │
        │                              │
┌───────▼────────┐           ┌─────────▼──────────┐
│  Auth Service  │           │  Product Service   │
│   (Node.js)    │           │    (Node.js)       │
│                │           │                    │
│  - Login       │           │  - CRUD Products   │
│  - Register    │           │  - Search          │
│  - JWT         │           │  - Categories      │
└───────┬────────┘           └─────────┬──────────┘
        │                              │
        │                              │
┌───────▼──────────────────────────────▼──────────┐
│            PostgreSQL Database                  │
│                                                  │
│  ┌────────┐  ┌──────────┐  ┌──────────────┐   │
│  │ users  │  │ products │  │ orders       │   │
│  └────────┘  └──────────┘  └──────────────┘   │
└──────────────────────────────────────────────────┘

┌──────────────────────────────────────────────────┐
│              Redis Cache                         │
│         (Sessions, Rate Limiting)                │
└──────────────────────────────────────────────────┘
```

### Decisiones de Arquitectura (ADR)

```markdown
# ADR-001: Usar JWT para Autenticación

## Estado
Aceptado

## Contexto
Necesitamos un mecanismo de autenticación que:
- Sea stateless (escalable)
- Funcione con SPA (Single Page Application)
- Permita autenticación en múltiples servicios

## Decisión
Utilizaremos JSON Web Tokens (JWT) para autenticación.

## Consecuencias

### Positivas
- ✅ Stateless: No necesita almacenar sesiones en servidor
- ✅ Escalable: Fácil balanceo de carga
- ✅ Descentralizado: Cada servicio puede verificar el token
- ✅ Estándar: Ampliamente soportado

### Negativas
- ❌ No se puede revocar fácilmente (hasta que expire)
- ❌ Tamaño mayor que session ID
- ❌ Información visible (aunque firmada)

### Mitigación
- Usar tiempo de expiración corto (24h)
- Implementar refresh tokens
- Blacklist para tokens revocados críticos
```

---

## 4. Priorización y Estimación

### Técnicas de Priorización

#### MoSCoW

Clasifica requisitos en 4 categorías para definir el alcance del proyecto:

| Categoría | Significado | % Recomendado |
|-----------|-------------|---------------|
| **M**ust have | Crítico, sin esto no funciona | 60% |
| **S**hould have | Importante, pero no crítico | 20% |
| **C**ould have | Deseable si hay tiempo | 10% |
| **W**on't have (now) | Fuera del scope actual | 10% |

**Ejemplo aplicado:**
- **MUST HAVE:** Login, CRUD de productos, Carrito, Checkout básico
- **SHOULD HAVE:** Búsqueda y filtros, Recuperar contraseña
- **COULD HAVE:** Wishlist, Reviews de productos
- **WON'T HAVE:** Login social, Programa de puntos, Chat en vivo

#### Matriz de Valor/Esfuerzo

Herramienta visual para priorizar basándose en dos ejes:

```
        Alto Valor
            │
   Hacer    │  Hacer
   Primero  │  Después
────────────┼────────────
   Tal vez  │  Evitar
            │
        Bajo Valor
            
   Bajo ← Esfuerzo → Alto
```

### Técnicas de Estimación

#### Planning Poker

Técnica colaborativa de estimación usando cartas con la secuencia de Fibonacci:
- **Valores:** 0, ½, 1, 2, 3, 5, 8, 13, 20, 40, 100, ∞, ?
- **Story Points = Complejidad + Esfuerzo + Incertidumbre**

**Referencia rápida:**
- 1-2 puntos: Cambios simples
- 3-5 puntos: Funcionalidad estándar
- 8-13 puntos: Feature compleja
- 20+: Dividir en historias más pequeñas

#### Velocity

Mide la capacidad del equipo para planificar sprints:

```
Velocity = Story Points completados / Sprint
```

Ejemplo: Si tu equipo completa 20 puntos/sprint y el backlog tiene 180 puntos, necesitarás aproximadamente 9 sprints (4.5 meses con sprints de 2 semanas)

---

## 5. Ejercicios Prácticos

### 📝 Ejercicio 1: Entrevista a Parte Interesada

**🎯 Objetivo:** Practicar técnicas de elicitación  
**⏱️ Duración:** 1 hora

**Escenario:**  
Eres contratado para desarrollar un sistema de reservas para un gimnasio local.

**Tareas:**

1. **Preparar entrevista** (15 min):
   - Investigar sobre gimnasios
   - Preparar 15-20 preguntas
   - Organizar por categorías

2. **Rol-playing** (30 min):
   - Un compañero hace de "Dueño del gimnasio"
   - Realizar la entrevista
   - Tomar notas

3. **Documentar** (15 min):
   - Organizar hallazgos
   - Identificar requisitos funcionales y no funcionales
   - Lista de preguntas de seguimiento

---

### 📝 Ejercicio 2: Diagramas UML

**🎯 Objetivo:** Documentar diseño técnico  
**⏱️ Duración:** 2 horas

**Proyecto:** Sistema de reservas de hotel

**Crear:**

1. **Diagrama de Casos de Uso**
   - Identificar actores (3-4)
   - Casos de uso principales (8-10)
   - Relaciones include/extend

2. **Diagrama de Clases**
   - Entidades principales (5-7)
   - Atributos y métodos
   - Relaciones y cardinalidades

3. **Diagrama de Secuencia**
   - Flujo: "Reservar habitación"
   - Incluir: Frontend, API, DB

4. **Diagrama de Estados**
   - Entidad: Reserva
   - Estados y transiciones

**Herramientas sugeridas:**
- draw.io
- PlantUML
- Lucidchart
- Mermaid

---

### 📝 Ejercicio 3: Priorización con MoSCoW

**🎯 Objetivo:** Practicar priorización de requisitos  
**⏱️ Duración:** 1 hora

**Proyecto:** Red social para profesionales

**Lista de 20 funcionalidades:**
```
1. Crear perfil
2. Login/registro
3. Publicar post
4. Comentar posts
5. Dar like
6. Compartir posts
7. Mensajería privada
8. Búsqueda de usuarios
9. Notificaciones
10. Feed personalizado
11. Grupos temáticos
12. Eventos
13. Ofertas de empleo
14. Dark mode
15. Estadísticas de perfil
16. Recomendaciones IA
17. Video posts
18. Stories
19. Live streaming
20. Monetización
```

**Tareas:**

1. Clasificar cada funcionalidad en MoSCoW
2. Justificar decisiones
3. Validar que MUST < 60%
4. Crear roadmap de 3 releases
5. Presentar y defender ante el equipo

---

## 📚 Recursos Adicionales

### Libros Recomendados
- 📗 "Software Requirements" - Karl Wiegers
- 📘 "Agile Estimating and Planning" - Mike Cohn

### Herramientas
- **Diagramas:** draw.io, PlantUML, Lucidchart
- **Prototipos:** Figma, Sketch, Adobe XD
- **Documentación:** Notion, Confluence, GitBook
- **Entrevistas:** Miro, Mural (para workshops)

### Templates
- [ADR Template](https://github.com/joelparkerhenderson/architecture-decision-record)
- [Interview Guide Template](https://github.com/interview-guide)

---

## 🎯 Checklist de Competencias

Al finalizar este bloque, deberías ser capaz de:

- [ ] Aplicar técnicas de elicitación de requisitos
- [ ] Realizar entrevistas efectivas a partes interesadas
- [ ] Identificar y analizar partes interesadas
- [ ] Crear diagramas UML (Casos de Uso, Clases, Secuencia, Estados)
- [ ] Documentar decisiones de arquitectura (ADR)
- [ ] Aplicar técnicas de priorización (MoSCoW, Valor/Esfuerzo)
- [ ] Estimar con Planning Poker y Story Points
- [ ] Calcular velocity del equipo

---

[⬅️ Bloque 1: Metodologías Ágiles](bloque1.md) | [➡️ Bloque 3: Desarrollo con IA](bloque3.md)
