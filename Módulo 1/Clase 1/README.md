# Clase 1: Introducción a JavaScript

---

# ¿Qué es JavaScript?

JavaScript es el lenguaje que da comportamiento a las páginas web.

| Tecnología | Función        |
| ---------- | -------------- |
| HTML       | Estructura     |
| CSS        | Apariencia     |
| JavaScript | Comportamiento |

---

# ¿Dónde se ejecuta?

## Navegador

Tiene acceso a:

* HTML
* Botones
* Formularios
* Ventanas (`window`)

```javascript
alert("Hola");
```

---

## Node.js

Se ejecuta fuera del navegador.

```javascript
console.log("Hola desde Node");
```

Se utiliza para:

* Servidores
* APIs
* Automatización

---

# 👋 Hola Mundo

```javascript
console.log("Hola Mundo");
```

Salida:

```text
Hola Mundo
```

---

# 🔥 El gran cambio: C++ vs JavaScript

## C++ → Tipado Estático

```cpp
int edad = 15;
```

❌ Esto produce error:

```cpp
edad = "Hola";
```

La variable tiene un tipo fijo.

---

## JavaScript → Tipado Dinámico

```javascript
let edad = 15;

edad = "Hola";

edad = true;
```

✅ Es válido.

Una variable puede cambiar de tipo.

---

# typeof

Permite saber el tipo de un dato.

```javascript
let dato = 10;

console.log(typeof dato);
```

Salida:

```text
number
```

---

```javascript
dato = "Hola";

console.log(typeof dato);
```

Salida:

```text
string
```

---

## Tipos que veremos

| Tipo      | Ejemplo            |
| --------- | ------------------ |
| String    | `"Juan"`           |
| Number    | `25`, `3.14`       |
| Boolean   | `true`, `false`    |
| Null      | `null`             |
| Undefined | variable sin valor |

---

# 📦 Variables

## let

Se utiliza cuando el valor puede cambiar.

```javascript
let edad = 15;

edad = 16;
```

---

## const

Se utiliza cuando el valor NO debe cambiar.

```javascript
const PI = 3.1416;
```

❌ Error:

```javascript
PI = 5;
```

---

# Regla rápida

```text
¿Va a cambiar?

Sí → let
No → const
```

---

# ➕ Operadores aritméticos

```javascript
+
-
*
/
%
```

Ejemplo:

```javascript
let a = 10;
let b = 5;

console.log(a + b);
```

Salida:

```text
15
```

---

# 🔍 Comparación

Mayor que

```javascript
10 > 5
```

```text
true
```

---

Menor que

```javascript
10 < 5
```

```text
false
```

---

Igualdad estricta

```javascript
5 === 5
```

```text
true
```

---

## ⚠ Siempre preferir

```javascript
===
```

sobre

```javascript
==
```

Porque también compara el tipo.

```javascript
"5" == 5
```

Resultado:

```text
true
```

---

```javascript
"5" === 5
```

Resultado:

```text
false
```

---

# 🚀 Operadores modernos

---

## OR ||

Si el valor de la izquierda es falso, utiliza el de la derecha.

```javascript
let nombre = "";

console.log(nombre || "Invitado");
```

Salida:

```text
Invitado
```

---

### Valores falsos (Falsy)

```javascript
false
0
""
null
undefined
NaN
```

---

## AND &&

Solo ejecuta la derecha si la izquierda es verdadera.

```javascript
let logueado = true;

logueado && console.log("Bienvenido");
```

Salida:

```text
Bienvenido
```

---

Equivale a:

```javascript
if(logueado){
    console.log("Bienvenido");
}
```

---

## Nullish ??

Usa el valor de la derecha solo si el de la izquierda es:

* `null`
* `undefined`

```javascript
let nombre = null;

console.log(nombre ?? "Invitado");
```

Salida:

```text
Invitado
```

---

# Diferencia entre || y ??

```javascript
let puntos = 0;
```

Con `||`

```javascript
console.log(puntos || 100);
```

Salida:

```text
100
```

Porque `0` es falsy.

---

Con `??`

```javascript
console.log(puntos ?? 100);
```

Salida:

```text
0
```

Porque `0` sí existe.

---

# 📌 Resumen rápido

## Variables

```javascript
let nombre = "Juan";
const PI = 3.14;
```

---

## Saber el tipo

```javascript
typeof valor
```

---

## Comparación recomendada

```javascript
===
```

---

## Operadores modernos

```javascript
&&
```

Ejecuta si existe algo verdadero.

---

```javascript
||
```

Valor por defecto.

---

```javascript
??
```

Valor por defecto solo para `null` y `undefined`.

---

# 🧠 Mentalidad para quienes vienen de C++

### C++

```cpp
int edad = 15;
```

La variable es un entero para siempre.

---

### JavaScript

```javascript
let edad = 15;

edad = "quince";

edad = true;
```

Todo es válido.

> En JavaScript el tipo pertenece al valor, no a la variable.
