# Quiz JS

<img src="https://res.cloudinary.com/juancms98/image/upload/v1635658504/javascript-1_akpi8w.svg" width="700" heigth="700">

## 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

**1. ¿Qué es una variable y para qué sirve?**

R.- Una variable es un espacio en memoria que se almacena y sirve para almacenar cualquier valor que pueda ser utilizado más adelante.

**2. ¿Cuál es la diferencia entre declarar e inicializar una variable?**

R.- Declarar una variable signifca que esa variable estará sin un valor definido hasta que sea inicializado con una asignación, ejemplo: let saludo; (declarada), saludo = "hola" (inicializada).

**3. ¿Cuál es la diferencia entre sumar números y concatenar strings?**

R.- Se necesita que las variables sean del mismo tipo de datos, ya que cuando el operador (+) se encuentra junto tipos de datos distintos, el lenguaje hace una coerción.

**4. ¿Cuál operador me permite sumar o concatenar?**

R.- El operador encargado en sumar y/o concatenar es el operador de más (+).

## 2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

- Nombre = string

- Apellido = string

- Nombre de usuario en Platzi = string

- Edad = number

- Correo electrónico = string

- Mayor de edad = boolean

- Dinero ahorrado = number

- Deudas = number

## 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

let nombre = "Juan", apellido = "Montilla", usuarioPlatzi = "juancms98", edad = 23, email = "montillasanchezjuancarlos@gmail.com", mayorDeEdad = true, dineroAhorrado= 500, deudas = 160;

## 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

`` console.log(`Mi nombre completo es: ${nombre} ${apellido}`); ``

`console.log(dineroAhorrado - deudas);`

# Funciones:

## 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

**1. ¿Qué es una función?**

R.- Una función es un bloque de código que realiza alguna operación.

**2. ¿Cuándo me sirve usar una función en mi código?**

R.- Cuando el código sea repetitivo o una instrucción sea realizada a largo plazo y se pasarían argumentos para cambiar los valores de forma automatizada.

**3. ¿Cuál es la diferencia entre parámetros y argumentos de una función?**

R.- Los parámetros son definidos cuando se está creando la función, es decir, para indicar que recibirá ciertos datos.
Los argumentos son valores que recibe la función ya definidos y específicos.

## 2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```js
function fullName(name, lastname) {
  return name + " " + lastname;
}

function myPresentation(name, lastname, nickname) {
  const completeName = fullName(name, lastname);
  console.log(
    "Mi nombre es " +
      completeName +
      ", pero prefiero que me digas " +
      nickname +
      "."
  );
}

myPresentation("Juan", "Montilla", "juancms98");
```

# Condicionales

## 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

**¿Qué es un condicional?**

R.- Una condicional, como su nombre lo indica, es una condición que se aplica en bloque de códigos para comprobar si se cumple una instrucción o no: valores true: se cumple, valores false: no se cumple.

**¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?**

R.- Condicionales if, else if, else, condicionales oneline

- If: indica si se cumple la condición y finaliza si es verdadera o falso y retorna lo que está dentro del bloque de código.

- else if: se refiere si hay más de una condición a evaluar.

- Else: significa que si la condición que está entre paréntesis del if no se cumple, cualquier otra acción que coloques dentro de ese bloque de código se realizará.

**¿Puedo combinar funciones y condicionales?**

R.- Sí, si se puede unir condiciones dentro de las funciones y nos permite evaluar que en las funciones se cumplan

## 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```js
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
  case "Free":
    console.log("Solo puedes tomar los cursos gratis");
    break;
  case "Basic":
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
    break;
  case "Expert":
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
    break;
  case "ExpertPlus":
    console.log(
      "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"
    );
    break;
}

const tipoDeSuscripcion = "Basic";

