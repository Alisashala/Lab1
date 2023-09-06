# Obligatorisk 1

## Øvelse 2
##### Endpoint: https://api.dropboxapi.com/2/files/create_folder 
##### HTTP verb: POST 

##### Body:
{
    "path": "/TestMappe"
}

##### Kommentar: I Postman, i body-sektionen, har jeg angivet JSON-data for at specificere mappens navn. Dette har oprettet en mappe med navnet "TestMappe" i mit Dropbox-konto.

## Øvelse 3

##### Endpoint: https://api.dropboxapi.com/2/files/get_metadata

##### HTTP-verb: POST (mens GET bruges til at hente data, var dette ikke en mulighed da den ikke returnerede det rigtige JSON svar. Vi spurgte derfor chatGPT, og fik at vide, at nogle API'er, som Dropbox, bruger POST i stedet for GET, pga. sikkerhedsmæssige årsager, dermed gik vi videre med det 🙂 )

##### Body request: {
    "path": "/TestMappe"
}

Body response: 
{
    ".tag": "folder",
    "name": "TestMappe",
    "path_lower": "/testmappe",
    "path_display": "/TestMappe",
    "id": "id:cDODuX3Ank0AAAAAAAAXhQ"
}

##### status code: 200 ok

##### Er flowet i overenstemmelse med princippet om "uniform interface" i REST principperne?
- Jeg mener at flowet er i overensstemmelse med princippet om "uniform interface" i REST principperne, selvom jeg ikke bruger det "korrekte" HTTP-verb. Det tillod den mig ikke :( 

## Øvelse 4
##### Endpoint = https://content.dropboxapi.com/2/files/upload
##### HTTP verb = POST

##### Beskrivelse: Filen blev uploadet ved at sende en POST-forespørgsel til det angivne endpoint med en gyldig "Bearer Token" i "Authorization"-headeren. Filtypen blev angivet som "application/octet-stream," og filen blev inkluderet som binær data i requestens krop. Mappenavnet og filnavnet blev specificeret i "Dropbox-API-Arg"-headeren, og filen blev derefter uploadet til "TestMappe" i Dropbox.
