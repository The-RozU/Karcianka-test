# Kalon: testowa wersja gry

Wersja testowa Kalona jest zawsze budowana z gałęzi [Karcianka/dev-mode](https://github.com/The-RozU/Karcianka/tree/dev-mode). Stabilna wersja [Karcianka/main](https://github.com/The-RozU/Karcianka/tree/main) pozostaje niezależna i nie jest modyfikowana przez publikację testową.

## Linki do gry

- **Główny link do testowania na telefonie:** https://the-rozu.github.io/Karcianka-test/
- **Alternatywny adres tej samej gry:** https://the-rozu.github.io/Karcianka-test/dev/
- **Archiwum eksperymentu z labiryntem:** https://the-rozu.github.io/Karcianka-test/experiment/
- **Wersja stabilna:** https://the-rozu.github.io/Karcianka/

Adres główny i /dev/ są tworzone z dokładnie tego samego commita źródłowego `Karcianka/dev-mode`. Identyfikator źródłowego commita jest zapisany w `/dev-source-sha.txt`.

## Publikacja

Workflow [Publikacja Kalon - wersja testowa](.github/workflows/deploy.yml) uruchamia się po push na gałąź `dev-mode` w **tym repozytorium** lub ręcznie przez GitHub Actions. Pobiera bieżące źródło `The-RozU/Karcianka@dev-mode`, sprawdza spójność numeru wersji, a następnie publikuje dwa identyczne podglądy i zachowuje archiwum eksperymentu w /experiment/.

Aby zmiany `Karcianka/dev-mode` same uruchamiały powyższy workflow, w **repozytorium Karcianka** należy jednorazowo ustawić sekret Actions **`KALON_TEST_SYNC_TOKEN`**. Wartością powinien być fine-grained personal access token z uprawnieniem **Contents: Read and write** wyłącznie dla repozytorium `The-RozU/Karcianka-test`. Nie należy wpisywać tokenu do żadnego pliku ani wysyłać go na czacie.

Po ustawieniu sekretu workflow `Karcianka/.github/workflows/sync-test-preview.yml` przy każdym pushu na źródłowe `dev-mode` tworzy pusty commit powiadamiający w `Karcianka-test/dev-mode`. Ten commit uruchamia aktualizację GitHub Pages. Do pełnej synchronizacji nie jest potrzebna ręczna zmiana plików, pobieranie ZIP ani modyfikowanie `main`.

Jeśli token nie jest ustawiony, publikacja po zmianach w źródłowym repozytorium **nie jest automatyczna**. Można uruchomić `Publikacja Kalon - wersja testowa` ręcznie z gałęzi `dev-mode` po udostępnieniu workflow w interfejsie Actions.

## Test gry

- Rozgrywka PvE odbywa się w labiryncie 7 × 10.
- Mechanika walki, wydarzenia, skrzynie, sklepy, boss i pozostałe zasoby są pobierane razem z aktualnym kodem gry.
- Wyświetlany numer wersji jest pobierany z `index.html` gałęzi źródłowej i nie jest na sztywno wpisywany w workflow publikacji.
