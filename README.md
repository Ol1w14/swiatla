# 🚦 Inteligentna sygnalizacja świetlna z czujnikami PIR

## 📌 Opis projektu

Projekt przedstawia system sygnalizacji świetlnej oparty na Arduino Uno oraz czterech czujnikach ruchu PIR. Każdy czujnik jest przypisany do osobnej sygnalizacji składającej się z czerwonej i zielonej diody LED.

Głównym celem projektu jest wykrywanie ruchu i automatyczne przełączanie świateł odpowiedniego kierunku na zielone, podczas gdy pozostałe kierunki mają światło czerwone.

## 🛠️ Wykorzystane komponenty

- Arduino Uno
- 4 czujniki ruchu PIR
- 4 czerwone diody LED
- 4 zielone diody LED
- Rezystory ograniczające prąd diod LED
- Przewody połączeniowe
- Tinkercad Circuits

## 🔌 Podłączenie elementów

### Diody LED

| Kierunek | Czerwona LED | Zielona LED |
|---|---|---|
| 1 | Pin 3 | Pin 2 |
| 2 | Pin 5 | Pin 4 |
| 3 | Pin 7 | Pin 6 |
| 4 | Pin 9 | Pin 8 |

### Czujniki PIR

| Czujnik | Pin Arduino |
|---|---|
| Czujnik 1 | 10 |
| Czujnik 2 | 11 |
| Czujnik 3 | 12 |
| Czujnik 4 | 13 |

Każdy czujnik PIR powinien być podłączony do zasilania, masy (GND) oraz odpowiedniego pinu sygnałowego Arduino.

## ⚙️ Zasada działania

1. Po uruchomieniu programu wszystkie kierunki mają czerwone światło.
2. Arduino stale odczytuje sygnały z czujników PIR.
3. Wykrycie zmiany sygnału z `LOW` na `HIGH` oznacza nowe zdarzenie ruchu.
4. Kierunek przypisany do aktywnego czujnika otrzymuje zielone światło.
5. Pozostałe kierunki mają czerwone światło.
6. Zielone światło pozostaje aktywne do momentu wykrycia nowego zdarzenia przez inny czujnik.
7. Jeśli nie zostanie wykryty kolejny ruch, ostatni stan sygnalizacji zostaje zachowany.

## 💻 Zastosowane funkcje

- `pinMode()` – ustawia piny Arduino jako wejścia lub wyjścia.
- `digitalRead()` – odczytuje stan czujników PIR.
- `digitalWrite()` – steruje diodami LED.
- `setup()` – inicjalizuje piny i ustawia początkowe światła.
- `loop()` – stale sprawdza stan czujników.
- `RISING` – oznacza przejście sygnału z `LOW` na `HIGH`, wykrywane w projekcie przez porównanie bieżącego i poprzedniego stanu czujnika.
- `delay(20)` – wprowadza krótką przerwę między odczytami.

## 🧠 Logika programu

Program zapamiętuje poprzedni stan każdego czujnika w zmiennych `poprzedni1`, `poprzedni2`, `poprzedni3` i `poprzedni4`.

Reakcja następuje tylko wtedy, gdy sygnał zmieni się z `LOW` na `HIGH`. Dzięki temu światła nie przełączają się wielokrotnie, gdy czujnik przez pewien czas utrzymuje stan `HIGH`.

Funkcja `wszystkieCzerwone()` ustawia wszystkie kierunki na czerwono, a `zieloneSwiatlo(nr)` aktywuje zielone światło wybranego kierunku i wyłącza jego światło czerwone.

## ▶️ Uruchomienie projektu

1. Otwórz projekt w Tinkercad Circuits.
2. Sprawdź poprawność połączeń.
3. Wklej kod do edytora Arduino.
4. Kliknij **Start Simulation**.
5. Zasymuluj wykrycie ruchu przez poszczególne czujniki PIR.
6. Obserwuj zmianę świateł.

## ⚠️ Uwagi

- Jeśli kilka czujników wykryje ruch jednocześnie, pierwszeństwo ma pierwszy aktywny czujnik według kolejności sprawdzania: 1, 2, 3, 4.
- Światła nie zmieniają się automatycznie co określony czas.
- Ostatni stan sygnalizacji zostaje zachowany do wykrycia kolejnego zdarzenia ruchu.
- W rzeczywistym układzie należy stosować odpowiednie rezystory przy diodach LED i prawidłowo podłączyć czujniki PIR.

## 🎯 Cel projektu

Celem projektu jest poznanie obsługi czujników ruchu PIR, sterowania diodami LED oraz wykrywania zmian stanów logicznych w Arduino. Projekt pokazuje, jak stworzyć prostą sygnalizację reagującą na ruch.

## 👨‍💻 Technologie

- Arduino C/C++
- Arduino Uno
- Tinkercad Circuits
