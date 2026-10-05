# Rachunek prawdopodobieństwa

Skrypt rozwijany na podstawie odręcznych notatek i zdjęć tablic.
Aktualny PDF: **[Rachunek-prawdopodobienstwa.pdf](Rachunek-prawdopodobienstwa.pdf)**.

## Układ projektu

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
Dwukrotne kliknięcie `kompiluj.cmd` przebuduje rysunki, skrypt i otworzy PDF.
W PowerShell można wykonać:

```powershell
.\kompiluj.ps1
.\kompiluj.ps1 -Otworz
```

Plik w głównym katalogu jest nadpisywany po udanej kompilacji.
Jeśli kompilacja się nie uda, wcześniejszy PDF pozostaje dostępny.
W edytorze LaTeX należy budować `latex/main.tex` przez ten skrypt,
aby zaktualizować również PDF w głównym katalogu.

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
