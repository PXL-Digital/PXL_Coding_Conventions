# REST
 
## Introductie
De stijlgids voor RESTful web services heeft als doel consistente REST APIs te ontwikkelen. De gids voorziet best practices en ontwerpregels voor het ontwikkelen van professionele web services.

## Conventies
### **CC-01 Naamgeving van resources**
Gebruik duidelijke en beschrijvende namen voor de resources, in het meervoud. Bijvoorbeeld <span style="color:green">/users</span> en niet <span style="color:red">/user</span>.

### **CC-02 HTTP Method: GET**
- Gebruik GET voor het opvragen van resources.
- Gebruik GET **NIET** om wijzigingen op de server aan te brengen.
- Gebruik queryparameters voor het filteren en sorteren van gegevens.
- Implementeer paginering voor grote hoeveelheden resources met behulp van queryparameters (bijvoorbeeld ?limit=10&offset=20) indien dit wordt gevraagd in de opgave.
- Gebruik HTTP statuscode 200 voor een succesvolle respons.

### **CC-03 HTTP Method: POST**
- Gebruik POST om nieuwe resources aan te maken of om een operatie te triggeren.
- Voeg de nodige gegevens in JSON-formaat toe aan het request.
- Het succesvol aanmaken van een nieuwe resource resulteert in statuscode 201 samen met de locatie van de zojuist aangemaakte resource.
- Bij een POST van een operatie die geen resource aanmaakt, is de respons bij succes 200.

### **CC-04 HTTP Method: PUT**
- Gebruik PUT om een resource bij te werken.  
- Voeg alle gegevens van de resource toe aan het request in JSON-formaat.
- Geef een statuscode 200 terug voor een succesvolle update.
- Geef de gewijzigde resource terug mee in het respons.

### **CC-05 HTTP Method: DELETE**
- Gebruik DELETE om een resource te verwijderen.
- Geef statuscode 204 (Geen Inhoud) terug voor een succesvolle verwijdering.

### **CC-06 JSON**
- Gebruik JSON-formaat voor request en respons tenzij anders vermeld.

### **CC-07 HTTP status codes**
- Gebruik standaard HTTP-statuscodes om de uitkomst van een request aan te geven 
	- 200 voor succes
	- 400 voor cliëntfouten
	- 500 voor serverfouten
- Bied informatieve foutberichten in het respons bij fouten.

### **CC-08 Authenticatie en Autorisatie**
Implementeer passende authenticatie- en autorisatiemechanismen, zoals JWT of OAuth2, indien dit wordt gevraagd in opdracht.

### **CC-09 Documentatie**
Lever API-documentatie met behulp van tools zoals Swagger of OpenAPI.
