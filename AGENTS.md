# Zasady rozwijania skryptu

Cały projekt, repozytorium Git i pliki robocze znajdują się w podfolderze
`projekt/`; dokument główny względem tego katalogu: `latex/main.tex`.
W katalogu nadrzędnym przedmiotu pozostają wyłącznie folder `projekt/`
i najnowszy `Rachunek-prawdopodobienstwa.pdf`.

- Przepisuj dostarczone notatki i zdjęcia po polsku do odpowiednich rozdziałów.
- Zachowuj PL Roman 12 pt, klasyczny skład oraz czarne, klikalne odnośniki.
- Oryginalne materiały kopiuj do `materialy/RRRR-MM-DD/`; nie usuwaj ich z Pobranych.
- Wszystkie rysunki i ich edytowalne źródła umieszczaj osobno w `grafika/`.
  Stosuj `\label`, `\ref` i względne ścieżki.
- Nie zgaduj nieczytelnych treści; zapisuj istotne niejasności w opisie materiałów
  i wyjaśniaj je z użytkownikiem. Nie dopisuj nowych tematów bez materiałów.
- Po każdej zmianie uruchom `kompiluj.ps1`, sprawdź odnośniki i wygląd PDF-a.
  Najnowszy PDF ma być dostępny jako `Rachunek-prawdopodobienstwa.pdf`
  w katalogu nadrzędnym, obok folderu `projekt/`. Skrypt kompilacji zapisuje
  również kopię wewnątrz repozytorium do wersjonowania.
- Wersjonuj źródła, materiały, grafikę i aktualny PDF. Repozytorium ma być prywatne.

## EasyShut

Podczas pracy używaj `C:\Users\szymo\AppData\Local\Programs\easyshut\EasyShut.exe -n`
i sprawdzaj `-status`. Przed uruchomieniem upewnij się, że pomoc/status
potwierdza respektowanie wygaszania Windows bez `-screen_on`.
Nie dodawaj `-screen_on`, nie ustawiaj czasowego wyłączenia, nie zamykaj
głównego okna EasyShut. Po pracy pozostaw tryb „Nigdy” i komputer włączony.
