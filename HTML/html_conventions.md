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

### Minimale HTML-structuur

```html
<!doctype html>
<html lang="nl">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <!-- Page content goes here -->
  </body>
</html>
```

- `lang="nl"`: Gebruik de juiste taalcode voor de taal van de pagina.
- meta viewport: Zorgt ervoor dat de pagina correct wordt weergegeven op mobiele apparaten.

### Tags

Gebruik kleine letters voor tag- en attribuutnamen.

```html
<p class="intro">Dit is een paragraaf.</p>
```

en **NIET**:

```
<P CLASS="intro">Dit is een paragraaf.</P>
```

### Self-closing tags

Gebruik een schuine streep aan het einde van een zelfsluitende tag.

```html
<img src="image.jpg" alt="Image" />
```

en **NIET**:

```html
<img src="image.jpg" alt="Image" />
```

### Uitlijning

Gebruik 2 spaties voor inspringing.

```html
<!doctype html>
<html lang="nl">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <!-- Page content goes here -->
  </body>
</html>
```

en **NIET**:

```
<!doctype html>
<html lang="nl">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Document</title>
</head>
<body>
<!-- Page content goes here -->
</body>
</html>
```

Plaats begin- en eindtags op dezelfde regel.

```html
<p class="intro">Dit is een paragraaf.</p>
```

Plaats begin- en eindtags onder elkaar als de inhoud meerdere regels bevat.

```html
<p class="intro">
  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Molestias odio
  inventore corrupti maxime quia fugiat ex, suscipit similique in id
  voluptatibus aperiam. Quisquam sit voluptate fugit cupiditate eos delectus
  repudiandae enim odio dolor iste id beatae rem placeat est, perferendis
  expedita sapiente quasi ratione illum laboriosam optio consequuntur. Eos, non!
</p>
```

### Quotes

Gebruik dubbele quotes voor attribuutwaarden.

```html
<img src="image.jpg" alt="Image" />
```

en **NIET**:

```
<img src='image.jpg' alt='Image' />
```

### Semantische HTML

Gebruik semantische HTML-elementen voor de juiste betekenis van de inhoud.

```html
<body>
  <header>
    <h1>Page Title</h1>
  </header>

  <main>
    <article>
      <h2>Article Title</h2>
      <p>Article content goes here.</p>
    </article>
  </main>

  <footer>
    <p>&copy; 2024</p>
  </footer>
</body>
```

en **NIET**:

```
<body>
  <div class="header">
    <h1>Page Title</h1>
  </div>

  <div class="main">
    <div class="article">
      <h2>Article Title</h2>
      <p>Article content goes here.</p>
    </div>
  </div>

  <div class="footer">
    <p>&copy; 2024</p>
  </div>
</body>
```
