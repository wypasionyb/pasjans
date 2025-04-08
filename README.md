# Pasjans - Gra Karciana

## Opis projektu

Pasjans to klasyczna gra karciana w wersji jednopodmiotowej, której celem jest uporządkowanie kart w czterech stosach końcowych, od Asa do Króla, dla każdego koloru (kier, karo, pik, trefl).

Projekt wykonany jest w języku C# jako aplikacja konsolowa. Gra pozwala na przenoszenie kart pomiędzy kolumnami, dobieranie kart z rezerwowego stosu, a także sprawdzenie, czy gra została wygrana.

## Zasady gry

1. **Układ początkowy:**

   - Talia kart: 52 karty (bez jokerów).
   - Karty mają 4 kolory: kier (♥), karo (♦), pik (♠), trefl (♣).
   - Układ początkowy to 7 kolumn, w których karty są stopniowo odkrywane.
   - Reszta kart trafia na stos rezerwowy.

2. **Rozgrywka:**

   - Karty można przenosić tylko w kolejności malejącej (Król → Królową → Walet → 10 → 9 → 8 → 7 → 6 → 5 → 4 → 3 → 2 → As) oraz naprzemiennie kolorami.
   - Możesz przenosić karty pomiędzy kolumnami oraz na stosy końcowe.
   - Kiedy przeniesiesz kartę, odkrywana jest karta poniżej.

3. **Zakończenie gry:**
   - Gra kończy się wygraną, gdy wszystkie karty zostaną poprawnie przeniesione na stosy końcowe.
   - Jeśli zdecydujesz się zakończyć grę, wybierz opcję "Zakończ grę".

## Instrukcja uruchomienia

### Wymagania:

- .NET 8.0 lub nowszy (jeśli jeszcze go nie masz, możesz pobrać go ze strony [dotnet.microsoft.com](https://dotnet.microsoft.com/download)).

### Krok 1: Pobierz lub sklonuj projekt

Sklonuj repozytorium lub pobierz pliki projektu na swoje urządzenie.

### Krok 2: Uruchom projekt

1. Przejdź do katalogu głównego.
2. Uruchom plik .exe

Gra powinna uruchomić się w terminalu i będzie dostępna do interakcji.

## Sterowanie

1. **Główne menu:**

- Wybierz **1**, aby rozpocząć nową grę.
- Wybierz **2**, aby zakończyć grę.

2. **W trakcie gry:**

- **1** – Przenieś kartę między kolumnami.
- **2** – Dobierz kartę z rezerwowego stosu.
- **3** – Zakończ grę.

3. **Ruchy:**

- Aby przenieść kartę, wybierz numer kolumny, z której chcesz przenieść kartę, oraz numer kolumny, do której chcesz ją przenieść.

4. **Zakończenie gry:**

- Gra zakończy się, gdy wszystkie karty zostaną uporządkowane w stosach końcowych.

## Przykład interakcji

Po uruchomieniu gry w terminalu, użytkownik zobaczy menu główne oraz będzie mógł podejmować decyzje o wyborze akcji. Gra wyświetli stan planszy oraz dostarczy opcje do dalszej interakcji.

[Kolumna 1] K♠ [Kolumna 2] Q♣, 2♥ ... [REZERWA] 3♦ 5♠ A♥

Wybierz akcję:

1. Przenieś kartę między kolumnami

2. Dobierz kartę ze stosu rezerwowego

3. Zakończ grę

## Struktura projektu

### Klasy

- **Card** – Reprezentuje pojedynczą kartę w grze.
- **Deck** – Reprezentuje talię kart.
- **Reserve** – Reprezentuje stos rezerwowy, z którego gracz może dobierać karty.
- **Column** – Reprezentuje kolumnę, w której układane są karty.
- **Game** – Zarządza całą logiką gry.
- **UI** – Zarządza interakcją z użytkownikiem (wyświetlanie menus, komunikatów itd.).
