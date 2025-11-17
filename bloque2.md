# 📗 Bloque 2: Ingeniería de Requisitos

**Objetivo:** Dominar el arte de capturar, analizar y documentar las necesidades del cliente

---

## 📑 Índice de Contenidos

1. [Introducción a la Ingeniería de Requisitos](#1-introducción-a-la-ingeniería-de-requisitos)
2. [Levantamiento de Requisitos](#2-levantamiento-de-requisitos)
   - [Técnicas de Elicitación](#-técnicas-de-elicitación)
   - [Entrevistas Efectivas](#-entrevistas-efectivas)
   - [Análisis de Stakeholders](#-análisis-de-stakeholders)
3. [User Stories y Épicas](#3-user-stories-y-épicas)
   - [Formato de User Stories](#-formato-de-user-stories)
   - [Criterios de Aceptación](#-criterios-de-aceptación)
   - [Story Mapping](#-story-mapping)
4. [Documentación Técnica](#4-documentación-técnica)
   - [Diagramas UML Esenciales](#-diagramas-uml-esenciales)
   - [Arquitectura de Solución](#-arquitectura-de-solución)
   - [Definition of Done](#-definition-of-done-dod)
5. [Priorización y Estimación](#5-priorización-y-estimación)
6. [Ejercicios Prácticos](#6-ejercicios-prácticos)

---

## 1. Introducción a la Ingeniería de Requisitos

La ingeniería de requisitos es el proceso de **descubrir, documentar y mantener** los requisitos de un sistema software. Es la base para construir el producto correcto.

### ¿Por qué es importante?

> 💡 **El 70% de los proyectos software fallan por problemas en los requisitos**

Problemas comunes:
- ❌ Requisitos ambiguos o incompletos
- ❌ No entender las necesidades reales del usuario
- ❌ Cambios constantes sin gestión
- ❌ Falta de comunicación con stakeholders
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

**Cuándo usar:** Con stakeholders clave, expertos del dominio

**Tipos:**
- **Estructuradas:** Preguntas predefinidas, formato formal
- **Semi-estructuradas:** Guión flexible, permite exploración
- **No estructuradas:** Conversación abierta, exploratoria

**Ventajas:**
- ✅ Información detallada y profunda
- ✅ Construye relación con stakeholder
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
- Reunir stakeholders clave (5-10 personas)
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

## 👥 Análisis de Stakeholders

Los stakeholders son todas las personas que tienen interés o son afectadas por el proyecto.

### Identificar Stakeholders

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

### Template de Stakeholder

```markdown
## Stakeholder: María García

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

## 3. User Stories y Épicas

Las User Stories son la forma ágil de capturar requisitos desde la perspectiva del usuario.

---

## 📝 Formato de User Stories

### Estructura Base

```
Como [tipo de usuario]
Quiero [funcionalidad/objetivo]
Para [beneficio/valor]
```

### Ejemplos Buenos vs Malos

#### ❌ Malo

```
Como usuario
Quiero un login
Para entrar al sistema
```

*Problemas:*
- Usuario muy genérico
- No explica el valor real
- Falta detalle

#### ✅ Bueno

```
Como cliente registrado
Quiero iniciar sesión con mi email y contraseña
Para acceder a mi historial de pedidos y realizar nuevas compras de forma rápida
```

*Por qué es mejor:*
- Usuario específico
- Funcionalidad clara
- Valor de negocio explícito

### Componentes Completos de una User Story

```markdown
## US-001: Login de Cliente

### Historia
Como cliente registrado
Quiero iniciar sesión con mi email y contraseña
Para acceder a mi historial de pedidos y realizar compras rápidamente

### Criterios de Aceptación
- [ ] El formulario incluye campos de email y contraseña
- [ ] Se valida formato de email
- [ ] Contraseña se muestra oculta con opción de ver
- [ ] Mensaje de error si credenciales incorrectas
- [ ] Redirección a dashboard tras login exitoso
- [ ] Opción "Recordarme" para mantener sesión
- [ ] Link a "¿Olvidaste tu contraseña?"

### Notas Técnicas
- Endpoint: POST /api/auth/login
- Autenticación: JWT con expiración de 7 días
- Rate limiting: 5 intentos por minuto
- Hash: bcrypt para contraseñas

### Definition of Done
- [ ] Código implementado y revisado
- [ ] Tests unitarios (>80% cobertura)
- [ ] Tests E2E del flujo de login
- [ ] Documentación API actualizada
- [ ] Probado en Chrome, Firefox, Safari
- [ ] Responsive en móvil
- [ ] Aprobado por PO

### Estimación
Story Points: 5
Tiempo estimado: 1-2 días

### Dependencias
- US-000: Sistema de registro debe estar completo

### Enlaces
- Diseño en Figma: [link]
- Épica padre: EP-01 Autenticación
```

---

## ✅ Criterios de Aceptación

Los criterios de aceptación definen cuándo una User Story está completa. Deben ser:

- **Específicos:** Sin ambigüedad
- **Medibles:** Se puede verificar
- **Alcanzables:** Técnicamente factible
- **Relevantes:** Aportan valor
- **Testeables:** Se pueden probar

### Formatos

#### 1. Checklist (Más común)

```markdown
## Criterios de Aceptación

- [ ] Usuario puede subir imagen de perfil
- [ ] Formatos aceptados: JPG, PNG, máx 5MB
- [ ] Vista previa antes de guardar
- [ ] Imagen se redimensiona automáticamente a 200x200px
- [ ] Mensaje de confirmación al guardar
```

#### 2. Escenarios Given-When-Then (BDD)

```gherkin
Escenario 1: Subida exitosa de imagen
  Dado que soy un usuario autenticado
  Y estoy en mi página de perfil
  Cuando selecciono una imagen JPG de 2MB
  Y hago clic en "Guardar"
  Entonces la imagen se sube exitosamente
  Y veo un mensaje "Foto actualizada"
  Y mi foto de perfil se actualiza

Escenario 2: Archivo demasiado grande
  Dado que soy un usuario autenticado
  Cuando intento subir una imagen de 10MB
  Entonces veo el error "Archivo muy grande (máx 5MB)"
  Y la imagen no se sube

Escenario 3: Formato no soportado
  Dado que soy un usuario autenticado
  Cuando intento subir un archivo PDF
  Entonces veo el error "Formato no soportado (usa JPG o PNG)"
  Y el archivo no se sube
```

### Validación de Criterios: Técnica SMART

| Letra | Significado | Pregunta |
|-------|-------------|----------|
| **S** | Specific (Específico) | ¿Es claro y sin ambigüedad? |
| **M** | Measurable (Medible) | ¿Podemos verificarlo objetivamente? |
| **A** | Achievable (Alcanzable) | ¿Es técnicamente factible? |
| **R** | Relevant (Relevante) | ¿Aporta valor al usuario? |
| **T** | Testable (Testeable) | ¿Podemos escribir un test para ello? |

---

## 🗺️ Story Mapping

Story Mapping es una técnica para organizar User Stories visualmente y priorizar el desarrollo.

### Estructura de un Story Map

```
[Actividad 1]     [Actividad 2]     [Actividad 3]
     |                  |                  |
[User Task 1.1]   [User Task 2.1]   [User Task 3.1]
[User Task 1.2]   [User Task 2.2]   [User Task 3.2]
[User Task 1.3]   [User Task 2.3]   [User Task 3.3]
     ↓                  ↓                  ↓
─────────────────────────────────────────────────── MVP (Release 1)
[Story 1.1]       [Story 2.1]       [Story 3.1]
[Story 1.2]       [Story 2.2]       
─────────────────────────────────────────────────── Release 2
[Story 1.3]       [Story 2.3]       [Story 3.2]
[Story 1.4]                         [Story 3.3]
```

### Ejemplo: E-commerce

```
[Descubrir]    [Comprar]      [Recibir]      [Soporte]
     |             |              |              |
[Buscar]      [Añadir al    [Elegir envío] [Contactar]
              carrito]
[Filtrar]     [Ver carrito] [Pagar]        [Ver FAQ]
[Ver detalle] [Checkout]    [Confirmar]    [Devoluciones]

═══════════════════════════════════════════════════ MVP
[US-01]       [US-05]        [US-10]
Búsqueda      Añadir         Checkout
básica        producto       básico
              
[US-02]       [US-06]        [US-11]
Ver           Ver carrito    Paypal
producto                     
              [US-07]        
              Actualizar
              cantidad

═══════════════════════════════════════════════════ v2.0
[US-03]       [US-08]        [US-12]        [US-15]
Filtros       Cupones        Múltiples      Chat
avanzados     descuento      direcciones    soporte

[US-04]       [US-09]        [US-13]        [US-16]
Favoritos     Wish list      Tarjeta        Email
                             crédito        tracking
```

### Pasos para crear un Story Map

1. **Identificar el User Journey** (de izquierda a derecha)
2. **Desglosar en actividades principales**
3. **Añadir tareas de usuario bajo cada actividad**
4. **Escribir User Stories específicas**
5. **Priorizar verticalmente** (arriba = más importante)
6. **Dibujar líneas de releases**
7. **Validar con stakeholders**

---

## 📐 Épicas

Las Épicas son User Stories grandes que se descomponen en múltiples historias más pequeñas.

### Estructura de una Épica

```markdown
# EP-01: Sistema de Autenticación

## Descripción
Implementar un sistema completo de autenticación y gestión de usuarios que 
permita registro, login, recuperación de contraseña y gestión de perfil.

## Valor de Negocio
- Permitir identificación de usuarios
- Base para personalización
- Requisito para funcionalidades avanzadas

## Objetivos Medibles
- 80% de usuarios se registran exitosamente en primer intento
- Login en <2 segundos
- <5% solicitudes de recuperación de contraseña

## User Stories Incluidas
- [ ] US-001: Registro de usuario (5 pts)
- [ ] US-002: Login con email/contraseña (5 pts)
- [ ] US-003: Recuperar contraseña (3 pts)
- [ ] US-004: Verificación de email (3 pts)
- [ ] US-005: Editar perfil (5 pts)
- [ ] US-006: Cambiar contraseña (2 pts)
- [ ] US-007: Login con Google (8 pts)
- [ ] US-008: Login con GitHub (8 pts)

**Total:** 39 Story Points

## Sprints Planificados
- Sprint 1: US-001, US-002 (MVP)
- Sprint 2: US-003, US-004
- Sprint 3: US-005, US-006
- Sprint 4: US-007, US-008 (OAuth)

## Criterios de Aceptación de la Épica
- [ ] Usuario puede registrarse y hacer login
- [ ] Usuario puede recuperar acceso si olvida contraseña
- [ ] Usuario puede gestionar su perfil
- [ ] Sistema cumple requisitos de seguridad (OWASP)
- [ ] Cobertura de tests >85%

## Riesgos
- Integración con OAuth puede ser compleja
- Requisitos de seguridad estrictos
- Validación de emails puede tener delays

## Dependencias
- Ninguna (es fundacional)
```

### Cuándo dividir una Épica

Una épica debe dividirse cuando:
- ✅ No cabe en un sprint (>13 story points)
- ✅ Involucra múltiples equipos
- ✅ Tiene objetivos claramente diferenciables
- ✅ Parte de ella puede entregar valor independientemente

---

## 4. Documentación Técnica

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

## ✅ Definition of Done (DoD)

La Definition of Done es un acuerdo compartido sobre qué significa "terminado".

### Niveles de DoD

#### 1. DoD de Tarea

```markdown
## DoD: Implementar endpoint POST /api/users

- [ ] Código escrito
- [ ] Validación de inputs
- [ ] Manejo de errores
- [ ] Tests unitarios
- [ ] Code review aprobado
```

#### 2. DoD de User Story

```markdown
## DoD: User Story

- [ ] Todos los criterios de aceptación cumplidos
- [ ] Código implementado según estándares
- [ ] Code review completado
- [ ] Tests unitarios (cobertura >80%)
- [ ] Tests de integración
- [ ] Sin bugs críticos
- [ ] Documentación técnica actualizada
- [ ] Validado por Product Owner
- [ ] Desplegado en entorno de staging
```

#### 3. DoD de Sprint

```markdown
## DoD: Sprint

- [ ] Todas las User Stories cumplen su DoD
- [ ] Tests de regresión pasando
- [ ] Performance aceptable (<2s carga)
- [ ] Sin deuda técnica crítica documentada
- [ ] Documentación de usuario actualizada
- [ ] Demo exitosa con stakeholders
- [ ] Retrospectiva completada
- [ ] Code coverage >85%
```

### Template de DoD para tu Proyecto

```markdown
# Definition of Done - Proyecto [Nombre]

## 1. Código

- [ ] Implementado según User Story
- [ ] Sigue guías de estilo (ESLint/Prettier)
- [ ] Sin código comentado o debug logs
- [ ] Variables y funciones con nombres descriptivos
- [ ] Funciones pequeñas (<50 líneas)
- [ ] Sin código duplicado significativo

## 2. Tests

- [ ] Tests unitarios escritos
- [ ] Cobertura de código >80%
- [ ] Tests de integración (si aplica)
- [ ] Tests E2E para flujos críticos
- [ ] Todos los tests pasando en CI

## 3. Code Review

- [ ] PR creado con descripción completa
- [ ] Al menos 1 aprobación
- [ ] Todos los comentarios resueltos
- [ ] Sin conflictos de merge
- [ ] CI checks pasando

## 4. Documentación

- [ ] README actualizado (si aplica)
- [ ] Comentarios en código complejo
- [ ] API docs actualizadas (Swagger/OpenAPI)
- [ ] Changelog actualizado

## 5. Calidad

- [ ] Sin errores de linter
- [ ] Sin warnings en consola
- [ ] Accesibilidad básica (WCAG 2.1 Level A)
- [ ] Responsive (mobile, tablet, desktop)
- [ ] Probado en Chrome, Firefox, Safari

## 6. Seguridad

- [ ] Inputs validados y sanitizados
- [ ] Sin datos sensibles en logs
- [ ] Autenticación/autorización implementada
- [ ] Sin vulnerabilidades conocidas (npm audit)

## 7. Aceptación

- [ ] Todos los criterios de aceptación cumplidos
- [ ] Demostrado al Product Owner
- [ ] Product Owner aprueba
- [ ] Desplegado en ambiente de staging

## 8. DevOps

- [ ] Construye sin errores
- [ ] Migraciones de DB documentadas
- [ ] Variables de entorno documentadas
- [ ] Rollback plan considerado
```

---

## 5. Priorización y Estimación

### 🎯 Técnicas de Priorización

#### 1. MoSCoW

Clasifica requisitos en 4 categorías:

| Categoría | Significado | % Recomendado |
|-----------|-------------|---------------|
| **M**ust have | Crítico, sin esto no funciona | 60% |
| **S**hould have | Importante, pero no crítico | 20% |
| **C**ould have | Deseable si hay tiempo | 10% |
| **W**on't have (now) | Fuera del scope actual | 10% |

**Ejemplo:**
```
MUST HAVE (MVP):
- Login y registro
- CRUD de productos
- Carrito de compra
- Checkout básico

SHOULD HAVE:
- Búsqueda y filtros
- Recuperar contraseña
- Email confirmación

COULD HAVE:
- Wishlist
- Recomendaciones
- Reviews de productos

WON'T HAVE:
- Login social
- Programa de puntos
- Chat en vivo
```

---

#### 2. Matriz de Valor/Esfuerzo

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

**Ejemplo:**
```
🟢 HACER PRIMERO (Alto valor, Bajo esfuerzo):
   - Login básico
   - Listar productos
   
🟡 HACER DESPUÉS (Alto valor, Alto esfuerzo):
   - Búsqueda avanzada
   - Sistema de pagos
   
🟠 TAL VEZ (Bajo valor, Bajo esfuerzo):
   - Dark mode
   - Animaciones
   
🔴 EVITAR (Bajo valor, Alto esfuerzo):
   - IA para recomendaciones personalizadas v1
```

---

### 📏 Técnicas de Estimación

#### 1. Planning Poker

**Proceso:**
1. Product Owner presenta User Story
2. Equipo discute (max 5 min)
3. Cada miembro elige una carta en secreto
4. Todos revelan simultáneamente
5. Si hay consenso → listo
6. Si no → mayor y menor explican → repetir

**Valores:** 0, ½, 1, 2, 3, 5, 8, 13, 20, 40, 100, ∞, ?

```
Story Points ≠ Horas
Story Points = Complejidad + Esfuerzo + Incertidumbre
```

**Referencia:**
```
1 punto  = Cambiar texto en página
2 puntos = Añadir campo a formulario simple
3 puntos = Nueva página con CRUD básico
5 puntos = Integración con API externa simple
8 puntos = Feature compleja con múltiples componentes
13 puntos= Integración compleja o incertidumbre alta
```

---

#### 2. T-Shirt Sizing

Para estimación rápida inicial:

| Tamaño | Story Points | Ejemplo |
|--------|--------------|---------|
| XS | 1 | Cambio de texto |
| S | 2-3 | Formulario simple |
| M | 5-8 | CRUD completo |
| L | 13-20 | Feature compleja |
| XL | 40+ | Épica (dividir) |

---

#### 3. Velocity (Velocidad del equipo)

**Cálculo:**
```
Velocity = Story Points completados / Sprint

Ejemplo Sprint 1: 18 puntos completados
Ejemplo Sprint 2: 22 puntos completados
Ejemplo Sprint 3: 20 puntos completados

Velocity promedio = (18 + 22 + 20) / 3 = 20 puntos/sprint
```

**Uso:**
```
Product Backlog total: 180 story points
Velocity: 20 puntos/sprint
Sprints necesarios: 180 / 20 = 9 sprints

Con sprints de 2 semanas: 18 semanas (4.5 meses)
```

---

## 6. Ejercicios Prácticos

### 📝 Ejercicio 1: Entrevista a Stakeholder

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

### 📝 Ejercicio 2: Escribir User Stories

**🎯 Objetivo:** Practicar escritura de User Stories con criterios de aceptación  
**⏱️ Duración:** 2 horas

**Proyecto:** Sistema de biblioteca digital

**Tareas:**

1. **Identificar usuarios:**
   - Lector
   - Bibliotecario
   - Administrador

2. **Escribir 10 User Stories** (mínimo 2 por rol):
   ```
   Ejemplo:
   Como lector
   Quiero buscar libros por título, autor o categoría
   Para encontrar rápidamente lecturas de mi interés
   ```

3. **Para cada story:**
   - Criterios de aceptación (mínimo 3)
   - Notas técnicas
   - Definition of Done
   - Estimación

4. **Validar con INVEST:**
   - ¿Es independiente?
   - ¿Es negociable?
   - ¿Aporta valor?
   - ¿Es estimable?
   - ¿Es pequeña?
   - ¿Es testeable?

---

### 📝 Ejercicio 3: Story Mapping

**🎯 Objetivo:** Crear un story map completo  
**⏱️ Duración:** 2-3 horas

**Proyecto:** App de delivery de comida

**Tareas:**

1. **Identificar el User Journey:**
   ```
   Descubrir → Ordenar → Rastrear → Recibir → Calificar
   ```

2. **Actividades principales** (5-7)

3. **Tareas de usuario** bajo cada actividad (3-5 por actividad)

4. **Escribir User Stories** específicas

5. **Priorizar verticalmente**

6. **Definir releases:**
   - MVP (línea 1)
   - v2.0 (línea 2)
   - v3.0 (línea 3)

7. **Presentar al equipo** y justificar priorización

---

### 📝 Ejercicio 4: Diagramas UML

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

### 📝 Ejercicio 5: Definition of Done

**🎯 Objetivo:** Crear DoD para tu proyecto  
**⏱️ Duración:** 1 hora

**Tareas:**

1. **En equipo, definir:**
   - DoD de tarea
   - DoD de User Story
   - DoD de Sprint

2. **Considerar:**
   - Estándares de código
   - Testing
   - Code review
   - Documentación
   - Performance
   - Seguridad
   - Accesibilidad

3. **Validar:**
   - ¿Es realista?
   - ¿Es medible?
   - ¿Todo el equipo está de acuerdo?

4. **Documentar** en el README del proyecto

5. **Revisar cada sprint** en la retrospectiva

---

### 📝 Ejercicio 6: Priorización con MoSCoW

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
- 📕 "User Story Mapping" - Jeff Patton
- 📘 "Agile Estimating and Planning" - Mike Cohn
- 📗 "Software Requirements" - Karl Wiegers

### Herramientas
- **Story Mapping:** Miro, Mural, StoriesOnBoard
- **Diagramas:** draw.io, PlantUML, Lucidchart
- **Prototipos:** Figma, Sketch, Adobe XD
- **Documentación:** Notion, Confluence, GitBook

### Templates
- [User Story Template](https://github.com/user-story-template)
- [ADR Template](https://github.com/joelparkerhenderson/architecture-decision-record)
- [Interview Guide Template](https://github.com/interview-guide)

---

## 🎯 Checklist de Competencias

Al finalizar este bloque, deberías ser capaz de:

- [ ] Aplicar técnicas de elicitación de requisitos
- [ ] Realizar entrevistas efectivas a stakeholders
- [ ] Identificar y analizar stakeholders
- [ ] Escribir User Stories con formato INVEST
- [ ] Definir criterios de aceptación SMART
- [ ] Crear Story Maps para priorización
- [ ] Organizar trabajo en Épicas y Stories
- [ ] Crear diagramas UML (Casos de Uso, Clases, Secuencia)
- [ ] Documentar arquitectura de solución
- [ ] Definir Definition of Done
- [ ] Aplicar técnicas de priorización (MoSCoW, Valor/Esfuerzo)
- [ ] Estimar con Planning Poker y Story Points

---

[⬅️ Bloque 1: Metodologías Ágiles](bloque1.md) | [➡️ Bloque 3: Desarrollo con IA](bloque3.md)
