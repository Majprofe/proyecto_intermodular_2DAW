# 📙 Bloque 3: Desarrollo Asistido por IA

**Objetivo:** Aprender a desarrollar de forma eficiente con asistentes de IA como GitHub Copilot

---

## 📑 Índice de Contenidos

1. [Introducción al Desarrollo con IA](#1-introducción-al-desarrollo-con-ia)
2. [GitHub Copilot](#2-github-copilot)
   - [Configuración y Primeros Pasos](#-configuración-y-primeros-pasos)
   - [Prompting Efectivo](#-prompting-efectivo)
   - [GitHub Copilot Chat](#-github-copilot-chat)
3. [Pair Programming con IA](#3-pair-programming-con-ia)
   - [Flujo de Trabajo](#-flujo-de-trabajo)
   - [Casos de Uso](#-casos-de-uso)
   - [Limitaciones y Cuándo NO Usar IA](#-limitaciones-y-cuándo-no-usar-ia)
4. [Buenas Prácticas](#4-buenas-prácticas)
   - [Validación de Código Generado](#-validación-de-código-generado)
   - [Testing con IA](#-testing-con-ia)
   - [Seguridad y Privacidad](#-seguridad-y-privacidad)
5. [Herramientas Complementarias](#5-herramientas-complementarias)
6. [Ejercicios Prácticos](#6-ejercicios-prácticos)

---

## 1. Introducción al Desarrollo con IA

El desarrollo asistido por IA representa un cambio paradigmático en cómo escribimos software. No reemplaza a los desarrolladores, sino que **amplifica sus capacidades**.

### La Revolución de la IA en Desarrollo

```
Desarrollo Tradicional:
Idea → Investigar → Escribir código → Debuggear → Documentar
      [Horas]     [Horas]            [Horas]     [Horas]

Desarrollo con IA:
Idea → Describir → IA genera → Revisar → Ajustar
      [Minutos]   [Segundos]  [Minutos] [Minutos]
```

### ¿Qué puede hacer la IA?

| ✅ Puede | ❌ No puede (aún) |
|---------|-------------------|
| Generar código boilerplate | Entender requisitos de negocio |
| Sugerir completions | Tomar decisiones arquitectónicas |
| Escribir tests unitarios | Diseñar experiencia de usuario |
| Refactorizar código | Comprender contexto completo del proyecto |
| Documentar funciones | Evaluar trade-offs de negocio |
| Traducir entre lenguajes | Innovar soluciones disruptivas |
| Explicar código existente | Garantizar corrección 100% |
| Generar ejemplos | Depurar problemas complejos |

### Estadísticas Clave

- 📊 **46%** más rápido desarrollo con Copilot (GitHub Study 2023)
- 🎯 **74%** de desarrolladores se sienten más enfocados
- ⚡ **88%** sienten mayor productividad
- 🧠 **Reduce carga cognitiva** en tareas repetitivas

### Mindset: El Desarrollador como "IA Whisperer"

```
Desarrollador Tradicional        →  Desarrollador con IA
─────────────────────────────────────────────────────────
Escribe cada línea                → Dirige la generación
Busca en Stack Overflow          → Pregunta a Copilot
Copia y pega ejemplos            → Adapta sugerencias
Debuggea manualmente             → Co-debuggea con IA
Documenta después                → Documenta mientras genera
```

> 💡 **Tu nuevo rol:** Arquitecto y revisor de código, no solo escritor

---

## 2. GitHub Copilot

GitHub Copilot es un asistente de programación de IA desarrollado por GitHub y OpenAI. Funciona como un "pair programmer" que sugiere código en tiempo real.

---

## ⚙️ Configuración y Primeros Pasos

### Instalación

1. **Suscripción:**
   - 🎓 **Estudiantes:** Gratis con GitHub Student Developer Pack
   - 👔 **Profesional:** $10/mes o $100/año
   - 🏢 **Business:** $19/usuario/mes

2. **Instalar en VS Code:**
   ```
   Extensions → Buscar "GitHub Copilot"
   → Instalar "GitHub Copilot" y "GitHub Copilot Chat"
   → Sign in con tu cuenta de GitHub
   ```

3. **Configuración inicial:**
   ```json
   // settings.json
   {
     "github.copilot.enable": {
       "*": true,
       "yaml": true,
       "plaintext": false,
       "markdown": true
     },
     "github.copilot.editor.enableAutoCompletions": true,
     "editor.inlineSuggest.enabled": true
   }
   ```

### Atajos de Teclado Esenciales

| Atajo | Acción |
|-------|--------|
| `Tab` | Aceptar sugerencia completa |
| `Ctrl + →` | Aceptar palabra por palabra |
| `Alt + ]` | Siguiente sugerencia |
| `Alt + [` | Sugerencia anterior |
| `Esc` | Rechazar sugerencia |
| `Ctrl + Enter` | Ver todas las sugerencias |
| `Ctrl + I` | Abrir Copilot Chat inline |
| `Ctrl + Shift + I` | Abrir Copilot Chat panel |

---

## 💬 Prompting Efectivo

La calidad del código generado depende enormemente de cómo le pides a Copilot que lo genere.

### Anatomía de un Buen Prompt

```javascript
// ❌ Prompt malo: Vago y sin contexto
// funcion de login

// ✅ Prompt bueno: Específico y con contexto
/**
 * Función async para autenticar usuario con email/password
 * - Valida formato de email
 * - Hash de password con bcrypt
 * - Retorna JWT token si credenciales válidas
 * - Lanza error si credenciales incorrectas
 * @param {string} email - Email del usuario
 * @param {string} password - Password en texto plano
 * @returns {Promise<string>} JWT token
 */
async function loginUser(email, password) {
  // Copilot generará código de alta calidad aquí
}
```

### Técnicas de Prompting

#### 1. **Comentarios Descriptivos**

```python
# ❌ Malo
# validar email

# ✅ Bueno
# Función para validar email usando regex
# - Acepta formato: usuario@dominio.extension
# - Retorna True si válido, False si inválido
# - Ejemplo válido: juan@example.com
# - Ejemplo inválido: juan@example
def validate_email(email: str) -> bool:
```

#### 2. **Ejemplos en Comentarios**

```typescript
// Función para calcular descuento basado en cantidad
// Ejemplos:
//   calculateDiscount(5) -> 0 (sin descuento)
//   calculateDiscount(15) -> 10 (10% descuento)
//   calculateDiscount(25) -> 20 (20% descuento)
// Reglas:
//   - 0-9 items: 0% descuento
//   - 10-19 items: 10% descuento
//   - 20+ items: 20% descuento
function calculateDiscount(quantity: number): number {
  // Copilot generará la lógica correcta
}
```

#### 3. **Context Matters: Código Circundante**

```javascript
// Copilot aprende del código existente en tu archivo

// Si tienes esto arriba:
const formatDate = (date) => {
  return new Intl.DateTimeFormat('es-ES').format(date);
};

// Cuando escribas esto:
// Formatear hora con mismo estilo que formatDate
const formatTime = (date) => {
  // Copilot sugerirá: return new Intl.DateTimeFormat('es-ES', { timeStyle: 'medium' }).format(date);
};
```

#### 4. **Tests como Especificación**

```javascript
// Escribe el test primero (TDD):
describe('User.register', () => {
  it('should create user with hashed password', async () => {
    const user = await User.register('test@example.com', 'password123');
    expect(user.email).toBe('test@example.com');
    expect(user.password).not.toBe('password123');
    expect(user.password).toMatch(/^\$2[aby]\$.{56}$/); // bcrypt format
  });

  it('should throw error if email already exists', async () => {
    await User.register('test@example.com', 'password123');
    await expect(User.register('test@example.com', 'other'))
      .rejects.toThrow('Email already registered');
  });
});

// Ahora escribe: static async register(email, password) {
// Copilot generará la implementación que pasa los tests
```

#### 5. **Chain of Thought (Cadena de Pensamiento)**

```python
def complex_calculation(data):
    """
    Calcular precio final con impuestos y descuentos.
    
    Pasos:
    1. Calcular subtotal: precio * cantidad
    2. Aplicar descuento si cantidad >= 10: subtotal * 0.9
    3. Aplicar IVA (21%): subtotal * 1.21
    4. Aplicar redondeo a 2 decimales
    5. Retornar precio final
    
    Ejemplo: precio=10, cantidad=15
      1. subtotal = 150
      2. con descuento = 135
      3. con IVA = 163.35
      4. redondeado = 163.35
    """
    # Copilot generará paso por paso
```

---

## 💭 GitHub Copilot Chat

Copilot Chat permite conversación interactiva con la IA, no solo sugerencias de código.

### Slash Commands

| Comando | Uso |
|---------|-----|
| `/explain` | Explica el código seleccionado |
| `/fix` | Sugiere fix para errores |
| `/tests` | Genera tests para el código |
| `/doc` | Genera documentación |
| `/simplify` | Simplifica código complejo |
| `/optimize` | Optimiza rendimiento |

### Ejemplos de Uso

#### 1. Explicar Código Complejo

```javascript
// Selecciona este código y usa /explain
const memoize = (fn) => {
  const cache = new Map();
  return (...args) => {
    const key = JSON.stringify(args);
    return cache.has(key) ? cache.get(key) : 
           (cache.set(key, fn(...args)), cache.get(key));
  };
};

// Copilot explicará:
// "Esta función implementa memoization, una técnica de optimización
// que cachea resultados de funciones costosas..."
```

#### 2. Generar Tests

```typescript
// Selecciona la función y usa /tests
export function validatePassword(password: string): boolean {
  return password.length >= 8 && 
         /[A-Z]/.test(password) && 
         /[0-9]/.test(password);
}

// Copilot generará:
describe('validatePassword', () => {
  it('should return true for valid password', () => {
    expect(validatePassword('Pass1234')).toBe(true);
  });
  
  it('should return false if less than 8 characters', () => {
    expect(validatePassword('Pass12')).toBe(false);
  });
  
  // ... más tests
});
```

#### 3. Fix de Bugs

```python
# Selecciona código con error y usa /fix
def calculate_average(numbers):
    total = sum(numbers)
    return total / len(numbers)  # Bug: División por cero si lista vacía

# Copilot sugerirá:
def calculate_average(numbers):
    if not numbers:
        return 0
    total = sum(numbers)
    return total / len(numbers)
```

#### 4. Documentación

```javascript
// Selecciona función y usa /doc
function processPayment(amount, currency, cardToken) {
  // ... implementación compleja
}

// Copilot generará:
/**
 * Procesa un pago con tarjeta de crédito
 * @param {number} amount - Monto a cobrar (en centavos)
 * @param {string} currency - Código de moneda ISO 4217 (ej: 'USD', 'EUR')
 * @param {string} cardToken - Token de tarjeta generado por Stripe
 * @returns {Promise<PaymentResult>} Objeto con resultado del pago
 * @throws {PaymentError} Si el pago falla
 * 
 * @example
 * const result = await processPayment(1000, 'USD', 'tok_visa');
 * console.log(result.transactionId);
 */
```

### Preguntas Efectivas en Chat

```
❌ Malo: "como hacer login"

✅ Bueno: 
"Genera una función async loginUser en Node.js/Express que:
- Reciba email y password del body
- Valide con bcrypt contra DB (Prisma)
- Genere JWT token con expiración 24h
- Maneje errores apropiadamente
- Incluya tipos TypeScript"
```

---

## 3. Pair Programming con IA

---

## 🔄 Flujo de Trabajo

### Modelo de Colaboración

```
1. TÚ: Defines el problema y arquitectura
        ↓
2. IA: Genera implementación inicial
        ↓
3. TÚ: Revisas, ajustas, mejoras
        ↓
4. IA: Ayuda con edge cases y tests
        ↓
5. TÚ: Validas y apruebas
        ↓
6. IA: Documenta
```

### Ejemplo Real: Desarrollar Feature Completa

#### Paso 1: Definir estructura (TÚ)

```typescript
// src/features/auth/auth.service.ts

/**
 * Servicio de autenticación
 * Responsabilidades:
 * - Registro de usuarios
 * - Login con JWT
 * - Validación de tokens
 * - Refresh tokens
 */

// Empiezas escribiendo la interfaz:
interface AuthService {
  register(email: string, password: string): Promise<User>;
  login(email: string, password: string): Promise<AuthResponse>;
  validateToken(token: string): Promise<User>;
  refreshToken(refreshToken: string): Promise<AuthResponse>;
}
```

#### Paso 2: IA genera implementación

```typescript
// Copilot autocompleta con implementación sólida:
class AuthServiceImpl implements AuthService {
  constructor(
    private userRepo: UserRepository,
    private jwtService: JWTService
  ) {}

  async register(email: string, password: string): Promise<User> {
    // Valida email
    if (!this.isValidEmail(email)) {
      throw new ValidationError('Invalid email format');
    }

    // Verifica si existe
    const existingUser = await this.userRepo.findByEmail(email);
    if (existingUser) {
      throw new ConflictError('Email already registered');
    }

    // Hash password
    const hashedPassword = await bcrypt.hash(password, 10);

    // Crea usuario
    const user = await this.userRepo.create({
      email,
      password: hashedPassword,
      createdAt: new Date(),
    });

    return user;
  }

  // ... más métodos
}
```

#### Paso 3: TÚ revisas y ajustas

```typescript
// Mejoras que añades:

// 1. Validación más robusta de password
async register(email: string, password: string): Promise<User> {
  // Tu adición: validar password
  if (password.length < 8) {
    throw new ValidationError('Password must be at least 8 characters');
  }
  
  // ... resto del código generado por IA
}

// 2. Logging para debugging
async login(email: string, password: string): Promise<AuthResponse> {
  this.logger.info('Login attempt', { email }); // Tu adición
  
  // ... código IA ...
  
  this.logger.info('Login successful', { userId: user.id }); // Tu adición
  return response;
}
```

#### Paso 4: IA ayuda con tests

```typescript
// Prompt: "Genera tests completos para AuthService"
// Usa /tests en Copilot Chat

describe('AuthService', () => {
  let authService: AuthServiceImpl;
  let userRepo: MockUserRepository;
  let jwtService: MockJWTService;

  beforeEach(() => {
    userRepo = new MockUserRepository();
    jwtService = new MockJWTService();
    authService = new AuthServiceImpl(userRepo, jwtService);
  });

  describe('register', () => {
    it('should create user with hashed password', async () => {
      const user = await authService.register('test@example.com', 'Password123');
      
      expect(user.email).toBe('test@example.com');
      expect(user.password).not.toBe('Password123');
      expect(await bcrypt.compare('Password123', user.password)).toBe(true);
    });

    it('should throw ValidationError for invalid email', async () => {
      await expect(authService.register('invalid', 'Password123'))
        .rejects.toThrow(ValidationError);
    });

    // ... más tests
  });
});
```

---

## 🎯 Casos de Uso

### 1. Boilerplate Code (⭐⭐⭐⭐⭐)

**Ideal para:** CRUD, APIs REST, configuración

```typescript
// Prompt: "Create Express CRUD endpoints for Product model"

// Copilot genera:
router.post('/products', async (req, res) => {
  try {
    const product = await Product.create(req.body);
    res.status(201).json(product);
  } catch (error) {
    res.status(400).json({ error: error.message });
  }
});

router.get('/products', async (req, res) => {
  const products = await Product.findAll();
  res.json(products);
});

router.get('/products/:id', async (req, res) => {
  const product = await Product.findByPk(req.params.id);
  if (!product) {
    return res.status(404).json({ error: 'Product not found' });
  }
  res.json(product);
});

// ... PUT, DELETE
```

### 2. Conversión de Formatos (⭐⭐⭐⭐⭐)

**Ideal para:** JSON↔️XML, SQL↔️NoSQL, TypeScript↔️JavaScript

```javascript
// Prompt: "Convert this SQL to Prisma schema"

// SQL:
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  email VARCHAR(255) UNIQUE NOT NULL,
  password VARCHAR(255) NOT NULL,
  created_at TIMESTAMP DEFAULT NOW()
);

// Copilot genera Prisma:
model User {
  id        Int      @id @default(autoincrement())
  email     String   @unique
  password  String
  createdAt DateTime @default(now()) @map("created_at")

  @@map("users")
}
```

### 3. Tests Unitarios (⭐⭐⭐⭐)

**Ideal para:** Happy paths, edge cases, mocking

```javascript
// Función a testear
function calculateShipping(weight, distance, express = false) {
  const baseRate = 5;
  const weightCost = weight * 0.5;
  const distanceCost = distance * 0.1;
  const expressFee = express ? 10 : 0;
  return baseRate + weightCost + distanceCost + expressFee;
}

// Prompt: "Generate comprehensive tests for calculateShipping"
// Copilot genera suite completa de tests
```

### 4. Documentación (⭐⭐⭐⭐)

**Ideal para:** JSDoc, README, API docs

```typescript
// Usa /doc en Copilot Chat
class PaymentProcessor {
  async processPayment(orderId, amount, paymentMethod) {
    // ...
  }
}

// Genera:
/**
 * Procesa pagos de órdenes
 * 
 * @class PaymentProcessor
 * @description Maneja toda la lógica de procesamiento de pagos,
 * incluyendo validación, autorización y confirmación.
 * 
 * @example
 * const processor = new PaymentProcessor(stripeClient);
 * const result = await processor.processPayment('ORD123', 99.99, 'card');
 */
```

### 5. Refactoring (⭐⭐⭐)

**Ideal para:** Simplificar código legacy

```javascript
// Código legacy
function getUserData(id) {
  var user = null;
  var xhr = new XMLHttpRequest();
  xhr.open('GET', '/api/users/' + id, false);
  xhr.send();
  if (xhr.status === 200) {
    user = JSON.parse(xhr.responseText);
  }
  return user;
}

// Prompt: "Refactor to modern async/await with fetch"
// Copilot genera:
async function getUserData(id) {
  const response = await fetch(`/api/users/${id}`);
  if (!response.ok) {
    throw new Error(`HTTP error! status: ${response.status}`);
  }
  return await response.json();
}
```

---

## ⚠️ Limitaciones y Cuándo NO Usar IA

### Cuándo NO confiar en IA

| Situación | Por qué | Alternativa |
|-----------|---------|-------------|
| **Lógica de negocio compleja** | IA no entiende el dominio | Diseña tú, IA implementa detalles |
| **Decisiones de arquitectura** | Requiere trade-offs contextuales | Consulta con equipo senior |
| **Seguridad crítica** | Puede generar vulnerabilidades | Revisión humana exhaustiva + auditoría |
| **Algoritmos avanzados** | Puede ser subóptimo | Usa implementaciones probadas |
| **Cumplimiento legal** | No entiende regulaciones | Consulta expertos legales |

### Señales de Alerta

```javascript
// 🚨 RED FLAG: Copilot sugiere esto para auth
app.post('/login', (req, res) => {
  const user = users.find(u => u.email === req.body.email);
  if (user && user.password === req.body.password) { // ❌ Compara password en plain text!
    res.json({ token: user.id }); // ❌ Token es solo el ID!
  }
});

// ✅ TÚ debes reconocer y corregir:
app.post('/login', async (req, res) => {
  const user = await User.findByEmail(req.body.email);
  if (user && await bcrypt.compare(req.body.password, user.password)) {
    const token = jwt.sign({ userId: user.id }, process.env.JWT_SECRET, { expiresIn: '24h' });
    res.json({ token });
  } else {
    res.status(401).json({ error: 'Invalid credentials' });
  }
});
```

### Problemas Comunes

1. **Alucinaciones:** IA inventa APIs que no existen
   ```python
   # ❌ Copilot puede sugerir:
   import openai
   response = openai.generate_image(prompt)  # Esta función no existe!
   
   # ✅ Verifica en documentación oficial
   ```

2. **Código obsoleto:** Usa librerías antiguas
   ```javascript
   // ❌ Copilot sugiere:
   request.get('https://api.example.com', (err, res, body) => {
     // request está deprecated!
   });
   
   // ✅ Usa alternativas modernas:
   const response = await fetch('https://api.example.com');
   ```

3. **Over-engineering:** Soluciones demasiado complejas
   ```javascript
   // ❌ Copilot puede generar:
   class SingletonFactoryBuilder {
     // 50 líneas de patrón innecesario
   }
   
   // ✅ Simplifica:
   const config = { ... };
   ```

---

## 4. Buenas Prácticas

---

## ✅ Validación de Código Generado

### Checklist de Revisión

```markdown
## Antes de aceptar código de IA:

### Funcionalidad
- [ ] ¿Hace lo que se supone que debe hacer?
- [ ] ¿Maneja casos edge correctamente?
- [ ] ¿Qué pasa con inputs inválidos?

### Seguridad
- [ ] ¿Valida inputs del usuario?
- [ ] ¿Sanitiza datos antes de queries?
- [ ] ¿Expone información sensible?
- [ ] ¿Usa prácticas de seguridad actualizadas?

### Performance
- [ ] ¿Es eficiente algorítmicamente?
- [ ] ¿Hay fugas de memoria potenciales?
- [ ] ¿Escala con datos grandes?

### Calidad de Código
- [ ] ¿Es legible y mantenible?
- [ ] ¿Sigue las convenciones del proyecto?
- [ ] ¿Está bien estructurado?
- [ ] ¿Necesita refactoring?

### Testing
- [ ] ¿Es testeable?
- [ ] ¿Tiene tests?
- [ ] ¿Los tests cubren casos importantes?

### Dependencias
- [ ] ¿Las librerías existen y están actualizadas?
- [ ] ¿Son necesarias todas las dependencias?
```

### Proceso de Validación

```javascript
// 1. EJECUTA el código generado
// No asumas que funciona, pruébalo

// 2. LEE el código línea por línea
// ¿Entiendes qué hace cada parte?

// 3. PRUEBA casos edge
const testCases = [
  { input: null, expected: /* ... */ },
  { input: undefined, expected: /* ... */ },
  { input: [], expected: /* ... */ },
  { input: [-1, 0, 1], expected: /* ... */ },
];

// 4. VERIFICA en documentación oficial
// Si usa una API, confirma que existe

// 5. ANALIZA performance
console.time('operation');
// ... código
console.timeEnd('operation');

// 6. REVISA seguridad
// Usa herramientas: npm audit, Snyk, etc.
```

---

## 🧪 Testing con IA

### Estrategia de Testing

```
1. TÚ escribes test (TDD)
   ↓
2. IA genera implementación
   ↓
3. Verificas que tests pasen
   ↓
4. IA genera más tests (edge cases)
   ↓
5. TÚ revisas cobertura
```

### Ejemplo: TDD con IA

```javascript
// PASO 1: TÚ escribes el test
describe('calculateTax', () => {
  it('should calculate 21% IVA for Spain', () => {
    expect(calculateTax(100, 'ES')).toBe(21);
  });

  it('should calculate 19% VAT for Germany', () => {
    expect(calculateTax(100, 'DE')).toBe(19);
  });

  it('should throw error for invalid country', () => {
    expect(() => calculateTax(100, 'XX')).toThrow('Invalid country code');
  });
});

// PASO 2: IA genera implementación
function calculateTax(amount, countryCode) {
  const taxRates = {
    'ES': 0.21,
    'DE': 0.19,
    'FR': 0.20,
    'IT': 0.22,
  };

  if (!(countryCode in taxRates)) {
    throw new Error('Invalid country code');
  }

  return amount * taxRates[countryCode];
}

// PASO 3: Tests pasan ✅

// PASO 4: Pide a IA más tests
// Prompt: "Generate more edge case tests for calculateTax"

it('should handle amount of 0', () => {
  expect(calculateTax(0, 'ES')).toBe(0);
});

it('should handle negative amounts', () => {
  expect(() => calculateTax(-100, 'ES')).toThrow('Amount must be positive');
});

it('should round to 2 decimals', () => {
  expect(calculateTax(10.33, 'ES')).toBe(2.17);
});

// PASO 5: TÚ revisas e implementas casos faltantes
```

### Generar Tests de Integración

```typescript
// Prompt: "Generate integration tests for user registration endpoint"

describe('POST /api/auth/register', () => {
  it('should create new user and return 201', async () => {
    const response = await request(app)
      .post('/api/auth/register')
      .send({
        email: 'newuser@example.com',
        password: 'Password123!',
      });

    expect(response.status).toBe(201);
    expect(response.body).toHaveProperty('user');
    expect(response.body).toHaveProperty('token');
    expect(response.body.user.email).toBe('newuser@example.com');
  });

  it('should return 400 for invalid email', async () => {
    const response = await request(app)
      .post('/api/auth/register')
      .send({
        email: 'invalid-email',
        password: 'Password123!',
      });

    expect(response.status).toBe(400);
    expect(response.body.error).toContain('email');
  });

  it('should return 409 for existing email', async () => {
    // Crea usuario primero
    await User.create({
      email: 'existing@example.com',
      password: await bcrypt.hash('Password123!', 10),
    });

    const response = await request(app)
      .post('/api/auth/register')
      .send({
        email: 'existing@example.com',
        password: 'OtherPass123!',
      });

    expect(response.status).toBe(409);
  });
});
```

---

## 🔐 Seguridad y Privacidad

### Datos que NO debes compartir con IA

❌ **NUNCA envíes a Copilot:**
- Credenciales (API keys, passwords, tokens)
- Datos personales de usuarios reales
- Información propietaria de la empresa
- Secretos de infraestructura
- Datos regulados (GDPR, HIPAA, etc.)

### Configurar para Seguridad

```json
// settings.json
{
  // No permitir sugerencias de archivos específicos
  "github.copilot.advanced": {
    "excludedLanguages": [],
    "filterMatching": true
  }
}

// .gitignore - asegúrate de incluir:
.env
.env.local
secrets.json
*.key
*.pem
config/credentials.js
```

### Ejemplo: Código Seguro con IA

```javascript
// ❌ NO HAGAS ESTO: exponer secrets en código
const stripe = require('stripe')('sk_live_51H...'); // ❌ API key hardcodeada

// ✅ HAZ ESTO: usa variables de entorno
const stripe = require('stripe')(process.env.STRIPE_SECRET_KEY);

// ❌ NO: SQL injection vulnerable
app.get('/users/:id', (req, res) => {
  db.query(`SELECT * FROM users WHERE id = ${req.params.id}`); // ❌
});

// ✅ SÍ: usa prepared statements
app.get('/users/:id', (req, res) => {
  db.query('SELECT * FROM users WHERE id = ?', [req.params.id]); // ✅
});

// ❌ NO: XSS vulnerable
app.get('/search', (req, res) => {
  res.send(`<h1>Results for: ${req.query.q}</h1>`); // ❌
});

// ✅ SÍ: sanitiza outputs
const sanitizeHtml = require('sanitize-html');
app.get('/search', (req, res) => {
  const safeQuery = sanitizeHtml(req.query.q);
  res.send(`<h1>Results for: ${safeQuery}</h1>`); // ✅
});
```

### Auditoría de Código Generado

```bash
# 1. Analiza dependencias
npm audit
npm audit fix

# 2. Escanea vulnerabilidades
npx snyk test

# 3. Linter de seguridad
npm install --save-dev eslint-plugin-security
# Añade a .eslintrc:
{
  "plugins": ["security"],
  "extends": ["plugin:security/recommended"]
}

# 4. Análisis estático
npm install --save-dev @typescript-eslint/eslint-plugin
```

---

## 5. Herramientas Complementarias

### Ecosistema de IA para Desarrollo

| Herramienta | Propósito | Mejor para |
|-------------|-----------|------------|
| **GitHub Copilot** | Code completion | Día a día, all-purpose |
| **ChatGPT/Claude** | Conversación larga | Arquitectura, debugging complejo |
| **Tabnine** | Alternativa a Copilot | Teams con datos privados |
| **Codeium** | Free alternative | Estudiantes sin Copilot |
| **Amazon CodeWhisperer** | AWS integration | Proyectos AWS-heavy |
| **Cursor** | AI-first IDE | Proyectos nuevos desde cero |

### Integración con Otras Herramientas

```javascript
// 1. Pre-commit hooks con IA review
// .husky/pre-commit
npm run lint
npm run test
npx ai-code-review  // Herramienta ficticia, pero el concepto es real

// 2. CI/CD con análisis IA
// .github/workflows/ci.yml
- name: AI Code Quality Check
  uses: some-ai-tool/action@v1
  with:
    check-security: true
    check-performance: true
    check-best-practices: true

// 3. PR descriptions automáticas
// GitHub Action que usa IA para generar descripción de PR
```

---

## 6. Ejercicios Prácticos

### 📝 Ejercicio 1: Primer Contacto con Copilot

**🎯 Objetivo:** Familiarizarse con sugerencias básicas  
**⏱️ Duración:** 30 minutos

**Tareas:**

1. **Instala GitHub Copilot** en VS Code

2. **Prueba sugerencias inline:**
   ```javascript
   // Escribe este comentario y espera sugerencia:
   // function to validate email format
   ```

3. **Experimenta con completions:**
   - Escribe `function calculateTotal(` y observa
   - Acepta con Tab
   - Prueba Alt+] para ver alternativas

4. **Modifica sugerencias:**
   - Acepta palabra por palabra (Ctrl+→)
   - Rechaza y escribe tu versión
   - Compara resultados

---

### 📝 Ejercicio 2: CRUD con Copilot

**🎯 Objetivo:** Generar API REST completa  
**⏱️ Duración:** 1-2 horas

**Proyecto:** API de gestión de tareas (To-Do)

**Tareas:**

1. **Define el modelo:**
   ```typescript
   // models/task.ts
   // Define Task interface with id, title, description, completed, createdAt
   ```

2. **Genera endpoints con prompts:**
   ```typescript
   // routes/tasks.ts
   // Express router with CRUD endpoints for tasks:
   // - GET /tasks - list all
   // - GET /tasks/:id - get one
   // - POST /tasks - create
   // - PUT /tasks/:id - update
   // - DELETE /tasks/:id - delete
   ```

3. **Añade validación:**
   ```typescript
   // middleware/validation.ts
   // Joi schema validation for task creation and update
   ```

4. **Genera tests:**
   ```typescript
   // Usa /tests para generar suite completa
   ```

5. **Compara:**
   - ¿Cuánto tiempo te habría tomado manualmente?
   - ¿Qué partes tuviste que ajustar?
   - ¿Qué faltaba?

---

### 📝 Ejercicio 3: TDD con IA

**🎯 Objetivo:** Test-Driven Development asistido por IA  
**⏱️ Duración:** 1 hora

**Funcionalidad:** Carrito de compra

**Workflow:**

1. **Escribe tests PRIMERO:**
   ```javascript
   describe('ShoppingCart', () => {
     it('should start empty', () => {
       const cart = new ShoppingCart();
       expect(cart.items).toHaveLength(0);
       expect(cart.total).toBe(0);
     });

     it('should add item to cart', () => {
       const cart = new ShoppingCart();
       cart.addItem({ id: 1, name: 'Product', price: 10 });
       expect(cart.items).toHaveLength(1);
       expect(cart.total).toBe(10);
     });

     it('should calculate total with multiple items', () => {
       const cart = new ShoppingCart();
       cart.addItem({ id: 1, name: 'Product 1', price: 10 });
       cart.addItem({ id: 2, name: 'Product 2', price: 20 });
       expect(cart.total).toBe(30);
     });

     it('should remove item from cart', () => {
       // ... tu test
     });

     it('should apply discount code', () => {
       // ... tu test
     });
   });
   ```

2. **Deja que Copilot genere** la implementación

3. **Ejecuta tests** y ajusta si es necesario

4. **Añade más tests** para edge cases

5. **Refactoriza** con ayuda de IA (usa /simplify)

---

### 📝 Ejercicio 4: Refactoring de Código Legacy

**🎯 Objetivo:** Modernizar código antiguo con IA  
**⏱️ Duración:** 1-2 horas

**Código legacy proporcionado:**

```javascript
// legacy-user-service.js
var UserService = function() {
  this.users = [];
  
  this.addUser = function(name, email, password) {
    var user = {
      id: this.users.length + 1,
      name: name,
      email: email,
      password: password,  // Sin hash!
      created: new Date()
    };
    this.users.push(user);
    return user;
  };
  
  this.loginUser = function(email, password) {
    for (var i = 0; i < this.users.length; i++) {
      if (this.users[i].email == email && this.users[i].password == password) {
        return this.users[i];
      }
    }
    return null;
  };
  
  this.getAllUsers = function() {
    return this.users;
  };
};
```

**Tareas:**

1. **Convierte a ES6+ class con async/await**
   - Usa prompts: "Refactor to modern ES6 class with async methods"

2. **Añade seguridad:**
   - Hash de passwords con bcrypt
   - Validación de email
   - Sanitización de inputs

3. **Implementa TypeScript:**
   - Tipos e interfaces
   - Strict mode

4. **Añade manejo de errores:**
   - Try/catch
   - Errores personalizados
   - Logging

5. **Genera tests completos**

6. **Documenta con JSDoc/TSDoc**

**Compara:**
- Código antes vs después
- Tiempo invertido
- ¿Qué no pudo hacer la IA sola?

---

### 📝 Ejercicio 5: Debugging Asistido

**🎯 Objetivo:** Usar IA para debuggear  
**⏱️ Duración:** 45 minutos

**Código con bugs:**

```javascript
function processOrders(orders) {
  let total = 0;
  let discountedOrders = [];
  
  for (let i = 0; i <= orders.length; i++) {  // Bug 1
    let order = orders[i];
    
    if (order.amount > 100) {
      order.amount = order.amount * 0.9;  // Bug 2
    }
    
    total += order.amount;
    discountedOrders.push(order);
  }
  
  return {
    total: total,
    orders: discountedOrders,
    average: total / orders.length  // Bug 3
  };
}

const orders = [
  { id: 1, amount: 50 },
  { id: 2, amount: 150 },
  { id: 3, amount: 200 }
];

console.log(processOrders(orders));
```

**Tareas:**

1. **Ejecuta el código** - observa el error

2. **Usa Copilot Chat:**
   - Selecciona código
   - Usa `/fix`
   - Analiza la sugerencia

3. **Identifica TODOS los bugs** (hay 3)

4. **Usa `/explain`** para entender cada bug

5. **Corrige manualmente** para aprender

6. **Genera tests** que detectarían estos bugs

7. **Añade validación** para prevenir bugs similares

---

### 📝 Ejercicio 6: Proyecto Integrador

**🎯 Objetivo:** Desarrollar feature completa con IA  
**⏱️ Duración:** 4-6 horas

**Feature:** Sistema de comentarios en blog

**Requisitos:**

```markdown
## User Stories

### US-01: Crear comentario
Como lector
Quiero comentar en un post
Para expresar mi opinión

Criterios:
- Usuario debe estar autenticado
- Comentario de 1-500 caracteres
- Se guarda con timestamp
- Se muestra inmediatamente

### US-02: Ver comentarios
Como lector
Quiero ver comentarios en orden cronológico
Para seguir la discusión

Criterios:
- Mostrar usuario y fecha
- Paginación (10 por página)
- Incluir número total

### US-03: Editar comentario
Como autor del comentario
Quiero editar mi comentario
Para corregir errores

Criterios:
- Solo propietario puede editar
- Máximo 5 min después de publicar
- Marcar como "editado"

### US-04: Eliminar comentario
Como autor del comentario
Quiero eliminar mi comentario
Para retractarme

Criterios:
- Solo propietario puede eliminar
- Soft delete (no borrar de DB)
- Mostrar "[comentario eliminado]"
```

**Implementación con IA:**

1. **Arquitectura (TÚ decides):**
   - Frontend: React/Vue
   - Backend: Node.js + Express
   - DB: PostgreSQL o MongoDB

2. **Backend con Copilot:**
   ```typescript
   // Genera modelos, rutas, controladores, middlewares
   ```

3. **Tests (TDD):**
   ```typescript
   // Genera tests ANTES de implementar
   ```

4. **Frontend con Copilot:**
   ```typescript
   // Genera componentes, hooks, services
   ```

5. **Integración:**
   - Conecta frontend-backend
   - Manejo de errores
   - Loading states

6. **Pulido:**
   - Validación completa
   - Mensajes de error user-friendly
   - Responsive design
   - Accesibilidad básica

**Evaluación:**

- ¿Qué % fue generado por IA?
- ¿Cuánto tiempo ahorraste?
- ¿Qué problemas encontró la IA?
- ¿Qué problemas NO encontró?
- ¿Cuánto código tuviste que reescribir?

---

## 📚 Recursos Adicionales

### Documentación Oficial
- [GitHub Copilot Docs](https://docs.github.com/es/copilot)
- [Best Practices Guide](https://github.blog/2023-06-20-how-to-write-better-prompts-for-github-copilot/)
- [Copilot Trust Center](https://resources.github.com/copilot-trust-center/)

### Comunidades
- [GitHub Copilot Discord](https://discord.gg/github)
- [r/github_copilot](https://www.reddit.com/r/github_copilot/)

### Blogs y Tutoriales
- [GitHub Blog - Copilot](https://github.blog/tag/github-copilot/)
- [OpenAI Cookbook](https://cookbook.openai.com/)

### Cursos
- [LinkedIn Learning: GitHub Copilot](https://www.linkedin.com/learning/topics/github-copilot)
- [Pluralsight: AI Pair Programming](https://www.pluralsight.com/)

---

## 🎯 Checklist de Competencias

Al finalizar este bloque, deberías ser capaz de:

- [ ] Configurar y usar GitHub Copilot efectivamente
- [ ] Escribir prompts que generen código de calidad
- [ ] Usar Copilot Chat para debugging y refactoring
- [ ] Aplicar TDD con asistencia de IA
- [ ] Validar y revisar código generado por IA
- [ ] Identificar limitaciones y cuándo NO usar IA
- [ ] Generar tests automáticamente
- [ ] Refactorizar código legacy con IA
- [ ] Documentar código con ayuda de IA
- [ ] Mantener seguridad y privacidad con IA
- [ ] Integrar IA en workflow de desarrollo ágil

---

## 🚀 El Futuro del Desarrollo

> "GitHub Copilot no reemplaza a los desarrolladores, 
> sino que amplifica las capacidades de los buenos desarrolladores."

### Habilidades Clave en la Era de la IA

1. **Pensamiento Crítico:** Evaluar código generado
2. **Arquitectura:** Diseñar sistemas robustos
3. **Comunicación:** Prompts efectivos = mejor código
4. **Domain Knowledge:** IA no entiende tu negocio
5. **Testing:** IA ayuda, pero tú validas
6. **Security:** IA puede introducir vulnerabilidades
7. **Maintenance:** Código mantenible > código rápido

### Mantra del Desarrollador con IA

```
✅ Usa IA para acelerar
❌ No uses IA para pensar por ti

✅ Valida todo código generado
❌ No copies sin entender

✅ Aprende de las sugerencias
❌ No dependas ciegamente

✅ IA como copiloto
❌ No IA como piloto
```

---

[⬅️ Bloque 2: Ingeniería de Requisitos](bloque2.md) | [🏠 Volver al inicio](README.md)
