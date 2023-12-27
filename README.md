# Web Scraper - Books to Scrape

## Opis Projektu

Projekt ten jest prostym web scraperem napisanym w języku Python do zbierania informacji o książkach ze strony "Books to Scrape". Scraper umożliwia pobieranie listy wszystkich książek, filtrowanie według gatunku, pobieranie szczegółów dla określonej książki, zapisywanie danych do bazy danych SQLite oraz wyświetlanie danych z bazy.

## Użyte Technologie

- Python
- BeautifulSoup
- Requests
- SQLite

## Funkcje Aplikacji

1. **Pobieranie Listy Wszystkich Książek:**
   - Funkcja umożliwia pobranie listy wszystkich dostępnych książek na stronie.

2. **Filtrowanie Książek Według Gatunku:**
   - Możliwość filtrowania książek na podstawie określonego gatunku.

3. **Pobieranie Szczegółów Książki:**
   - Funkcja pozwala na uzyskanie szczegółowych informacji o określonej książce, takich jak cena i dostępność.

4. **Zapisywanie Danych do Bazy Danych:**
   - Automatyczne zapisywanie informacji o książkach do lokalnej bazy danych SQLite.

5. **Wyświetlanie Danych z Bazy Danych:**
   - Możliwość wyświetlania wszystkich zapisanych książek z bazy danych.


## Przykłady Użycia

```python
# Pobranie listy wszystkich książek
books_list = get_books_list('https://books.toscrape.com/')
print("List of all books:", books_list)

# Filtrowanie książek według gatunku
science_fiction_books = get_books_by_genre('https://books.toscrape.com/', 'Science Fiction')
print("Science Fiction books:", science_fiction_books)

# Pobranie szczegółów dla określonej książki
book_details = get_book_details('https://books.toscrape.com/', 'Sapiens: A Brief History of Humankind')
print("Details for the book:", book_details)

# Wyświetlenie wszystkich książek z bazy danych
display_all_books()
