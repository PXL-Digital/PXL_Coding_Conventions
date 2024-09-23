# CSS

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

| Definitie        | Beschrijving                                                                                                                           | Voorbeeld              |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------- | ---------------------- |
| Pascal Casing    | De eerste letter van elk woord is met een hoofdletter geschreven en andere letters staan in kleine letters.                            | `NewBachelorStudent`   |
| Camel Casing     | De eerste letter van elk woord, behalve het eerste woord, is met een hoofdletter geschreven en andere letters staan in kleine letters. | `newBachelorStudent`   |
| Upper Snake Case | Alle letters zijn in hoofdletters geschreven en woorden worden gescheiden door een underscore.                                         | `MAX_STUDENTS`         |
| Kebab Case       | Alle letters zijn in kleine letters geschreven en woorden worden gescheiden door een koppelteken.                                      | `new-bachelor-student` |

## Conventies

### Selector

Gebruik Kebab Case voor selectors.

```css
.my-selector {
  /* properties here */
}
```

en **NIET**:

```css
.mySelector {
  /* properties here */
}
```

### Gebruik classes in plaats van ID's voor styling

```css
.my-selector {
  /* properties here */
}
```

en **NIET**

```css
#my-selector {
  /* properties here */
}
```

### Vermijd `!important`

`!important` maakt het moeilijk om de CSS te overschrijven. Gebruik het alleen als het écht nodig is.
Écht nodig betekent dat je een inline style overschrijft of een third-party library. Aangezien we niet werken met inline styles, is het enkel nodig wanneer je een third-party library overschrijft.

**NIET** doen:

```css
.my-selector {
  color: red !important;
}
```

### Gebruik CSS Custom Properties

CSS Custom Properties (ook bekend als CSS-variabelen) zijn variabelen die je in je CSS kunt definiëren en hergebruiken.

```css
:root {
  --primary-color: #c0ffee;
  --on-primary-color: #000000;

  --secondary-color: #4f81bd;
  --on-secondary-color: #ffffff;
}

.primary {
  background-color: var(--primary-color);
  color: var(--on-primary-color);
}

button {
  background-color: var(--primary-color);
  color: var(--on-primary-color);
}

.secondary {
  background-color: var(--secondary-color);
  color: var(--on-secondary-color);
}
```

en **NIET**:

```css
.primary {
  background-color: #c0ffee;
  color: #000000;
}

button {
  background-color: #c0ffee;
  color: #000000;
}

.secondary {
  background-color: #4f81bd;
  color: #ffffff;
}
```
