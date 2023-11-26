# REST-API---blog-wa-aws

API Endpointy
1. Vytvoření nového blog příspěvku
URL: /api/blog

Metoda: POST

Formát požadavku: JSON

Příklad požadavku:

json
Copy code
{
  "content": "Obsah blog příspěvku",
  "createdAt": "2023-11-26T12:00:00",
  "author": "Jmeno Autora"
}
Odpověď:

json
Copy code
{
  "id": "unikátní-identifikátor"
}
2. Zobrazení všech blog příspěvků
URL: /api/blog

Metoda: GET

Odpověď:

json
Copy code
[
  {
    "id": "unikátní-identifikátor-1",
    "content": "Obsah blog příspěvku 1",
    "createdAt": "2023-11-26T12:00:00",
    "author": "Jmeno Autora 1"
  },
  {
    "id": "unikátní-identifikátor-2",
    "content": "Obsah blog příspěvku 2",
    "createdAt": "2023-11-27T14:30:00",
    "author": "Jmeno Autora 2"
  }
]
3. Zobrazení konkrétního blog příspěvku
URL: /api/blog/:blogId

Metoda: GET

Odpověď:

json
Copy code
{
  "id": "unikátní-identifikátor",
  "content": "Obsah blog příspěvku",
  "createdAt": "2023-11-26T12:00:00",
  "author": "Jmeno Autora"
}
4. Smazání konkrétního blog příspěvku
URL: /api/blog/:blogId
Metoda: DELETE
Odpověď: 204 No Content
5. Částečná aktualizace konkrétního blog příspěvku
URL: /api/blog/:blogId

Metoda: PATCH

Formát požadavku: JSON

Příklad požadavku:

json
Copy code
{
  "content": "Nový obsah blog příspěvku"
}
Odpověď:

json
Copy code
{
  "id": "unikátní-identifikátor",
  "content": "Nový obsah blog příspěvku",
  "createdAt": "2023-11-26T12:00:00",
  "author": "Jmeno Autora"
}
Autentizace
Aplikace vyžaduje autentizaci pro přístup k některým endpointům. Přidejte hlavičku Authorization s platným JWT tokenem k požadavkům.

Licence
Tato aplikace je poskytována pod licencí MIT License.
