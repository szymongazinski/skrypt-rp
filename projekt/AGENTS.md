# Zasady rozwijania skryptu

Cały projekt, repozytorium Git i pliki robocze znajdują się w podfolderze
`projekt/`; dokument główny względem tego katalogu: `latex/main.tex`.
W katalogu nadrzędnym przedmiotu pozostają wyłącznie folder `projekt/`
i dwa PDF-y: `Rachunek-prawdopodobienstwa.pdf` (bez oznaczeń wykładów)
oraz `Rachunek-prawdopodobienstwa-wyklady.pdf` (z oznaczeniami początków wykładów).
Ten sam układ obowiązuje w głównym katalogu repozytorium na GitHubie.
Repozytorium obejmuje katalog przedmiotu, a lokalne metadane Git pozostają
w `projekt/.git` z ustawieniem `core.worktree=../..`.
Polecenia Git wykonuj z folderu `projekt/` (lub przez `git -C projekt ...`).
Nie przenoś ponownie katalogu głównego repozytorium do folderu `projekt/`.

- Przepisuj dostarczone notatki i zdjęcia po polsku do odpowiednich rozdziałów.
- Dla `1_A` stosuj nazwy „indykator zbioru A” lub „funkcja charakterystyczna zbioru A”.
- Zachowuj PL Roman 12 pt, klasyczny skład oraz czarne, klikalne odnośniki.
- Nie używaj żywej paginy z nazwami rozdziałów. Stosuj `\pagestyle{plain}`:
  numery stron wyśrodkowane na dole, nagłówki puste.
- Pierwsza strona to wspólna graficzna okładka `grafika/okladka.pdf`,
  składana z pliku `grafika/okladka.tex` i kompletnego obrazu
  `grafika/okladka-realistyczna.png` oraz osobnej fotografii z przezroczystością
  `grafika/lebron-glowa.png`. Pełny prompt bazy zapisuj
  w `grafika/okladka-realistyczna-prompt.txt`.
  Na drugiej stronie podaj prowadzącego prof. Jacka Małeckiego oraz autora
  Szymona Gazińskiego i dopasuj informację o chronologii do wariantu PDF.
  Dopiero po obu tych stronach umieszczaj spis treści.
  Okładka ma typografię wpisaną w kasynowy plakat: wygięty „Rachunek” nad ruletką
  i „prawdopodobieństwa” pod nią. Nie dodawaj prostokątnych pól na napisy ani
  prostokątnych fotograficznych nakładek. Nowsze polecenie użytkownika zmienia
  styl postaci na realistyczny: obaj krupierzy są dorosłymi fikcyjnymi osobami
  o naturalnych proporcjach twarzy, bez podobieństwa do prowadzącego wykład.
  Są bez zarostu i okularów, z krótkimi włosami ułożonymi na bok,
  umiarkowanym uśmiechem i prawidłowo ustawionymi oczami patrzącymi na widza.
  Jedyny złoty ząb to górny kieł (trójka), a cztery przednie siekacze są białe.
  LeBron jest fotograficzny: używaj istniejącego wycięcia RGBA z oryginalnego
  zdjęcia użytkownika, umieszczonego w LaTeX bez prostokątnego tła.
  Pod mniejszym krupierem z cyframi 6 i 7 ma być podpis
  „co ty tam odpierdalasz z tymi rękami?”.
  Zachowuj trzy czarne i cztery białe kule oraz czytelne cyfry 6 i 7.
  Nie przywracaj dawnych okładek ani fotografii prowadzącego. Aktualna
  fotografia LeBrona została osobno wskazana przez użytkownika do okładki.
  Nieaktywne ilustracje zachowuj lokalnie w prywatnym archiwum metadanych Git.
  Niewybrane podglądy pozostawiaj lokalnie
  w ignorowanym katalogu `grafika/podglady-kreskowka/`.
- Nie umieszczaj w skrypcie informacji o dacie otrzymania materiałów.
- Utrzymuj oba PDF-y z jednej wspólnej treści. Wersję z chronologią buduje
  `latex/main-wyklady.tex`, zwykłą wersję buduje `latex/main.tex`.