if (tipoDeSuscripcion != "Basic") {
  if (tipoDeSuscripcion === "Free") {
    console.log("Solo puedes tomar los cursos gratis");
  } else if (tipoDeSuscripcion === "Expert") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
  } else if (tipoDeSuscripcion === "ExpertPlus") {
    console.log(
      "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"
    );
  }
} else {
  console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
}
```

## 3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

```js
function suscription(suscripcion) {
  if (suscripcion === "Free") {
    console.log("Solo puedes tomar los cursos gratis");
    return;
  }
  if (suscripcion === "Basic") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
    return;
  }
  if (suscripcion === "Expert") {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
    return;
  }
  if (suscripcion === "ExpertPlus") {
    console.log(
      "Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"
    );
    return;
  }

  console.warn("Esa suscripción no existe");
}
```

💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays u objetos y un solo condicional. 😏

```js
function suscripcion (index){

  const tipoSuscripcion = [
    {
     suscripcion : 'Free',
     message : 'Solo puedes tomar los cursos gratis',
    },
    {
     suscripcion : 'Basic',
     message : 'Puedes tomar casi todos los cursos de Platzi durante un mes',
    },
    {
     suscripcion : 'Expert',
     message : 'Puedes tomar casi todos los cursos de Platzi durante un año',
    },
    {
     suscripcion : 'ExpertPlus',
     message: 'Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año',
    }
]

const optFiltrada = tipoSuscripcion.filter(filtro => {
	if (filtro.suscripcion === index) {
		console.log(filtro.message);
	}
});

```

# Ciclos

## 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

**¿Qué es un ciclo?**

R.- Un ciclo es un bloque de código que se va a repetir siempre y cuando se cumpla una condición.

**¿Qué tipos de ciclos existen en JavaScript?**

R.- Los ciclos más populares son:

- for, while, do while, for each, for of.

**¿Qué es un ciclo infinito y por qué es un problema?**

R.- Un ciclo infinito es producido porque en la condición del ciclo no se le indica que hasta cierto punto deje de iterar y el problema hace que se llene el espacio en memoria y se trabe el programa. (😏 Tranquilo, hay programas que detectan un ciclo infinito y lo finalizan. El ejemplo claro es google chrome)

**¿Puedo mezclar ciclos y condicionales?**

R.- Sí, precisamente los ciclos tienen una condición inicial y se le puede "concatenar" más condiciones.

## 2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

```js
for (let i = 0; i < 5; i++) {
  console.log("El valor de i es: " + i);
}

let i = 0;

while (i < 5) {
  console.log("El valor de i es: " + i);
  i++;
}
```

```js
for (let i = 10; i >= 2; i--) {
console.log("El valor de i es: " + i);
}

let i = 10;

while (i >= 2){
  console.log("El valor de i es: " + i);
  i--
}

💡 //Debemos tener cuidado con el contador, ya que si se te olvidas caerás en el loop infinito.
```

## 3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

💡 Pista: puedes usar la función prompt de JavaScript.

```js
let respuesta;

while (respuesta != "4") {
  let pregunta = prompt("Cuánto es 2 + 2");
  respuesta = pregunta;
}
```

# Listas

## 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

**¿Qué es un array?**

R.- Un array es una matríz de elementos encapsulados que se separan por comas y pertenecen dentro de corchetes. Podemos llegar a su valor mediante su posición.

**¿Qué es un objeto?**

R.- Un objeto es una matriz de elementos encapsulados entre propiedades y su valor, estas se encuentran dentro de llaves y podemos llegar mediante su posición y/o propiedad.

**¿Cuándo es mejor usar objetos o arrays?**

R.- Si queremos tener una lista de valores y poder iterarla mediante un loop, lo recomendable es utilizar arrays pero si tenemos una lista donde su valor se almacena dentro de una propiedad, lo recomendable es utilizar objetos.

**¿Puedo mezclar arrays con objetos o incluso objetos con arrays?**

R.- Se puede mezclar un objeto con arrays, sí; como también se puede un array con un objeto.

## 2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

```js
function getArray(array) {
  if (Array.isArray(array) === false) {
    console.warn(
      `The get value as argument "${array}" isn't array, only allow array; check it.`
    );
  } else {
    let valueFirst = array[0];
    console.log(`The value first is: "${valueFirst}"`);
  }
}

getArray("i'm array"); // The get value as argument "i'm array" isn't array, only allow array; check it.
getArray([2, 3, 4, 5, 0]); // The value first is: "2"
```

## 3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

```js
// ARRAYS CON ciclo for of

function getArrayForSlice(array) {
  if (Array.isArray(array) === false) {
    console.warn(
      `The get value as argument "${array}" isn't array, only allow array; check it.`
    );
  } else {
    for (let elements of array) {
      console.log(`Value for one: ${elements}`);
    }
  }
}

getArrayForSlice([2, 3, 4, 5, 0]);

// ARRAYS CON ciclo for tradicional

function getArrayForSlice(array) {
  if (Array.isArray(array) === false) {
    console.warn(
      `The get value as argument "${array}" isn't array, only allow array; check it.`
    );
  } else {
    for (let i = 0; i < array.length; i++) {
      console.log("valor de arreglo: " + array[i]);
    }
  }
}

getArrayForSlice([2, 3, 4, 5, 0]);
```

## 4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

```js
function getObject(obj) {
  if (typeof obj != "object") {
    console.warn("check it be type object");
  } else {
    const arrayOfObject = Object.values(obj);
    for (let elements of arrayOfObject) {
      console.log(elements);
    }
  }
}
```

# Follow me in my social networks:

- [Linkedin](https://www.linkedin.com/in/juancodev/)
- [Twitter](https://twitter.com/juancodev_)
- [Facebook](https://www.facebook.com/juancodev)
- [Instagram](https://www.instagram.com/juancodev/)
- [My Web site](https://juancodev.github.io/Portfolio/)

![Logo](https://res.cloudinary.com/juancms98/image/upload/v1665415315/logo_omudfv.png)
<img src="https://res.cloudinary.com/juancms98/image/upload/v1630885661/juancms98_yzbssj.png" width="700" heigth="700">
