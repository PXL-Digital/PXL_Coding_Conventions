# Java

## Introductie

Programmeren volgens strikte richtlijnen heeft een aantal voordelen: 
- de code is leesbaar voor elk teamlid; 
- daardoor wordt de code ook beter onderhoudbaar; 
- en geeft de volledige code een professionele indruk; 

## Definities

| Definitie      | Beschrijving | Voorbeeld |
| ---        |    ----  |    ----  |
| Pascal Casing | De eerste letter van elk woord is met een hoofdletter geschreven en andere letters staan in kleine letters. | NewBachelorStudent |
| Camel Casing   | De eerste letter van elk woord, behalve het eerste woord, is met een hoofdletter geschreven en andere letters staan in kleine letters. | newBachelorStudent |

## Conventies

### CC-01 Gebruik Pascal Casing voor klassenamen

```java
public class BachelorStudent {
}
```

### CC-02 Gebruik Camel Casing voor methodenamen

```java
public void drawLogo(int xPosition, int yPosition) {
	// CODE COMES HERE
} 
```


### CC-03 Gebruik Camel Casing voor variabelen en methode parameters

```java
public void drawLogo(int xPosition, int yPosition) {     
    Color randomColor = ...;
}
``` 

### CC-04 Gebruik geen Hongaarse notatie om variabelen te benoemen

 Vroeger was het de gewoonte om een variabele benoemen met een prefix waaruit het type duidelijk wordt. Soms gebruikt men ook een prefix m_ om aan te geven dat het om een membervariabele gaat. Ook dit is niet toegelaten. 

```java
 int nAge;     //VERBODEN 
 string sName; //VERBODEN
 int m_age;    //VERBODEN 
 ```


### CC-05 Gebruik betekenisvolle namen voor klassen, methoden en variabelen.

Geen afkortingen! 

```java
String address; 
int salary;
```
Niet in orde: 
```java
String addr; 
int sal; 
```

### CC-06 Gebruik geen variabelenamen die bestaan uit één karakter

Geen i, n, s enz. Maar wel index, temp, enz. 
Een uitzondering kan voor lusvariabelen: 

```java
for (int i = 0; i < count; i++) {
    // CODE COMES HERE
} 
```


### CC-07 Gebruik hoofdletters en _ als scheidingsteken tussen woorden voor constantevariabelen

```java
static final int MIN_WIDTH = 4; 
static final int MAX_WIDTH = 8; 
```
 
### CC-08 Plaats accolades { } na en onder het statement, netjes uitgelijnd

```java
 if (filled) {     
 	rectangle.fill(brush);
 } else {     
 	rectangle.fill(null); 
 }
 ``` 

 en  **NIET**: 
 
 ```java
 if (filled) 
 {     
 	rectangle.fill(brush);
 } else 
 {     
 	rectangle.fill(null); 
 } 
 ``` 

### CC-09 Gebruik een aparte lijn per declaratie voor variabelen van hetzelfde type

```java
 int level; 
 int size;
```  

en **NIET**: 

```java
int level, size; 
```

### CC-10 Verkies maximaal één publieke klasse per bestand

 Het bestand krijgt dezelfde naam als de klasse met extensie `.java`. Bijvoorbeeld: `BachelorStudent.java` 

### CC-11 Streaming API: schrijf elke operatie op een nieuwe lijn

Een filter met een map uitvoeren op de Streaming API? Elke operatie op een nieuwe regel om de **leesbaarheid** te vergroten. 

```java
Arrays.asList(1, 2, 3, 4).stream()
    .filter(n -> n % 2 == 0)
    .map(n -> n * n)
    .toList()
```

en **NIET**:

```java
Arrays.asList(1, 2, 3, 4).stream().filter(n -> n % 2 == 0).map(n -> n * n).toList()
```

### CC-12 Unit test naming guidelines: methode_conditie_verwachting

Werk een duidelijk leesbare logische zin uit die als methodenaam dient voor een unittest waarin drie elementen zijn verwerkt: welke methode is er onder test, wat is de conditie, en wat is de verwachting.

```java
@Test
void calculate_oneOfBothNumbersIsNegative_throwsIllegalArgumentEx() {
    assertThrows(IllegalArgumentException.class, () -> calculate(1, -5));
}
@Test
void calculate_bothNumbersArePositive_returnsMultipliedNumber() {
    assertEquals(8, calculate(2, 4));
}
```

en **NIET** een onduidelijke namen die niet beschrijven wat de verwachting is:

```java
@Test
void calculateTest1() {
    // ...
}
```

## Referenties

[1] [Java Coding Conventions](http://www.oracle.com/technetwork/java/codeconventions-150003.pdf)

[2] R. C. Martin, "Clean Code: A Handbook of Agile Software Craftsmanship," Prentice Hall, 2008.

[3] [Google's Java Coding Conventions Guideline](https://google.github.io/styleguide/javaguide.html)
