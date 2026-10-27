# Rachunek prawdopodobieństwa

Skrypt rozwijany na podstawie odręcznych notatek i zdjęć tablic.
Najnowsze PDF-y: **[bez oznaczeń wykładów](../Rachunek-prawdopodobienstwa.pdf)**
i **[z oznaczeniami wykładów](../Rachunek-prawdopodobienstwa-wyklady.pdf)** są dostępne
w katalogu przedmiotu, obok folderu `projekt/`. Ten sam układ obowiązuje
lokalnie i w głównym katalogu repozytorium na GitHubie.

Repozytorium: [skrypt-rp](https://github.com/szymongazinski/skrypt-rp).
Bieżące pliki zawierają aktualną realistyczną okładkę. Dawne okładki
z fotografią prowadzącego nie są częścią tego repozytorium ani jego historii.

## Układ projektu

Katalog `D:\Studia\Semestr 3\Rachunek prawdopodobieństwa` zawiera tylko:

```text
Rachunek prawdopodobieństwa/
├── Rachunek-prawdopodobienstwa.pdf
├── Rachunek-prawdopodobienstwa-wyklady.pdf
└── projekt/
```

Cały kod, materiały, grafika, repozytorium Git oraz pliki robocze
znajdują się w `projekt/`. Poniższe ścieżki są względem tego folderu:

- `latex/main.tex` - dokument główny i kolejność rozdziałów.
- `latex/main-wyklady.tex` - wariant z oznaczeniami początków wykładów.
- `latex/strony/tytulowe.tex` - okładka i druga strona z informacją o skrypcie.
- `latex/preambula.tex` - pakiety, czcionka, formatowanie i polecenia matematyczne.
- `latex/rozdzialy/` - tekst kolejnych rozdziałów.
- `grafika/` - osobne źródła rysunków i ich gotowe pliki PDF.
- `materialy/README.md` - pochodzenie materiałów i uwagi do transkrypcji.
- `materialy/RRRR-MM-DD/` - zachowane oryginalne notatki i zdjęcia.
- `build/` - pliki robocze kompilacji; pomijane przez Git.
- `kompiluj.ps1` i `kompiluj.cmd` - budowanie aktualnego PDF-a.

## Kompilacja

Wymagany jest `pdflatex` z MiKTeX lub TeX Live dostępny w PATH.
Na tym komputerze MiKTeX i potrzebne pakiety są już zainstalowane.
Dwukrotne kliknięcie `projekt/kompiluj.cmd` przebuduje rysunki i obie wersje
skryptu oraz otworzy oba PDF-y.
W PowerShell można wykonać:

```powershell
cd projekt
.\kompiluj.ps1
.\kompiluj.ps1 -Otworz
```

Oba PDF-y obok folderu `projekt/` są aktualizowane po udanej kompilacji
obu wersji i wersjonowane w głównym katalogu repozytorium.
Jeśli kompilacja się nie uda, wcześniejsze PDF-y pozostają dostępne.
Buduj przez `kompiluj.ps1`, aby zaktualizować oba pliki.

## Podział na wykłady

Oba warianty mają tę samą treść, kolejność i numerację matematyczną.
Wariant `-wyklady.pdf` pokazuje dodatkowo nagłówki „Wykład 1”, „Wykład 2”
itd. oraz odpowiadające im wpisy w klikalnym spisie treści. Wariant zwykły
pomija znaczniki. Czerwona falowana kreska może oznaczać początek wykładu
lub przerwę w notatkach, np. pominięty przykład, definicję albo twierdzenie.
Granice ustalaj według wyjaśnień użytkownika; wstawiaj w nich
`\poczatekwykladu{numer}`.
Znaczniki nie resetują liczników. Nie dodawaj dat materiałów do PDF-a.
Wyraźnie wskazana przez użytkownika granica ma pierwszeństwo:
wykład 2 zaczyna się przed dowodem własności 6 (ciąg rosnący),
a stwierdzenia wszystkich siedmiu własności należą do wykładu 1.
Wykład 3 zaczyna się od początku materiału o niezależności, przed definicją
niezależności dwóch zdarzeń.
Wykład 4 zaczyna się od przykładu z nieskończenie wieloma wystąpieniami ORRO,
po lemacie Borela--Cantellego; dalej obejmuje zmienne losowe i układy pi oraz lambda.

## Formatowanie

Wzorcem typograficznym jest [„Miara i całka” Grzegorza Plebanka](http://www.math.uni.wroc.pl/~grzes/dydaktyka18_19/fr_main.pdf).
Wykorzystujemy PL Roman, 12 pt, format A4, klasyczne numerowane rozdziały
i podrozdziały, numerowane definicje, przykłady i wzory oraz spis treści
z klikalnymi czarnymi odnośnikami bez obramowania. Wzorzec jest używany
wyłącznie do formatowania, a nie jako źródło treści wykładu.

Każdy PDF zaczyna się wspólną graficzną okładką i stroną z informacją
o prowadzącym, autorze oraz właściwym wariancie chronologii. Dopiero trzecia
strona zawiera spis treści. Okładka i strona informacyjna nie mają numerów;
spis treści ma numerację rzymską, a treść arabską. W treści nie ma nagłówków
z nazwami rozdziałów; numery stron są wyśrodkowane na dole.

Każdy rodzaj elementu (definicja, przykład, twierdzenie, fakt, lemat,
wniosek, uwaga) ma osobny licznik ciągły przez cały rozdział i resetowany
wyłącznie na początku `\chapter`. Sekcje i podsekcje nie resetują liczników.
Numery mają postać `rozdział.numer`, np. Definicja 1.1, Definicja 1.2
oraz osobno Przykład 1.1, Przykład 1.2. Skrypt nie zawiera dat otrzymania materiałów.

Nowe rysunki należy umieszczać w `grafika/`, wstawiać przez
`\includegraphics`, nadawać im `\label` i odwoływać się do nich przez `\ref`.

## Aktualizacje

Po każdej zmianie treści przebuduj dokument, sprawdź PDF i zapisz zmianę
w Git. Źródła, rysunki, materiały wejściowe i bieżący PDF są wersjonowane;
pliki tymczasowe nie trafiają do repozytorium.

Lokalne metadane Git są w `projekt/.git`, a katalog roboczy repozytorium
obejmuje katalog przedmiotu (`core.worktree=../..`). Polecenia Git wykonuj
z folderu `projekt/`, np. `git -C projekt status` z katalogu przedmiotu.
Przy zwykłym klonowaniu z GitHub układ plików jest taki sam; Git utworzy
standardowy ukryty katalog `.git` w katalogu klonu.
