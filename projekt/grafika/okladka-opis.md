# Okładka

Aktywne pliki:

- `okladka.tex` - edytowalny skład A4, pozycja fotografii i tekst dostępności.
- `okladka.pdf` - wspólna kompletna okładka obu wersji skryptu.
- `okladka-realistyczna.png` - baza plakatu z realistycznymi fikcyjnymi krupierami,
  wygenerowana wbudowanym imagegen; obejmuje kasyno, rekwizyty i całą typografię.
- `okladka-realistyczna-prompt.txt` - pełny prompt bazy.
- `lebron-glowa.png` - istniejące wycięcie fotograficzne RGBA ze zdjęcia użytkownika,
  wykorzystane ponownie bez generowania twarzy. Przezroczystość usuwa prostokątne tło.

Nowsze polecenie użytkownika zastępuje kreskówkowy styl realistycznymi postaciami.
Obaj krupierzy są dorośli i fikcyjni, bez podobieństwa do prowadzącego, z normalnymi
proporcjami twarzy, skoordynowanym spojrzeniem oraz pojedynczym złotym górnym kłem.
Cztery przednie siekacze są białe. Zachowano białe koszule, czarne kamizelki i muchy,
wyprostowane ręce głównej postaci oraz oparcie dłoni na ruletce.

„Rachunek” jest ozdobnie wygięty nad ruletką, a „prawdopodobieństwa” pod nią.
Napisy są wkomponowane w kasynowy plakat. Pod postacią trzymającą cyfry 6 i 7 jest
podpis „co ty tam odpierdalasz z tymi rękami?”. W urnie są trzy czarne i cztery białe kule.
Fotograficzna głowa LeBrona znajduje się nad dolnym prawym cytatem, bez ramki i tła zdjęcia.

Imagegen odrzucił generowanie realistycznego LeBrona. Z tego powodu gotowe wycięcie
zdjęcia umieszczono jako osobny element LaTeX. Baza obrazu pozostawia dla niego wolne miejsce.
Wszystkie zależności kompletnej okładki znajdują się w `grafika/`.

Dawne okładki z fotografią prowadzącego i nieaktywne ilustracje pozostają lokalnie
w prywatnym archiwum metadanych Git. Nie są potrzebne do kompilacji.
