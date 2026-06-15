# Clase 1: Introducción a JavaScript, Variables, Tipado Dinámico y Operadores Especiales

## Objetivos de la clase

Al finalizar esta clase los estudiantes serán capaces de:

* Comprender qué es JavaScript y para qué se utiliza.
* Diferenciar entre el entorno Navegador y Node.js.
* Entender la diferencia entre tipado estático y tipado dinámico.
* Declarar variables utilizando `let` y `const`.
* Identificar los principales tipos de datos de JavaScript.
* Utilizar operadores aritméticos, de comparación y lógicos.
* Aplicar los operadores modernos `&&`, `||` y `??`.

---

# Parte 1: ¿Qué es JavaScript?

Cuando visitamos una página web normalmente intervienen tres tecnologías:

### HTML

Define la estructura de la página.

```html
<h1>Hola Mundo</h1>
<button>Presionar</button>
```

---

### CSS

Define la apariencia visual.

```css
h1{
    color: blue;
}
```

---

### JavaScript

Define el comportamiento.

```javascript
console.log("Hola Mundo");
```

JavaScript permite:

* Responder a clics de botones.
* Validar formularios.
* Mostrar información dinámica.
* Consumir datos desde Internet.
* Crear videojuegos.
* Construir aplicaciones completas.

Actualmente es uno de los lenguajes más utilizados del mundo porque puede trabajar tanto en el navegador como en el servidor.

---

# Parte 2: ¿Dónde se ejecuta JavaScript?

## En el Navegador

Ejemplos:

* Chrome
* Firefox
* Edge

JavaScript puede controlar:

* Botones
* Formularios
* Imágenes
* Ventanas
* Elementos HTML

Ejemplo:

```javascript
alert("Hola desde el navegador");
```

---

## En Node.js

Node.js permite ejecutar JavaScript fuera del navegador.

Ejemplo:

```javascript
console.log("Hola desde Node.js");
```

Se utiliza para:

* Crear servidores web.
* Construir APIs.
* Automatizar tareas.
* Crear aplicaciones backend.

---

## Comparación

| Navegador        | Node.js         |
| ---------------- | --------------- |
| Tiene HTML       | No tiene HTML   |
| Tiene DOM        | No tiene DOM    |
| Tiene window     | No tiene window |
| Interfaz gráfica | Consola         |

---

# Parte 3: Mi primer programa

El programa más famoso de cualquier lenguaje es:

```javascript
console.log("Hola Mundo");
```

Explicación:

* `console` representa la consola.
* `log()` muestra información.

Resultado:

```text
Hola Mundo
```

---

# Parte 4: El gran cambio para quienes vienen de C++

## Tipado Estático vs Tipado Dinámico

Antes de aprender variables en JavaScript debemos entender una diferencia fundamental respecto a C++.

---

## ¿Cómo funciona C++?

Cuando creamos una variable debemos indicar el tipo de dato.

```cpp
int edad = 15;
string nombre = "Carlos";
bool activo = true;
```

Cada variable tiene un tipo fijo.

Por ejemplo:

```cpp
int edad = 15;

edad = "Hola";
```

Esto genera error porque la variable fue creada para almacenar números enteros.

---

### ¿Qué significa Tipado Estático?

**Definición:**

> El tipo de dato se define al crear la variable y no puede cambiar.

Visualmente:

```text
edad
└── SOLO puede almacenar enteros
```

Ventajas:

* Detecta errores antes de ejecutar.
* Es más seguro.
* Es más estricto.

---

## ¿Cómo funciona JavaScript?

En JavaScript no indicamos el tipo.

```javascript
let edad = 15;
```

JavaScript analiza automáticamente el valor y determina el tipo.

---

### Esto es válido

```javascript
let dato = 15;

dato = "Hola";

dato = true;
```

La misma variable almacena distintos tipos de datos.

Visualmente:

```text
dato
└── 15
```

Después:

```text
dato
└── "Hola"
```

Después:

```text
dato
└── true
```

---

### ¿Qué significa Tipado Dinámico?

**Definición:**

> El tipo puede cambiar durante la ejecución del programa.

---

## Analogía

### C++

Caja especializada:

```text
┌─────────┐
│ INT     │
└─────────┘
```

Solo acepta números.

---

### JavaScript

Caja flexible:

```text
┌─────────┐
│         │
└─────────┘
```

Hoy puede guardar un número.

Mañana un texto.

Después un valor booleano.

---

## El operador typeof

Permite averiguar el tipo de un dato.

```javascript
let dato = 15;

console.log(typeof dato);
```

Resultado:

```text
number
```

---

