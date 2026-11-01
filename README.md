# Angielski z notatek

Responsywna aplikacja PWA na telefon. Działa na GitHub Pages, bez serwera i logowania.

## Publikacja na GitHub Pages

1. Utwórz publiczne repozytorium na GitHub, np. `angielski-fiszki`.
2. Prześlij pliki `index.html`, `manifest.webmanifest`, `icon.svg`, `sw.js` **do katalogu głównego repozytorium**.
3. Wejdź w **Settings → Pages**. Wybierz **Deploy from a branch**, gałąź `main` i folder `/(root)`, następnie zapisz.
4. Otwórz adres `https://TWOJ-LOGIN.github.io/angielski-fiszki/` (wstaw swoją nazwę użytkownika i repozytorium).
5. Na telefonie użyj w przeglądarce opcji „Dodaj do ekranu głównego”.

## Zawartość i przechowywanie danych

- **Fiszki:** dotknij, by zobaczyć odpowiedź; oceniaj jako „Umiem” lub „Powtórz”.
- **Test:** wpisywanie tłumaczenia PL → EN, automatyczne sprawdzanie dokładnej odpowiedzi (ignoruje wielkość liter i końcową interpunkcję).
- **Baza:** szukanie, filtrowanie, dodawanie i usuwanie słówek, zdań i skrótów.
- **Dane:** import i eksport JSON.

Przykładowa baza jest zapisana w `index.html` w stałej `SAMPLE`. Po pierwszym użyciu własne dane przechowywane są w `localStorage` *konkretnej przeglądarki na danym urządzeniu*. Nie synchronizują się między urządzeniami i mogą zniknąć po wyczyszczeniu danych przeglądarki. **Regularnie eksportuj kopię JSON.** Opublikowana strona jest publiczna, dlatego nie umieszczaj prywatnych notatek bezpośrednio w kodzie.

## Format importu

Plik JSON może mieć postać:

```json
{
  "items": [
    {"type": "word", "pl": "wyzwanie", "en": "challenge"},
    {"type": "sentence", "pl": "Jestem gotowy.", "en": "I am ready."},
    {"type": "abbr", "pl": "I'm", "en": "I am"}
  ]
}
```

Dozwolone typy: `word`, `sentence`, `abbr`. Import **zastępuje** bieżącą bazę i zeruje postępy, dlatego najpierw wykonaj eksport.

## Aktualizowanie z notatek

Po przesłaniu zdjęć notatek można przygotować z nich plik JSON w powyższym formacie, który następnie zaimportujesz do aplikacji, albo zmienić dane startowe w kodzie.


## Materiał z przesłanych zdjęć (wersja 2.0)

Aplikacja zawiera 241 haseł w trzech kategoriach: słowa, zdania, skróty. Pełny import danych: `materialy-z-notatek.json`. Tłumaczenia są poprawione językowo i bywają parafrazą widocznych ćwiczeń. Niewyraźnych zapisów nie rekonstruowano dosłownie.

**Uwaga przy aktualizacji:** baza lokalna ma odrębny klucz `angielski-notatki-v2`. Jeśli masz własne fiszki w starej aplikacji, najpierw wykonaj ich eksport, a później import do nowej wersji (import zastępuje obecną bazę).


## Materiał z przesłanych zdjęć (wersja 2.0)

Aplikacja zawiera 239 haseł w trzech kategoriach: słowa, zdania, skróty. Pełny import danych: `materialy-z-notatek.json`. Tłumaczenia są poprawione językowo i bywają parafrazą widocznych ćwiczeń. Niewyraźnych zapisów nie rekonstruowano dosłownie.

**Uwaga przy aktualizacji:** baza lokalna ma odrębny klucz `angielski-notatki-v2`. Jeśli masz własne fiszki w starej aplikacji, najpierw wykonaj ich eksport, a później import do nowej wersji (import zastępuje obecną bazę).


## Materiały z notatek (wersja 2)

Wbudowana baza zawiera 254 pozycji: 136 słówek, 67 zdań i 51 skrótów. Materiał pochodzi z przesłanych zdjęć; niejasne fragmenty rękopisu pominięto. Tłumaczenia zostały językowo poprawione.

Plik `materialy-z-notatek.json` stanowi również samodzielny import do poprzedniej wersji. Nowa wersja po wgraniu do GitHub Pages sama dokłada nowe fiszki do lokalnej bazy.
