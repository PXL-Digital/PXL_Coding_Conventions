# JavaScript

## Introductie

Programmeren volgens strikte richtlijnen heeft een aantal voordelen:

- de code is leesbaar voor elk teamlid;
- daardoor wordt de code ook beter onderhoudbaar;
- en geeft de volledige code een professionele indruk;

## Voertaal

Programmeren doe je vaak in een internationaal team. Daarom kiezen we voor
Engels als voertaal in je broncode. Dit betekent dat je alle benamingen (van
klassen, variabelen, methodes, properties, enz.) en ook je commentaar in je
code in het Engels schrijft.

## Definities

| Definitie        | Beschrijving                                                                                                                           | Voorbeeld            |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------- | -------------------- |
| Pascal Casing    | De eerste letter van elk woord is met een hoofdletter geschreven en andere letters staan in kleine letters.                            | `NewBachelorStudent` |
| Camel Casing     | De eerste letter van elk woord, behalve het eerste woord, is met een hoofdletter geschreven en andere letters staan in kleine letters. | `newBachelorStudent` |
| Upper Snake Case | Alle letters zijn in hoofdletters geschreven en woorden worden gescheiden door een underscore.                                         | `MAX_STUDENTS`       |

## Conventies

Om consistentie in de code te garanderen, volgen we de [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript). Gebruik deze style guide als referentie voor het schrijven van JavaScript-code.

Deze conventies kunnen automatisch gecontroleerd worden, zie [Configuratie IDE](./configuratie_ide.md).

De belangrijkste conventies staan hieronder opgesomd. Twijfel je over een bepaalde conventie, raadpleeg dan de volledige [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript).

### Gebruik Camel Casing voor variabelen, functies en instanties

```javascript
const bachelorStudent = {};
function drawLogo() {}
```

Uitzondering: Upper Snake Case voor globale constanten.

```javascript
const MAX_STUDENTS = 30;
```

### Gebruik Pascal Casing voor klassen en constructors

```javascript
class BachelorStudent {
  constructor() {}
}

const newBachelorStudent = new BachelorStudent();
```

### Gebruik betekenisvolle namen

```javascript
const width = 10;
const height = 20;
const area = width * height;

function calculateArea(width, height) {
  return width * height;
}
```

en **NIET**:

```javascript
// niet doen
const x = 10;
const y = 20;
const z = x * y;

function q(w, h) {
  return w * h;
}
```

Uitzondering: Gebruik korte namen voor tellers in loops.

```javascript
for (let i = 0; i < 10; i++) {
  // CODE COMES HERE
}
```

Uitzondering: Gebruiker korte namen in lambda functies.

```javascript
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter((n) => n % 2 === 0);
```

### Plaats accolades op dezelfde regel

```javascript
function drawLogo() {
  // CODE COMES HERE
}
```

In andere programmeertalen, zoals C#, worden accolades vaak op een nieuwe regel geplaatst. In JavaScript is het gebruikelijk om accolades op dezelfde regel te plaatsen.

### Gebruik `const` en `let` in plaats van `var`

```javascript
const width = 10;
let height;
height = 20;
```

en **NIET**:

```javascript
var width = 10;
var height;
height = 20;
```

> Waarom? `const` en `let` zijn block-scoped, terwijl `var` function-scoped is.

### Gebruik `===` in plaats van `==`

Gebruik altijd `===` in plaats van `==` en `!==` in plaats van `!=`.

```javascript
if (age === 10) {
  // CODE COMES HERE
}

if (age !== 10) {
  // CODE COMES HERE
}
```

```javascript
if (age == 10) {
  // CODE COMES HERE
}

if (age != 10) {
  // CODE COMES HERE
}
```

> Waarom? `===` en `!==` vergelijken de waarde en het type, terwijl `==` en `!=` alleen de waarde vergelijken.

### Gebruik een aparte lijn per declaratie voor variabelen

```javascript
let level;
let size;
```

en **NIET**:

```javascript
let level, size;
```

## Referenties

1. [Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript)
   1. [Types](https://github.com/airbnb/javascript#types)
   1. [References](https://github.com/airbnb/javascript#references)
   1. [Objects](https://github.com/airbnb/javascript#objects)
   1. [Arrays](https://github.com/airbnb/javascript#arrays)
   1. [Destructuring](https://github.com/airbnb/javascript#destructuring)
   1. [Strings](https://github.com/airbnb/javascript#strings)
   1. [Functions](https://github.com/airbnb/javascript#functions)
   1. [Arrow Functions](https://github.com/airbnb/javascript#arrow-functions)
   1. [Classes & Constructors](https://github.com/airbnb/javascript#classes--constructors)
   1. [Modules](https://github.com/airbnb/javascript#modules)
   1. [Iterators and Generators](https://github.com/airbnb/javascript#iterators-and-generators)
   1. [Properties](https://github.com/airbnb/javascript#properties)
   1. [Variables](https://github.com/airbnb/javascript#variables)
   1. [Hoisting](https://github.com/airbnb/javascript#hoisting)
   1. [Comparison Operators & Equality](https://github.com/airbnb/javascript#comparison-operators--equality)
   1. [Blocks](https://github.com/airbnb/javascript#blocks)
   1. [Control Statements](https://github.com/airbnb/javascript#control-statements)
   1. [Comments](https://github.com/airbnb/javascript#comments)
   1. [Whitespace](https://github.com/airbnb/javascript#whitespace)
   1. [Commas](https://github.com/airbnb/javascript#commas)
   1. [Semicolons](https://github.com/airbnb/javascript#semicolons)
   1. [Type Casting & Coercion](https://github.com/airbnb/javascript#type-casting--coercion)
   1. [Naming Conventions](https://github.com/airbnb/javascript#naming-conventions)
   1. [Accessors](https://github.com/airbnb/javascript#accessors)
   1. [Events](https://github.com/airbnb/javascript#events)