```javascript
dato = "Hola";

console.log(typeof dato);
```

Resultado:

```text
string
```

---

```javascript
dato = true;

console.log(typeof dato);
```

Resultado:

```text
boolean
```

---

## Ventajas del Tipado Dinámico

Permite escribir código más rápido.

```javascript
let nombre = "Carlos";
let edad = 15;
let activo = true;
```

No es necesario especificar tipos.

---

## Desventajas

Puede producir errores inesperados.

```javascript
let numero = "10";

console.log(numero + 5);
```

Resultado:

```text
105
```

Porque `"10"` es texto y JavaScript concatena ambos valores.

---

### Comparación rápida

| Característica        | C++ | JavaScript |
| --------------------- | --- | ---------- |
| Tipo obligatorio      | Sí  | No         |
| Puede cambiar de tipo | No  | Sí         |
| Más flexible          | No  | Sí         |
| Más seguro            | Sí  | Menos      |

---

## Lo que deben recordar

La diferencia más importante entre C++ y JavaScript es:

> En JavaScript las variables no tienen un tipo fijo.

---

# Parte 5: Variables

Las variables son espacios en memoria donde almacenamos información.

---

## let

Se utiliza cuando el valor puede cambiar.

```javascript
let edad = 15;

edad = 16;
```

---

## const

Se utiliza cuando el valor no debe cambiar.

```javascript
const PI = 3.1416;
```

Esto genera error:

```javascript
PI = 5;
```

---

## Regla rápida

¿El valor cambiará?

* Sí → `let`
* No → `const`

---

# Parte 6: Tipos de datos básicos

## String

Texto.

```javascript
let nombre = "Carlos";
```

---

## Number

Números enteros o decimales.

```javascript
let edad = 15;
let precio = 19.99;
```

---

## Boolean

Verdadero o falso.

```javascript
let activo = true;
let premium = false;
```

---

## Null

Representa ausencia de valor.

```javascript
let usuario = null;
```

---

## Undefined

Variable creada pero sin valor.

```javascript
let correo;
```

---

# Parte 7: Operadores básicos

## Aritméticos

```javascript
let a = 10;
let b = 5;

console.log(a + b);
console.log(a - b);
console.log(a * b);
console.log(a / b);
```

---

## Comparación

```javascript
console.log(10 > 5);
```

Resultado:

```text
true
```

---

```javascript
console.log(10 < 5);
```

Resultado:

```text
false
```

---

## Igualdad estricta

```javascript
console.log(5 === 5);
```

Resultado:

```text
true
```

---

# Parte 8: Operadores modernos de JavaScript

Estos operadores aparecen constantemente en proyectos reales.

---

## Operador ||

Significa:

> Si el valor de la izquierda es falso, utiliza el de la derecha.

```javascript
let nombre = "";

console.log(nombre || "Invitado");
```

Resultado:

```text
Invitado
```

---

## Operador &&

Significa:

> Solo ejecuta lo de la derecha si lo de la izquierda es verdadero.

```javascript
let logueado = true;

logueado && console.log("Bienvenido");
```

Resultado:

```text
Bienvenido
```

---

## Operador ??

Significa:

> Usa el valor de la derecha únicamente si el de la izquierda es null o undefined.

```javascript
let nombre = null;

console.log(nombre ?? "Invitado");
```

Resultado:

```text
Invitado
```

---

## Diferencia entre || y ??

```javascript
let puntos = 0;

console.log(puntos || 100);
```

Resultado:

```text
100
```

---

```javascript
console.log(puntos ?? 100);
```

Resultado:

```text
0
```

---

## Regla para recordar

```text
||  → reemplaza cualquier valor falso

?? → reemplaza solamente null o undefined
```

---

# Ejercicio Guiado

```javascript
const nombre = "Ana";
let edad = 15;
let estudiante = true;

console.log(nombre);
console.log(edad);
console.log(estudiante);
```

---

# Mini Reto Individual

### Ejercicio 1

Crear variables:

```javascript
nombre
edad
ciudad
```

y mostrarlas en consola.

---

### Ejercicio 2

Crear:

```javascript
let nota = 80;
```

Mostrar:

```text
Aprobado
```

si la nota es mayor o igual a 60.

---

### Ejercicio 3

```javascript
let usuario = "";
```

Mostrar:

```text
Invitado
```

utilizando `||`.

---

### Ejercicio 4

Analizar el siguiente código:

```javascript
let dato = 10;

console.log(typeof dato);

dato = "Hola";

console.log(typeof dato);

dato = false;

console.log(typeof dato);
```

Explicar por qué los resultados son:

```text
number
string
boolean
```
