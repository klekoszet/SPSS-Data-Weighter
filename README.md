# [EN] SPSS Data Weighter - Raking/IPF Automation Tool

A professional GUI-based tool designed for Data Processing (DP) specialists to automate sample weighting in SPSS using the Raking (Iterative Proportional Fitting) algorithm.

## 🚀 Key Features
- **Smart Mapping:** Automatically maps labels from Excel (e.g., "Female") to SPSS numeric codes (e.g., "2") by analyzing file metadata.
- **Flexible Target Entry:** Load target proportions directly from an Excel file or enter them manually via a dynamic interface.
- **Weight Trimming:** Features built-in capping (min/max limits) to prevent extreme weights and ensure the statistical validity of the dataset.
- **Metadata Preservation:** Generates the weighted file while keeping all original SPSS variable labels, value labels, and formats intact.

## 🛠️ Requirements
- Python 3.x
- Libraries: `pandas`, `numpy`, `pyreadstat`, `openpyxl`

`pip install pandas numpy pyreadstat openpyxl`

## 📖 How to Use
1. **Load SPSS File:** Select the `.sav` data file you wish to weight.
2. **Define Targets:** - Use an **Excel file** with three columns: Variable Name, Category, and Target Proportion (e.g., 0.5 for 50%).
   - OR use **Manual Mode** to input proportions directly into the interface.
3. **Set Limits:** Define the minimum and maximum allowed weights (default limits: 0.33 - 3.0).
4. **Run:** The tool will calculate the weights and generate a new `.sav` file containing the calculated `WAGA` variable in the designated output folder.

---

# [PL] Ważarka SPSS - Automatyzacja Ważenia Danych (Raking/IPF)

Profesjonalne narzędzie z interfejsem graficznym (GUI) stworzone dla specjalistów Data Processing, automatyzujące proces ważenia prób w plikach SPSS przy użyciu algorytmu Raking (Iterative Proportional Fitting).

## 🚀 Kluczowe Funkcje
- **Inteligentne Mapowanie:** Automatycznie dopasowuje etykiety z pliku Excel (np. "Kobieta") do kodów numerycznych w SPSS (np. "2") na podstawie analizy metadanych pliku.
- **Elastyczne źródła danych:** Możliwość wczytania proporcji docelowych bezpośrednio z arkusza Excel lub ręcznego zdefiniowania ich w interfejsie programu.
- **Trimming (Przycinanie wag):** Wbudowana funkcja limitowania wag (min/max), zapobiegająca powstawaniu wag ekstremalnych i dbająca o poprawność statystyczną zbioru.
- **Zachowanie Metadanych:** Zapisuje wynikowy plik, zachowując wszystkie oryginalne etykiety zmiennych, etykiety wartości oraz formaty SPSS.

## 🛠️ Wymagania
- Python 3.x
- Biblioteki: `pandas`, `numpy`, `pyreadstat`, `openpyxl`

`pip install pandas numpy pyreadstat openpyxl`

## 📖 Instrukcja Obsługi
1. **Wybierz plik SPSS:** Wskaż bazę danych w formacie `.sav`.
2. **Zdefiniuj cele (Targets):**
   - Użyj **pliku Excel** z trzema kolumnami: Nazwa Zmiennej, Kategoria, Proporcja Docelowa (np. 0.4 dla 40%).
   - LUB wybierz **Tryb Ręczny**, aby wpisać wartości bezpośrednio w oknach dialogowych.
3. **Ustaw Limity:** Określ dolną i górną granicę wagi (standardowy zakres: 0.33 - 3.0).
4. **Generuj:** Program wyliczy wagi i utworzy nowy plik `.sav` z dodaną zmienną `WAGA` w zdefiniowanym folderze roboczym.
