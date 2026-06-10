# Warcaby (Checkers) - JavaFX

Gra w warcaby (klasyczny wariant) napisana w języku Java z wykorzystaniem biblioteki graficznej JavaFX. Aplikacja oferuje rozgrywkę lokalną dla dwóch graczy z wbudowanym systemem zegarów szachowych.

### 🌟 Główne funkcje

* **Lokalna gra wieloosobowa (1vs1):** Rozgrywka na jednym komputerze (Hot-Seat).
* **Pełna mechanika warcabów:** Implementacja wymuszonego bicia, ruchu do tyłu podczas bicia wielokrotnego oraz promocji zwykłych pionków na damki (Kings).
* **Zegary szachowe:** Każdy z graczy ma domyślnie 10 minut na całą partię. Czas odlicza się w czasie rzeczywistym.
* **Rejestr ruchów:** Boczny panel wyświetlający historię i czas trwania poszczególnych ruchów dla koloru białego i czerwonego.
* **Przygotowanie pod tryb sieciowy:** Interfejs zawiera menu z zaplanowanym trybem LAN (obecnie w fazie rozwoju).

---

### 🛠 Technologie

Projekt został zbudowany z użyciem nowoczesnego stosu technologicznego dla aplikacji okienkowych Java:

* **Język:** Java 23
* **GUI:** JavaFX 17.0.6 (Controls & FXML)
* **Narzędzie budowania:** Maven (z wbudowanym Maven Wrapper)
* **Testy:** JUnit 5.10.2 (skonfigurowane w `pom.xml`)

---

### ⚙️ Wymagania systemowe

Aby skompilować i uruchomić projekt na swoim komputerze, potrzebujesz:

* Zainstalowanego **Java Development Kit (JDK)** w wersji **23** lub nowszej.
* Zmiennej środowiskowej `JAVA_HOME` wskazującej na folder z instalacją JDK.
* *Nie musisz instalować Mavena – projekt korzysta z dołączonego skryptu Maven Wrapper (`mvnw`).*

---

### 🚀 Instrukcja instalacji i uruchomienia

Skorzystaj z wbudowanego pluginu `javafx-maven-plugin`, aby automatycznie pobrać zależności, skompilować kod i uruchomić grę.

**Dla systemu Windows:**
Otwórz terminal (Wiersz polecenia lub PowerShell) w głównym katalogu projektu i wpisz:
```cmd
mvnw.cmd clean javafx:run
```

**Dla systemów Linux / macOS:**
Otwórz terminal w głównym katalogu projektu, nadaj uprawnienia do wykonywania skryptu (tylko za pierwszym razem) i uruchom grę:
```bash
chmod +x mvnw
./mvnw clean javafx:run
```

---

### 📂 Struktura projektu

Główna logika aplikacji jest podzielona na czytelne klasy i pakiety:

| Plik / Klasa | Opis |
| :--- | :--- |
| `CheckersApp.java` | Główna klasa startowa aplikacji JavaFX. |
| `CheckersGame.java` | Zarządza interfejsem graficznym (GUI), menu, planszą i zegarami. |
| `GameLogic.java` | Silnik gry. Odpowiada za weryfikację ruchów, bicia, promocję i warunki wygranej. |
| `Piece.java` & `Tile.java` | Reprezentacja wizualna i stanowa pionków oraz pól na planszy. |
| `MoveResult.java` & `MoveType.java` | Klasy pomocnicze do obsługi rezultatów i typów ruchów (zwykły, bicie, brak ruchu). |
| `pom.xml` | Plik konfiguracyjny Maven zawierający zależności JavaFX. |

---

### 🤝 Autorzy i rozwój
Projekt jest gotowy do rozbudowy. Najbliższym zaplanowanym krokiem w rozwoju aplikacji jest wdrożenie pełnoprawnego trybu **LAN** do gry przez sieć lokalną, opierając się na architekturze klient-serwer.
