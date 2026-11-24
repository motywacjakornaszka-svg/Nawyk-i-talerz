# Nawyki i Talerz 4.0

Elastyczne nawyki (Mini / Plus / Elita, pamiętnik, cele, projekty, mentor AI) i Talerz (licznik kalorii ze zdjęć, płyny, kroki, waga) w jednej aplikacji.

## Co daje połączenie
- **Zakładka 🍽️ Jedzenie**: cały Talerz z podzakładkami Dziś, Historia i Profil.
- **Nawyki ⚡ zaliczają się same** z danych Jedzenia. Na start:
  - „Wypicie 2 litrów wody”: płyny 1000 / 1500 / 2000 ml;
  - „Owoc i warzywo”: 100 / 250 / 400 g;
  - „Spacer (kroki)”: 4000 / 7000 / 10 000 kroków.
  W „✏️ Edytuj nawyki” możesz zmienić progi albo podpiąć inny nawyk do: wody, warzyw, kroków, cukrów wolnych lub „jedzenie zapisane i w limicie”. Nawyk zawsze możesz też zaznaczyć ręcznie, a liczy się wyższy z dwóch poziomów.
- **Karta Jedzenia na ekranie Dziś**: kalorie / limit, płyny, warzywa i kroki, z szybkimi przyciskami 📷 Posiłek, 💧 Woda i 👟 Kroki. Posiłek i wodę dodasz też przyciskiem ＋.
- **Mentor AI widzi jedzenie, płyny, kroki i wagę.** Możesz to wyłączyć w Ustawieniach → Prywatność.
- **Postęp**: karta „Jedzenie – ostatnie 7 dni” (dni w limicie, cel płynów, warzywa, kroki, zmiana wagi).
- **Wspólne klucze AI** (Gemini i Claude): klucz dodany w jednym miejscu działa w obu częściach.
- **Kopia zapasowa** (Więcej → Kopie i dane) zawiera także dane Jedzenia.

## Uruchomienie na GitHub Pages
1. Na koncie **motywacjakornaszka-svg** utwórz nowe repozytorium, np. `nawyki-talerz`, z widocznością **Public**.
2. Wgraj **wszystkie pliki z tego folderu** do głównego folderu repozytorium, bez podfolderu.
3. Wejdź w Settings → Pages → Source: „Deploy from a branch”, wybierz gałąź `main`, folder `/ (root)` i kliknij Save.
4. Po 1–2 minutach aplikacja będzie pod adresem `https://motywacjakornaszka-svg.github.io/nawyki-talerz/`. Otwórz go w Chrome na telefonie i zainstaluj (⋮ → Zainstaluj aplikację).

## Twoje dane przejdą same
Przeglądarka przechowuje dane osobno dla każdego adresu bazowego. Adres bazowy to tu `motywacjakornaszka-svg.github.io`, a nie folder repozytorium. Stare aplikacje i nowa mają ten sam adres bazowy, więc nowa aplikacja **od razu widzi** Twoje nawyki, pamiętnik, zdjęcia, posiłki, wagę i klucze AI. Nie trzeba niczego przenosić.

Warunek: używasz **tej samej przeglądarki na tym samym telefonie**. Dla bezpieczeństwa przed pierwszym uruchomieniem zrób kopie w starych aplikacjach (Nawyki: Raport → 💾 Kopia JSON, Talerz: Profil → Eksportuj dane).

Po przejściu korzystaj już tylko z nowej aplikacji. Stare możesz zostawić na jakiś czas jako zapas, bo pracują na tych samych danych.

## Aktualizacje
Po zmianie plików podbij `VERSION` w `sw.js` (np. `nawyki-talerz-v4.0-2`). Zamknij aplikację i otwórz ją ponownie.

## Pliki
- `index.html`, `app.js`, `data.js`, `style.css`: Nawyki (aplikacja główna);
- `talerz.html`: Jedzenie (Talerz), wyświetlane w zakładce;
- `sw.js`: działanie offline;
- `manifest.webmanifest`: instalacja i skróty z ikony (Dodaj posiłek / Dodaj wodę);
- ikony.

Klucze API zostają tylko na telefonie i nie trafiają do repozytorium ani do kopii. **Nigdy nie wpisuj klucza do plików.**
