# REST-API - blog wa aws

API Endpointy

### 1. Vytvoření nového blog příspěvku
- URL: /api/blog
- Metoda: POST
- Formát požadavku: JSON
Příklad požadavku (json):
{__
    "title":"nazev",__
    "content":"obsah",__
    "author_id":"id cislo autora"__
}__
Odpověď (json):
{
    "message": "Blog post created successfully"
}

### 2. Zobrazení všech blog příspěvků
- URL: /api/blog
- Metoda: GET
Odpověď (json):
{
    "post_id": "id",
    "title": "nazev",
    "content": "obsah",
    "creation_date": "datum vytvoreni"
    "author_id": "id autora"
},
{
    "post_id": "id",
    "title": "nazev",
    "content": "obsah",
    "creation_date": "datum vytvoreni"
    "author_id": "id autora"
}
  
### 3. Zobrazení konkrétního blog příspěvku
- URL: /api/blog/blogId
- Metoda: GET
Odpověď (json):
{
    "post_id": "id",
    "title": "nazev",
    "content": "obsah",
    "creation_date": "datum vytvoreni"
    "author_id": "id autora"
}

### 4. Smazání konkrétního blog příspěvku
- URL: /api/blog/:blogId
- Metoda: DELETE
Odpověď (json): 
{
    "message": "Blog post deleted successfully"
}

### 5. Částečná aktualizace konkrétního blog příspěvku
- URL: /api/blog/blogId
- Metoda: PATCH
- Formát požadavku: JSON

Příklad požadavku (json):
{
  "content": "Nový obsah blog příspěvku"
}
Odpověď (json):
{
    "message": "Blog post updated successfully"
}

## Autentizace
Aplikace vyžaduje autentizaci pro přístup k některým endpointům. Přidejte hlavičku Authorization s platným JWT tokenem k požadavkům.

## Licence
Tato aplikace je poskytována pod licencí MIT License.
