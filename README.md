🚦 Sygnalizacja świetlna LED
📋 Opis projektu

Projekt przedstawia prostą symulację sygnalizacji świetlnej z wykorzystaniem Arduino oraz 8 diod LED.

🚦 Działanie

Sygnalizacja działa naprzemiennie:

Kierunek 1 i 3 mają światło zielone.

Kierunek 2 i 4 mają światło czerwone.

Następuje zmiana świateł.

Kierunek 2 i 4 otrzymują światło zielone.

Kierunek 1 i 3 otrzymują światło czerwone.

Cykl powtarza się w nieskończoność.

🔌 Podłączenie
💡 Piny LED
Kierunek	LED czerwona	LED zielona
1	Pin 2	Pin 3
2	Pin 4	Pin 5
3	Pin 6	Pin 7
4	Pin 8	Pin 9
⏱️ Czas działania
🟢 Zielone światło

Czas świecenia: 5 sekund

🔄 Zmiana świateł

Czas zmiany: 1 sekunda

🛠️ Wymagane elementy
📦 Lista elementów

Arduino

4 × czerwona dioda LED

4 × zielona dioda LED

8 × rezystorów

Płytka stykowa

Przewody połączeniowe

💻 Kod
🧑‍💻 Wykorzystane funkcje

Program został napisany w języku C++ dla Arduino.

pinMode()
digitalWrite()
delay()

▶️ Uruchomienie
📌 Instrukcja

Podłącz diody LED zgodnie z tabelą.

Otwórz kod w Arduino IDE.

Wybierz odpowiednią płytkę Arduino.

Wybierz właściwy port COM.

Wgraj program na Arduino.

Obserwuj działanie sygnalizacji.

🔄 Schemat działania
🚦 Cykl 1
Kierunek 1 🟢    Kierunek 3 🟢
Kierunek 2 🔴    Kierunek 4 🔴

🔄 Zmiana
Zmiana świateł - 1 sekunda

🚦 Cykl 2
Kierunek 1 🔴    Kierunek 3 🔴
Kierunek 2 🟢    Kierunek 4 🟢

🔁 Powtórzenie

Po zakończeniu drugiego cyklu program wraca do pierwszego i cały proces jest powtarzany.

