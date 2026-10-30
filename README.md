# Calion: test labiryntu 7×10

Oddzielna publikacja eksperymentalnej mapy Calionu. Publiczna wersja [Karcianki](https://the-rozu.github.io/Karcianka/) pozostaje niezależna.

## Dwa osobne podglądy

- Eksperyment 7×10: https://the-rozu.github.io/Karcianka-labirynt/ (źródło: gałąź experiment/labirynt-5x8).
- Zintegrowana główna wersja rozwojowa: https://the-rozu.github.io/Karcianka-labirynt/dev/ (źródło: gałąź dev-mode).

Workflow publikuje je jednocześnie w osobnych folderach, nie zmieniając oryginalnego publicznego adresu gry https://the-rozu.github.io/Karcianka/. Po aktualizacji dev-mode należy ponownie uruchomić workflow lub wywołać nowy push na tej gałęzi repozytorium testowego.

## Uruchamianie

Docelowy adres: https://the-rozu.github.io/Karcianka-labirynt/

Źródło gry: [The-RozU/Karcianka, gałąź experiment/labirynt-5x8](https://github.com/The-RozU/Karcianka/tree/experiment/labirynt-5x8).

Workflow na gałęzi `dev-mode` pobiera komplet plików źródłowych (wraz z grafikami) i publikuje je przez GitHub Pages. Nie zmienia oryginalnego repozytorium.

## Układ mobilny

W trybie poziomym mapa zajmuje lewą część ekranu, a statystyki i opis bossa są po prawej. Plansza mieści wszystkie 7 kolumn bez przewijania w poziomie; przewijamy wyłącznie pionowo. Na większych ekranach okno mapy zajmuje więcej przestrzeni.

## Rozklad pol 7×10

70 pol lacznie: 1 start, 1 boss, maksymalnie 10 zwyklych przeciwnikow, 4 elity, 2 sklepy, 3 skrzynie, 2 leczenia, 3 wydarzenia i 44 puste korytarze. Kazde leczenie znajduje sie w slepym zaulku z jednym wejsciem przez zwyklego przeciwnika. Wydarzenia nie dodaja nowych walk ponad limit.

## Sterowanie mapą (wersja testowa 8)

- Cała szerokość 7 pól jest widoczna jednocześnie, a mapa przewija się wyłącznie pionowo.
- Szare, niezbadane przejścia pozostają widoczne po odejściu gracza, bez ikon i ścian.
- Ściany danego pola ujawniają się dopiero po wejściu na to pole.
- Ściany nieodkrytych pomieszczeń są ukryte. Odsłaniają się przy postaci i pozostają widoczne w odwiedzonych polach.
- Odkryte ściany są grubsze i bardziej kontrastowe.
- Po ukończeniu walki, skrzyni, leczenia, sklepu lub wydarzenia oryginalna ikona pozostaje na zielonym polu.
- Powrót na odwiedzone pole służy do poruszania się i nie uruchamia ponownie nagród ani sklepów.
- Start ma przynajmniej dwie drogi wyjścia, a dodatkowe połączenia tworzą alternatywne trasy.
- Kliknij sąsiedni, nieodkryty pokój, żeby przejść do niego z animacją.
- Kliknij dowolny wcześniej odwiedzony pokój, aby postać wróciła po najkrótszej trasie prowadzącej wyłącznie przez odwiedzone pola.
- Pomieszczenia mijane po drodze nie wywołują ponownie wydarzeń ani walk.
- W podsumowaniu walki przycisk powrotu na mapę jest główny, a wyjście do lobby jest mniejsze i czerwone.

## Pierwsze uruchomienie GitHub Pages

1. W tym repozytorium otwórz **Settings → Pages**.
2. W sekcji **Build and deployment → Source** wybierz **GitHub Actions**.
3. Otwórz **Actions → Publikacja labiryntu Calion → Run workflow**, wybierz gałąź `dev-mode` i uruchom.
4. Po zakończeniu wdrożenia otwórz adres powyżej.

Po zmianach w źródłowej gałęzi eksperymentalnej uruchom workflow ponownie. Zmiany w gałęzi `dev-mode` tego repozytorium uruchamiają go automatycznie. Przy kolejnej publikacji uruchom **nowy workflow** (Run workflow), zamiast używać Re-run jobs, ponieważ ponowne użycie starego uruchomienia może zdublować artefakt `github-pages`.