- Granice wykładów ustalaj według poleceń użytkownika. Czerwona falowana
  kreska może oznaczać początek wykładu albo przerwę w notatkach, np. miejsce
  pominiętego przykładu, definicji lub twierdzenia. Nie traktuj jej automatycznie
  jako granicy wykładów. W ustalonym miejscu wstawiaj `\poczatekwykladu{numer}`;
  znacznik jest widoczny tylko
  w wersji z chronologią, także w spisie treści. Nie resetuje liczników.
  Nie wyznaczaj nowych granic wyłącznie na podstawie dat plików.
  Wyraźnie wskazana przez użytkownika granica ma pierwszeństwo przed
  oznaczeniami w materiałach. Wykład 2 zaczyna się przed dowodem własności 6
  (ciąg rosnący); wszystkie siedem stwierdzeń należą jeszcze do wykładu 1.
  Wykład 3 zaczyna się od początku notatek o niezależności, przed definicją
  niezależności dwóch zdarzeń. Kreska na zrzucie z tego wykładu oznacza przerwę.
  Wykład 4 zaczyna się przed przykładem ORRO, po dowodach lematu
  Borela--Cantellego. Następnie obejmuje zmienne losowe i układy pi oraz lambda.
  Wykład 5 zaczyna się przed twierdzeniem o funkcjach niezależnych bloków
  zmiennych losowych; dalej obejmuje rozkłady zmiennych losowych i rozkłady dyskretne.
- Definicje, przykłady, twierdzenia, fakty, lematy, wnioski i uwagi mają osobne
  liczniki ciągłe przez cały rozdział, resetowane wyłącznie przy `\chapter`.
  Sekcje i podsekcje nie resetują liczników. Numer ma postać `rozdział.numer`,
  np. Definicja 1.1, Definicja 1.2 oraz osobno Przykład 1.1, Przykład 1.2.
- Oryginalne materiały kopiuj do `materialy/RRRR-MM-DD/`; nie usuwaj ich z Pobranych.
- Wszystkie rysunki i ich edytowalne źródła umieszczaj osobno w `grafika/`.
  Stosuj `\label`, `\ref` i względne ścieżki.
- Nie zgaduj nieczytelnych treści; zapisuj istotne niejasności w opisie materiałów
  i wyjaśniaj je z użytkownikiem. Nie dopisuj nowych tematów bez materiałów.
- Po każdej zmianie uruchom `kompiluj.ps1`, sprawdź odnośniki i wygląd PDF-a.
  Oba najnowsze PDF-y mają być dostępne obok folderu `projekt/` i wersjonowane
  w głównym katalogu repozytorium. Nie twórz dodatkowych kopii w projekcie.
- Wersjonuj źródła wykładów, materiały dydaktyczne, bieżącą grafikę i aktualne
  PDF-y. Użytkownik polecił udostępnić repozytorium publicznie pod warunkiem,
  że poprzednie okładki i ich fotografie nie będą dostępne w plikach ani historii.
  Nie zmieniaj widoczności na publiczną, dopóki ten warunek nie jest sprawdzony.
  Repozytorium na GitHubie:
  `https://github.com/szymongazinski/skrypt-rp`.
- Stosuj wyłącznie oficjalne, krótkie komunikaty commitów w formie bezosobowej:
  `dodano wykład N` przy dodaniu wykładu, a `Poprawki stylistyczne` przy
  pozostałych zmianach. Nie dodawaj rozwinięcia ani szczegółowych opisów.

## EasyShut

Podczas pracy używaj `C:\Users\szymo\AppData\Local\Programs\easyshut\EasyShut.exe -n`
i sprawdzaj `-status`. Przed uruchomieniem upewnij się, że pomoc/status
potwierdza respektowanie wygaszania Windows bez `-screen_on`.
Nie dodawaj `-screen_on`, nie ustawiaj czasowego wyłączenia, nie zamykaj
głównego okna EasyShut. Po pracy pozostaw tryb „Nigdy” i komputer włączony.
