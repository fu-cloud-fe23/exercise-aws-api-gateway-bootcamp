# AWS API Gateway Bootcamp

## Kortleks-API
Skapa ett API där du kan hantera en kortlek med följande metoder:

### Skapa kortlek

```
/deck/create - GET
```

Vid detta anrop skall en kortlek skapas upp i den anropade lambdafunktionen, och returneras som ett deck-objekt. Varje objekt skall ha följandde utformning:

```
{
  value : 2,
  suit : "hearts",
  card : "2 of Hearts"
}
```

### Blanda kortlek

```
/deck/shuffle - POST
```

Vid detta anrop skall hela kortleken som skapades upp i föregående anrop skickas med i din requests body enligt följande utformning:

```
{
  deck : [...]
}
```

### Hämta alla kort med ett visst värde

```
/deck/{value} - POST
```

Vid detta anrop skall hela kortleken skickas med i din requests body. Du skall därefter använda din angivna parameter för att hämta ut alla kort i kortleken med samma värde som du angett.

## Todo API - Veckans Code Review Uppgift
Koda om ditt Todo API från förra veckan, men använd dig denna gång av API Gateway. Eftersom dina lambdafunktioner inte kan dela kod med varandra så Får du "hårdkoda" in 3-5 todouppgifter i varje funktion som du kan leka med. Följande routes skall finnas med:

```
/api/todos - GET
```

```
/api/todos/{id} - GET
```

```
/api/todos - POST
```

```
/api/todos/{id} - PUT
```

```
/api/todos/{id} - DELETE
```

Vid de tre sista anropen skall den nya todolistan skickas med i response för att säkerställa att anropet lyckats.

