
# MongoDB Kolokwium - Grupa A


Sklep posiada produkty, które mają następujące właściwości:
- Nazwa produktu
- Cena
- Kategoria
- Ilość dostępna w magazynie
- Opis produktu
- Producent (zagnieżdżony dokument zawierający nazwę producenta, kraj i adres (miasto, ulica))
- Recenzje (tablica zagnieżdżonych dokumentów zawierających użytkownika, ocenę i komentarz)


## Zadanie 1: Komendy CRUD i Wyszukiwanie

Wykonaj następujące operacje CRUD i wyszukiwanie na bazie danych MongoDB dla kolekcji "produkty":

a) Wstaw nowy dokument do kolekcji "produkty":
```json
{
    "nazwa": "Laptop ABC",
    "cena": 3000,
    "kategoria": "Elektronika",
    "ilosc": 10,
    "opis": "Wysokiej jakości laptop z procesorem Intel i7",
    "producent": {
        "nazwa": "TechCorp",
        "kraj": "USA",
        "adres": {
            "miasto": "San Francisco",
            "ulica": "Market Street"
        }
    },
    "recenzje": [
        {
            "uzytkownik": "Jan Kowalski",
            "ocena": 5,
            "komentarz": "Świetny laptop!"
        },
        {
            "uzytkownik": "Anna Nowak",
            "ocena": 4,
            "komentarz": "Bardzo dobry, ale bateria mogłaby być lepsza."
        }
    ]
}
```

b) Zaktualizuj dokument, zmieniając cenę produktu "Laptop ABC" na 2800.

c) Usuń dokument, w którym ilość produktu jest mniejsza niż 5.

## Zadanie 2: Wyszukiwanie

d) Znajdź wszystkie produkty z kategorii "Elektronika".

e) Znajdź wszystkie produkty, których producent pochodzi z USA.

f) Znajdź wszystkie produkty, które mają ocenę recenzji równą 5.

## Zadanie 3: Agregacje

Skorzystaj z frameworku agregacji, aby wykonać następujące zadania na kolekcji "produkty":

a) Oblicz średnią cenę produktów w każdej kategorii.

b) Znajdź trzy najdroższe produkty w kolekcji.

c) Oblicz średnią ocenę dla każdego produktu.

d) Zlicz liczbę produktów w każdej kategorii.

e) Znajdź produkty, które mają więcej niż jedną recenzję.

## Instrukcje Dodatkowe

- Do wykonania operacji CRUD użyj komend MongoDB: `insertOne()`, `updateOne()`, `deleteMany()`, `find()`.
- Do operacji agregacyjnych użyj komendy `aggregate()`.
