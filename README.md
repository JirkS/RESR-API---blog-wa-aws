# REST-API - blog wa aws

adresa: http://16.16.68.180:5000/<br />
API Endpointy

### 1. Vytvoření nového blog příspěvku
- URL: /api/blog
- Metoda: POST
- Formát požadavku: JSON
Příklad požadavku (json):<br />
{<br />
    "title":"nazev",<br />
    "content":"obsah",<br />
    "author_id":"id cislo autora"<br />
}<br />
Odpověď (json):<br />
{<br />
    "message": "Blog post created successfully"<br />
}<br />

### 2. Zobrazení všech blog příspěvků
- URL: /api/blog
- Metoda: GET
Odpověď (json):<br />
{<br />
    "post_id": "id",<br />
    "title": "nazev",<br />
    "content": "obsah",<br />
    "creation_date": "datum vytvoreni"<br />
    "author_id": "id autora"<br />
},<br />
{<br />
    "post_id": "id",<br />
    "title": "nazev",<br />
    "content": "obsah",<br />
    "creation_date": "datum vytvoreni"<br />
    "author_id": "id autora"<br />
}<br />
  
### 3. Zobrazení konkrétního blog příspěvku
- URL: /api/blog/blogId
- Metoda: GET
Odpověď (json):<br />
{<br />
    "post_id": "id",<br />
    "title": "nazev",<br />
    "content": "obsah",<br />
    "creation_date": "datum vytvoreni"<br />
    "author_id": "id autora"<br />
}<br />

### 4. Smazání konkrétního blog příspěvku
- URL: /api/blog/:blogId
- Metoda: DELETE
Odpověď (json): <br />
{<br />
    "message": "Blog post deleted successfully"<br />
}<br />

### 5. Částečná aktualizace konkrétního blog příspěvku
- URL: /api/blog/blogId
- Metoda: PATCH
- Formát požadavku: JSON
Příklad požadavku (json):<br />
{<br />
  "content": "Nový obsah blog příspěvku"<br />
}<br />
Odpověď (json):<br />
{<br />
    "message": "Blog post updated successfully"<br />
}<br />

## Autentizace
Aplikace vyžaduje autentizaci pro přístup k některým endpointům. Přidejte hlavičku Authorization s platným JWT tokenem k požadavkům.

## Licence
Tato aplikace je poskytována pod licencí MIT License.
