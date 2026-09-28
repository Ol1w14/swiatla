🚦 Sygnalizacja świetlna LED

Projekt przedstawia prostą symulację sygnalizacji świetlnej z wykorzystaniem Arduino oraz 8 diod LED — po dwie dla każdego z 4 kierunków.

📋 Opis projektu

Układ składa się z 4 zestawów świateł:

🔴 czerwone

🟢 zielone

Sygnalizacja działa naprzemiennie:

Kierunek 1 i 3 mają światło zielone.

Kierunek 2 i 4 mają światło czerwone.

Następuje zmiana świateł.

Kierunek 2 i 4 otrzymują światło zielone.

Kierunek 1 i 3 otrzymują światło czerwone.

Cykl powtarza się w nieskończoność.

🔌 Podłączenie
Kierunek	LED czerwona	LED zielona
1	Pin 2	Pin 3
2	Pin 4	Pin 5
3	Pin 6	Pin 7
4	Pin 8	Pin 9
⏱️ Czas działania

🟢 Zielone światło: 5 sekund

🔴 Zmiana świateł: 1 sekunda

Następnie zielone otrzymują przeciwne kierunki.

🛠️ Wymagane elementy

Arduino

4 × czerwona dioda LED

4 × zielona dioda LED

8 × rezystorów

płytka stykowa

przewody połączeniowe

💻 Kod

Program został napisany w języku C++ dla Arduino.

Główne funkcje wykorzystywane w projekcie:

pinMode()
digitalWrite()
delay()

▶️ Uruchomienie

Podłącz diody LED zgodnie z tabelą.

Otwórz kod w Arduino IDE.

Wybierz odpowiednią płytkę Arduino.

Wybierz właściwy port COM.

Wgraj program na Arduino.

Obserwuj działanie sygnalizacji.

🔄 Schemat działania
┌─────────────────────────────┐
│ Kierunek 1 🟢   Kierunek 3 🟢 │
│ Kierunek 2 🔴   Kierunek 4 🔴 │
└──────────────┬──────────────┘
               │ 5 s
               ▼
          Zmiana 1 s
               │
               ▼
┌─────────────────────────────┐
│ Kierunek 1 🔴   Kierunek 3 🔴 │
│ Kierunek 2 🟢   Kierunek 4 🟢 │
└──────────────┬──────────────┘
               │ 5 s
               ▼
          Zmiana 1 s
               │
               └──────► powtórzenie

📁 Struktura projektu
sygnalizacja-led/
│
├── sygnalizacja-led.ino
└── README.md

📜 Licencja

Projekt został wykonany w celach edukacyjnych.
