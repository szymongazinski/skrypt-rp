# Rachunek prawdopodobieństwa

Skrypt rozwijany na podstawie odręcznych notatek i zdjęć tablic.
Najnowszy PDF jest dostępny w katalogu przedmiotu, obok folderu `projekt/`.
W repozytorium znajduje się też jego
**[wersjonowana kopia](Rachunek-prawdopodobienstwa.pdf)**.

## Układ projektu

Katalog `D:\Studia\Semestr 3\Rachunek prawdopodobieństwa` zawiera tylko:

```text
Rachunek prawdopodobieństwa/
├── Rachunek-prawdopodobienstwa.pdf
└── projekt/
```

Cały kod, materiały, grafika, repozytorium Git oraz pliki robocze
znajdują się w `projekt/`. Poniższe ścieżki są względem tego folderu:

- `latex/main.tex` - dokument główny i kolejność rozdziałów.
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
Dwukrotne kliknięcie `projekt/kompiluj.cmd` przebuduje rysunki, skrypt i otworzy PDF.
W PowerShell można wykonać:

```powershell
cd projekt
.\kompiluj.ps1
.\kompiluj.ps1 -Otworz
```

PDF obok folderu `projekt/` jest nadpisywany po udanej kompilacji,
podobnie jak jego wersjonowana kopia w repozytorium.
Jeśli kompilacja się nie uda, wcześniejszy PDF pozostaje dostępny.
W edytorze LaTeX należy budować `latex/main.tex` przez ten skrypt,
aby zaktualizować również PDF w katalogu przedmiotu.

## Formatowanie

Wzorcem typograficznym jest [„Miara i całka” Grzegorza Plebanka](http://www.math.uni.wroc.pl/~grzes/dydaktyka18_19/fr_main.pdf).
Wykorzystujemy PL Roman, 12 pt, format A4, klasyczne numerowane rozdziały
i podrozdziały, numerowane definicje, przykłady i wzory oraz spis treści
z klikalnymi czarnymi odnośnikami bez obramowania. Wzorzec jest używany
wyłącznie do formatowania, a nie jako źródło treści wykładu.

Nowe rysunki należy umieszczać w `grafika/`, wstawiać przez
`\includegraphics`, nadawać im `\label` i odwoływać się do nich przez `\ref`.

## Aktualizacje

Po każdej zmianie treści przebuduj dokument, sprawdź PDF i zapisz zmianę
w Git. Źródła, rysunki, materiały wejściowe i bieżący PDF są wersjonowane;
pliki tymczasowe nie trafiają do repozytorium.
