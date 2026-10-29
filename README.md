# Calion: test labiryntu 5×8

Oddzielna publikacja eksperymentalnej mapy Calionu. Publiczna wersja [Karcianki](https://the-rozu.github.io/Karcianka/) pozostaje niezależna.

## Uruchamianie

Docelowy adres: https://the-rozu.github.io/Karcianka-labirynt/

Źródło gry: [The-RozU/Karcianka, gałąź experiment/labirynt-5x8](https://github.com/The-RozU/Karcianka/tree/experiment/labirynt-5x8).

Workflow na gałęzi `dev-mode` pobiera komplet plików źródłowych (wraz z grafikami) i publikuje je przez GitHub Pages. Nie zmienia oryginalnego repozytorium.

## Układ mobilny

W trybie poziomym mapa zajmuje lewą część ekranu, a statystyki i opis bossa są w panelu po prawej. Rozmiary kafelków dopasowują się do wysokości telefonu. Można przewijać labirynt pionowo.

## Pierwsze uruchomienie GitHub Pages

1. W tym repozytorium otwórz **Settings → Pages**.
2. W sekcji **Build and deployment → Source** wybierz **GitHub Actions**.
3. Otwórz **Actions → Publikacja labiryntu Calion → Run workflow**, wybierz gałąź `dev-mode` i uruchom.
4. Po zakończeniu wdrożenia otwórz adres powyżej.

Po zmianach w źródłowej gałęzi eksperymentalnej uruchom workflow ponownie. Zmiany w gałęzi `dev-mode` tego repozytorium uruchamiają go automatycznie.
