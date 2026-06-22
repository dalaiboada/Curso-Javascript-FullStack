# Clase 2: Control de Flujo y Estructuras de Datos

# Control de Flujo

## if / else

```js
let edad = 18;

if (edad >= 18) {
    console.log("Mayor de edad");
} else {
    console.log("Menor de edad");
}
```

## switch

```js
let opcion = 2;

switch (opcion) {
    case 1:
        console.log("Inicio");
        break;

    case 2:
        console.log("Configuración");
        break;

    default:
        console.log("Opción inválida");
}
```

---

# Bucles

## for

```js
for (let i = 0; i < 5; i++) {
    console.log(i);
}
```

### Recorrer un arreglo

```js
let frutas = ["Manzana", "Pera", "Mango"];

for (let i = 0; i < frutas.length; i++) {
    console.log(frutas[i]);
}
```

---

## while

```js
let i = 0;

while (i < 5) {
    console.log(i);
    i++;
}
```

---

## do while

```js
let i = 0;

do {
    console.log(i);
    i++;
} while (i < 5);
```

---

# Arrays

## Crear un arreglo

```js
let numeros = [10,20,30];
```

```text
Índices

0 → 10
1 → 20
2 → 30
```

## Acceder a un elemento

```js
numeros[0]
```

Resultado:

```js
10
```

## Agregar elementos

### push()

```js
numeros.push(40);
```

```js
[10,20,30,40]
```

### Eliminar último elemento

```js
numeros.pop();
```

## Tamaño del arreglo

```js
numeros.length
```

---

# Objetos Literales

## Crear un objeto

```js
let persona = {
    nombre: "Carlos",
    edad: 25,
    activo: true
};
```

## Acceder a propiedades

### Notación punto

```js
persona.nombre
```

### Notación corchetes

```js
persona["edad"]
```

## Modificar propiedades

```js
persona.edad = 26;
```

## Agregar propiedades

```js
persona.ciudad = "Caracas";
```

Resultado:

```js
{
    nombre: "Carlos",
    edad: 26,
    activo: true,
    ciudad: "Caracas"
}
```

## Eliminar propiedades

```js
delete persona.activo;
```

---

# Arrays de Objetos

```js
let productos = [
    {
        nombre: "Laptop",
        precio: 800
    },
    {
        nombre: "Mouse",
        precio: 20
    }
];
```

Acceder:

```js
productos[0].nombre
```

Resultado:

```js
Laptop
```

## Recorrer

```js
for (let i = 0; i < productos.length; i++) {
    console.log(productos[i].nombre);
}
```

---

# Map

## Crear

```js
let usuarios = new Map();
```

## Agregar

```js
usuarios.set("admin", "Carlos");
usuarios.set("editor", "Ana");
```

## Obtener

```js
usuarios.get("admin");
```

Resultado:

```js
Carlos
```

## Eliminar

```js
usuarios.delete("editor");
```

## Cantidad de elementos

```js
usuarios.size
```

---

# Set

## Crear

```js
let numeros = new Set();
```

## Agregar

```js
numeros.add(10);
numeros.add(20);
numeros.add(10);
```

Resultado:

```js
Set(2) {10,20}
```

(No permite repetidos)

## Tamaño

```js
numeros.size
```

## Eliminar

```js
numeros.delete(20);
```

# Eliminar duplicados de un Array

### Array original

```js
let categorias = [
    "Audio",
    "Video",
    "Audio",
    "Monitores"
];
```

### Con Set

```js
let sinDuplicados = [...new Set(categorias)];
```

Resultado:

```js
["Audio","Video","Monitores"]
```

---

# Comparación rápida

| Estructura | Uso                   | Permite repetidos |
| ---------- | --------------------- | ----------------- |
| Array      | Lista ordenada        | ✅ Sí              |
| Object     | Representar entidades | ✅ Sí              |
| Map        | Almacenar clave-valor | ✅ Sí              |
| Set        | Valores únicos        | ❌ No              |

---

# Métodos importantes

## Arrays

| Método | Función               |
| ------ | --------------------- |
| push() | Agrega al final       |
| pop()  | Elimina el último     |
| length | Cantidad de elementos |

### Ejemplo

```js
frutas.push("Mango");
frutas.pop();
frutas.length;
```

---

## Objetos

| Operación | Ejemplo                    |
| --------- | -------------------------- |
| Leer      | persona.nombre             |
| Modificar | persona.edad = 30          |
| Agregar   | persona.ciudad = "Caracas" |
| Eliminar  | delete persona.edad        |

---

## Map

| Método   | Función  |
| -------- | -------- |
| set()    | Agregar  |
| get()    | Obtener  |
| delete() | Eliminar |
| size     | Cantidad |

---

## Set

| Método   | Función  |
| -------- | -------- |
| add()    | Agregar  |
| delete() | Eliminar |
| size     | Cantidad |

---

# Diferencias con C++

| C++                     | JavaScript            |
| ----------------------- | --------------------- |
| Arrays con tamaño fijo  | Arrays dinámicos      |
| Struct                  | Object                |
| std::map                | Map                   |
| std::set                | Set                   |
| Tipado estático         | Tipado dinámico       |
| Estructuras más rígidas | Estructuras flexibles |

---

# Conceptos que debes recordar

### Array

```js
["Juan", "Pedro", "Ana"]
```

➡️ Lista ordenada.

---

### Object

```js
{
    nombre: "Juan",
    edad: 20
}
```

➡️ Representa entidades.

---

### Map

```js
clave → valor
```

➡️ Colección clave-valor especializada.

---

### Set

```js
10,20,30
```

➡️ No permite valores repetidos.

---

# ⭐ Regla de oro

### Si piensas:

> "Tengo una lista"

Usa:

```js
[]
```

(Array)

---

> "Tengo una entidad con propiedades"

Usa:

```js
{}
```

(Object)

---

> "Necesito clave → valor"

Usa:

```js
new Map()
```

---

> "Necesito valores únicos"

Usa:

```js
new Set()
```
