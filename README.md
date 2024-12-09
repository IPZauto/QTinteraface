# Adaptacyjny Interfejs Samochodowy Reagujący na Zmęczenie Kierowcy

## Opis

Projekt adaptacyjnego interfejsu samochodowego, który ma na celu zwiększenie bezpieczeństwa kierowcy poprzez monitorowanie i reagowanie na oznaki zmęczenia. Interfejs, zbudowany przy użyciu **Qt**, dynamicznie dostosowuje się w czasie rzeczywistym, oferując wizualne, dźwiękowe lub haptyczne powiadomienia, aby ostrzec kierowcę i zminimalizować ryzyko wypadku.

System jest zintegrowany z **Euro Truck Simulator 2 (ETS2)**, co pozwala testować rozwiązania w realistycznym środowisku symulacyjnym bez konieczności fizycznej jazdy pojazdem. Dane z ETS2 są wykorzystywane do monitorowania stanu kierowcy i symulowania scenariuszy zmęczenia.

## Funkcje

- **Wykrywanie zmęczenia**: Monitoruje zachowanie kierowcy za pomocą zintegrowanych czujników (np. śledzenie oczu, monitorowanie tętna) lub danych z ETS2.
- **Integracja z ETS2**: Pobiera dane o aktywności kierowcy (np. czas jazdy, czas postoju, prędkość) w celu symulacji zmęczenia w wirtualnym środowisku.
- **Adaptacyjny interfejs**: Dynamicznie dostosowuje elementy interfejsu (np. przyciemnienie świateł, uproszczenie układu) w zależności od stanu kierowcy.
- **System alertów**: Generuje ostrzeżenia w formie:
  - Sygnałów wizualnych (powiadomienia na ekranie, zmiany kolorów)
  - Sygnałów dźwiękowych (sygnały dźwiękowe, komunikaty głosowe)
  - Haptycznych (wibracje w kierownicy lub fotelu)
- **Konfigurowalne progi**: Użytkownik może dostosować czułość systemu w wykrywaniu zmęczenia, co pozwala na dopasowanie do różnych warunków jazdy i indywidualnych potrzeb.
- **Rozszerzalna architektura**: Łatwa integracja z innymi systemami pojazdu, takimi jak autopilot, nawigacja czy urządzenia IoT.

## Użyte technologie

- **Qt Framework**: Tworzenie interfejsu i zapewnienie kompatybilności między platformami.
- **C++/QML**: Główne języki programowania użyte do logiki i projektowania UI.
- **Modele uczenia maszynowego** (opcjonalnie): Wykrywanie zmęczenia na podstawie danych z czujników.
- **Integracja z ETS2**: Korzystanie z API telemetrycznego ETS2 do pobierania danych o stanie gry.
- **Integracja z czujnikami**: API do współpracy z zewnętrznymi urządzeniami w celu zbierania danych w czasie rzeczywistym.

## Instalacja

1. **Wymagania wstępne**:

   - Środowisko programistyczne Qt (zalecana wersja 6.0 lub nowsza)
   - Kompilator C++
   - Kompatybilny system operacyjny: Windows, macOS lub Linux
   - Euro Truck Simulator 2 z włączonym API telemetrycznym
   - (Opcjonalnie) Python do integracji z modelami ML

2. **Sklonuj repozytorium**:

   ```bash
   git clone https://github.com/username/adaptive-automotive-interface.git
   cd adaptive-automotive-interface
   ```

3. **Zbuduj projekt**:

   - Otwórz projekt w Qt Creator.
   - Skonfiguruj ustawienia kompilacji zgodnie z używaną platformą.
   - Skompiluj i uruchom projekt.

4. **Skonfiguruj ETS2**:

   - Włącz API telemetryczne w ETS2, modyfikując plik konfiguracyjny `config.cfg`:
     ```text
     uset g_developer "1"
     uset g_console "1"
     ```
   - Skonfiguruj ścieżkę dostępu do API telemetrycznego w aplikacji.

5. **Skonfiguruj czujniki**:
   - Podłącz obsługiwane czujniki (np. kamera do śledzenia oczu, urządzenie noszone do monitorowania tętna).
   - Skonfiguruj ustawienia czujników w aplikacji.

## Użytkowanie

1. Uruchom aplikację.
2. Skalibruj system, korzystając z kreatora konfiguracji, aby dostosować czułość do swoich preferencji.
3. Uruchom ETS2 i zacznij jazdę. System będzie:
   - Pobierał dane z ETS2 w czasie rzeczywistym.
   - Monitorował Twój stan.
   - Generował adaptacyjne powiadomienia lub alerty w przypadku wykrycia oznak zmęczenia.

## Współpraca

Zapraszamy do współpracy nad tym projektem! Aby wnieść swój wkład:

1. Sforkuj repozytorium.
2. Utwórz nową gałąź (`feature/nazwa-funkcji`).
3. Wprowadź swoje zmiany i zatwierdź je.
4. Zgłoś pull request.

## Licencja

Projekt jest licencjonowany na podstawie licencji MIT. Szczegóły znajdują się w pliku [LICENSE](LICENSE).

## Kontakt

W razie pytań lub potrzeby wsparcia, prosimy o kontakt:

- **Autor**: Twoje Imię
- **E-mail**: twoj.email@example.com
- **GitHub**: [Twój profil GitHub](https://github.com/username)

Możesz rozbudowywać ten plik `README.md` o szczegółowe instrukcje lub informacje, które pojawią się w trakcie rozwoju projektu. 🚗
