# [EN] SPSS Data Weighter - Raking/IPF Automation Tool

## 1. Project Goal
A local GUI application designed to automate survey sample weighting in SPSS using the Iterative Proportional Fitting (IPF) / Raking algorithm. It ensures datasets align with target demographic proportions while maintaining full statistical and structural integrity.

## 2. Vibe Coding & Development Approach
This tool was created using the "vibe coding" methodology in collaboration with AI models. As the system architect, I focused on the mathematical and methodological requirements: defining the IPF convergence loop, implementing weight trimming (capping) to prevent extreme variance, and designing the logic for reverse-mapping Excel string labels to SPSS numeric codes. AI handled the Tkinter GUI implementation and standard data manipulation boilerplate. This synergy allowed me to quickly prototype a statistically robust tool without getting bogged down in manual syntax generation.

## 3. Key Features
- **Smart Metadata Mapping:** Automatically maps text labels from Excel (e.g., "Female") back to SPSS numeric codes (e.g., "2") by parsing the `.sav` file's internal dictionary.
- **Flexible Target Entry:** Load target proportions via an Excel template or input them manually through a dynamic interface.
- **Weight Trimming:** Built-in limits (e.g., 0.33 to 3.0) clip extreme weights, preventing individual respondents from skewing the final analysis.
- **Lossless Metadata Export:** Generates the new weighted `.sav` file while preserving all original variable labels, value labels, and formatting.

## 4. Security & Data Protection
**Zero-Cloud Architecture.** Weighting often involves sensitive demographic data. This application processes `.sav` files 100% locally on the user's machine using `pandas` and `pyreadstat`. No datasets or target matrices are sent to external servers or AI APIs, ensuring full compliance with GDPR and academic data security standards.

## 5. Performance & Limitations
- **Algorithm Constraints:** The IPF algorithm is capped at 50 iterations with a 1e-4 tolerance. While sufficient for standard survey weighting, highly complex or sparse target matrices might not perfectly converge within these limits.
- **In-Memory Processing:** Uses RAM for matrix calculations, which is highly efficient for typical survey samples but bounded by system hardware for exceptionally massive datasets.
- **Environment Limit:** The output directory is hardcoded to `C:\WAGA SPSS`, requiring a Windows OS environment.

## 6. Future Roadmap
Planned enhancements to the open architecture include:
- **Dynamic Save Path:** Replacing the hardcoded output directory with a user-selected folder via the GUI.
- **Convergence Reporting:** Adding a post-processing log that informs the user whether the IPF algorithm successfully converged or hit the 50-iteration limit.
- **Effective Base Calculation:** Automatically calculating and reporting the Weighting Efficiency / Effective Sample Size post-trimming.

## 🛠️ Requirements & Execution
- Python 3.x
- Libraries: `pip install pandas numpy pyreadstat openpyxl`
- Run: `python wazarka.py`

---

# [PL] Ważarka SPSS - Automatyzacja Ważenia Danych (Raking/IPF)

## 1. Cel projektu
Lokalna aplikacja z interfejsem graficznym (GUI), automatyzująca proces ważenia prób badawczych w plikach SPSS za pomocą algorytmu Raking (Iterative Proportional Fitting). Pozwala na szybkie dostosowanie struktury próby do rozkładów populacyjnych przy zachowaniu pełnej integralności statystycznej bazy.

## 2. Podejście do tworzenia (Vibe Coding)
Narzędzie powstało w modelu "vibe codingu" przy wsparciu modeli AI. Jako projektant skupiłem się na poprawności metodologicznej: zdefiniowałem pętlę konwergencji dla algorytmu IPF, logikę przycinania wag (trimming) oraz mechanizm odwróconego mapowania etykiet tekstowych z Excela na kody numeryczne SPSS. Sztuczna inteligencja zajęła się generowaniem kodu interfejsu (Tkinter) i rutynowych przekształceń danych. To dowodzi, że znajomość statystyki i logiki badawczej pozwala sprawnie budować własne oprogramowanie z pomocą AI, bez konieczności ręcznego pisania każdej funkcji.

## 3. Kluczowe Funkcje
- **Inteligentne Mapowanie:** Automatycznie dopasowuje etykiety tekstowe z Excela (np. "Kobieta") do kodów w SPSS (np. "2") wykorzystując wbudowany słownik bazy.
- **Elastyczne Źródła Danych:** Możliwość wczytania proporcji celowych z pliku Excel (3 kolumny) lub wpisania ich ręcznie w dynamicznym oknie.
- **Trimming Wag:** Funkcja limitowania wag (np. w zakresie 0.33 - 3.0), zapobiegająca powstawaniu wag ekstremalnych, które mogłyby zaburzyć wariancję bazy.
- **Bezstratny Eksport:** Skrypt tworzy nową zmienną `WAGA` i zapisuje plik, zachowując wszystkie oryginalne etykiety zmiennych i wartości.

## 4. Bezpieczeństwo i ochrona danych
**Brak integracji z chmurą.** Ważenie danych demograficznych wymaga poufności. Skrypt przetwarza bazę całkowicie lokalnie w pamięci urządzenia za pomocą bibliotek `pandas` i `pyreadstat`. Żadne dane, w tym struktura próby, nie są wysyłane do zewnętrznych usług, co gwarantuje pełną zgodność z RODO oraz wymogami projektów uczelnianych i komercyjnych.

## 5. Wydajność i ograniczenia
- **Limity algorytmu:** Raking jest ograniczony do 50 iteracji z tolerancją błędu na poziomie 1e-4. Dla standardowych badań jest to wartość optymalna, jednak przy bardzo rzadkich lub skomplikowanych macierzach celów, algorytm może nie osiągnąć pełnej konwergencji.
- **Zależność od Windows:** Wymuszenie zapisu pliku wynikowego do sztywno ustalonego folderu (`C:\WAGA SPSS`) sprawia, że program w obecnej wersji jest natywnie dedykowany pod system Windows.

## 6. Perspektywy rozwoju
Do najbliższych planów rozwojowych aplikacji należą:
- **Wybór folderu zapisu:** Wdrożenie okna dialogowego pozwalającego zapisać plik w dowolnym miejscu.
- **Raport z konwergencji:** Dodanie komunikatu informującego użytkownika, czy wagi "spięły się" przed osiągnięciem limitu 50 iteracji, czy algorytm został przerwany wymuszeniem.
- **Efektywność ważenia:** Wyliczanie i raportowanie efektywnej wielkości próby (Effective Sample Size) po zastosowaniu limitów (trimmingu).

## 🛠️ Wymagania i Uruchomienie
- Python 3.x
- Biblioteki: `pip install pandas numpy pyreadstat openpyxl`
- Uruchomienie: `python wazarka.py`
